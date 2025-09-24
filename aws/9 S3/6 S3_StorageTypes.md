```sh
Amazon S3 (Simple Storage Service) offers different types of storage classes to help optimize cost, performance,
and availability based on your data access patterns. Here's a breakdown of the main types:
```

## 1. S3 Standard
```sh
Use case: Frequently accessed data
Features:
	High durability and availability
	Low latency and high throughput
	Ideal for active content, websites, big data analytics
```
## 2. S3 Intelligent-Tiering
```sh
Use case: Data with unpredictable access patterns
Features:
  Automatically moves data between tiers (frequent, infrequent, archive)
  Optimizes cost without performance impact
  No retrieval fees
```
## 3. S3 Standard-IA (Infrequent Access)
```sh
Use case: Data accessed less frequently but needs quick access
Features:
  Lower cost than Standard
  Retrieval fee applies
  Good for backups and disaster recovery
```
## 4. S3 One Zone-IA
```sh
Use case: Infrequently accessed data that can be recreated if lost
Features:
  Stored in a single AZ (Availability Zone)
  Lower cost than Standard-IA
  Less resilient (no multi-AZ redundancy)
```
## 5 S3 Glacier Instant Retrieval
```sh
Use case: Long-lived archive data accessed once a quarter
          Instant retrieval in milliseconds
          Stored in 3 AZ
          Per-GB retrival fees apply
```
## 6. S3 Glacier Flexible Retrieval (formerly Glacier)
```sh
Use case: Long-lived archive data accessed once a year
          Archival data with retrieval times in minutes to hours
          Stored in 3 AZ
          Per-GB retrival fees apply
```

## 7. S3 Glacier Deep Archive
```sh
Use case: Long-term archival (e.g., 7–10 years)
Features:
  Lowest cost storage class
  Retrieval time: 12–48 hours
  Best for rarely accessed data with long retention requirements
```
## 8. S3 Reduced Redundancy Storage (Deprecated)
```sh
Use case: Non-critical, reproducible data
Note: AWS recommends using other classes like One Zone-IA instead.
```
