# DynamoDB Limits and Capacity

## TTL

- Enable TTL on a numeric timestamp attribute—DynamoDB deletes expired items in the background
- Deletion is not instantaneous—items may remain queryable for hours after expiry
- TTL values are Unix epoch **seconds**; milliseconds fail silently
- When freshness matters in queries, filter with `attribute_exists(ttl) AND ttl > :now` in addition to relying on TTL deletion

## Capacity

- On-demand: pay per request and auto-scale—good for spiky or unknown traffic
- Provisioned: set RCU/WCU—often cheaper at steady high scale, needs capacity planning
- Provisioned auto-scaling: set min/max and target utilization for smoother patterns
- `ProvisionedThroughputExceededException` means throttling—back off, retry, and fix hot keys or capacity

## Limits

- Item size max **400KB**—store large objects in S3 and keep references in DynamoDB
- Per-partition throughput guidance: roughly 3000 RCU and 1000 WCU before splitting load
- Query/Scan responses max 1MB—pagination is mandatory beyond that
- Keep attribute names short; attribute name + value sizes both count toward item size
