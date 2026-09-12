# DynamoDB Best Practices

## Key Design

- Partition key determines data distribution—high-cardinality keys spread load evenly
- Hot partition = one key gets all traffic—use composite keys or add a random/bucket suffix when a single entity is extremely hot
- Sort key enables range queries within a partition—design sort keys for the real access patterns (time, status, version)
- Keys cannot change after table creation—enumerate read/write paths before provisioning

## Single-Table Design

- One table can hold multiple entity types—prefix partition keys: `USER#123`, `ORDER#456`
- Overloaded sort keys encode item role: `METADATA`, `ORDER#2024-01-15`, `ITEM#abc`
- Queries may return mixed types—filter client-side or use `begins_with`
- Single-table is a tool, not doctrine—start from access patterns; split tables when isolation or blast-radius matters

## Access-Pattern First Modeling

1. List every required query as “given X, return Y ordered by Z”
2. Assign partition keys that isolate those lookups and keep cardinality healthy
3. Add sort keys only where range, ordering, or adjacency is needed
4. Introduce GSIs for alternate paths that the base table cannot serve efficiently
5. Prefer sparse indexes when only a subset of items should appear in the alternate path
