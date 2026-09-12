# DynamoDB Operations

## Query vs Scan

- Query uses partition key + optional sort key—O(items in the matched partition slice); prefer it
- Scan reads the entire table—expensive, slow, and usually a missing-index smell
- “I need to filter by X” usually means add a GSI or sparse index; do not make Scan + Filter the primary path
- `FilterExpression` applies **after** capacity is consumed—filtered-out items still cost reads

## Global Secondary Indexes

- GSI = different partition/sort key for alternate access patterns
- GSI reads are eventually consistent—writes propagate with lag
- Each GSI has its own capacity cost (on-demand or provisioned)
- Sparse index trick: only items that contain the indexed attribute appear in the GSI

## Pagination

- Results are capped at 1MB per request—callers must paginate
- `LastEvaluatedKey` present means more pages—pass it as `ExclusiveStartKey`
- Loop until `LastEvaluatedKey` is absent—do not assume one call is complete
- `Limit` caps evaluated items, not guaranteed returned matches—still paginate

## Consistency

- Reads are eventually consistent by default and may return stale data
- `ConsistentRead: true` provides strong consistency on base-table reads at 2x RCU
- GSI reads are always eventually consistent—no strong-consistency option
- Read-after-write paths need consistent reads, short retries, or a redesign

## Conditional Writes

- `ConditionExpression` implements optimistic locking and create-if-absent guards
- Prevent overwrites: `attribute_not_exists(pk)`
- Version check: `version = :expected` then increment
- `ConditionCheckFailedException` means re-read, recompute, and retry—do not blind-fail forever

## Batch Operations

- `BatchWriteItem` is **not** atomic—partial success is normal; always inspect `UnprocessedItems`
- Retry unprocessed items with exponential backoff (AWS SDKs help)
- Max 25 items per batch and 16MB total—split larger workloads
- No per-item conditions in batch writes—use `TransactWriteItems` when conditions + atomicity are required

## Transactions

- `TransactWriteItems` provides all-or-nothing multi-item writes
- Max 100 items per transaction and 4MB total
- `TransactGetItems` provides a consistent multi-item read snapshot
- Transactions cost about 2x normal operations—use only when atomicity is required
