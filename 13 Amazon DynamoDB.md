# Amazon DynamoDB

* NoSQL DB
* Backend is SSD
* Single-digit ms response design
* Built-in security, resilience as it's managed by AWS
* Replicated across multiple AZ
* No limits to storage
* Provisioned throughput (we pay for Provisioned throughput)
  * Reads
  * Writes
  * Can auto-scale

## Amazon DynamoDB Tables

* No joints/replication
* Denormalization data
* Schema-less, need to specify unique primary key
* Secondary indexes could be specified
* No table size limit
* Item limit is 400KB
* Item-level TTL exists

## Use cases

* Ad impression/clicks
* Gaming leaderboards
* Shopping cards
* Session/stat storage
* Operational state/history (jenkins jobs result and similar)
