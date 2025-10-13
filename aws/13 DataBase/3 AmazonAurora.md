```sh
An online game using Aurora to manage real-time game state, player data, and leaderboards, ensuring low latency
 and high availability for a smooth gaming experience
Amazon Aurora is a cloud-native relational database service provided by Amazon Web Services (AWS). It is
compatible with MySQL and PostgreSQL, offering the performance and availability of high-end commercial databases
with the simplicity and cost-effectiveness of open-source databases.

Aurora is available in 2 compatibility Modes
  1. MySQL Compatibility Edition
  2. PostGreSQL Compatibility Edition

Aurora DB will store 6 copies of your data across 3 Availability Zones
Aurora can provide upto 5X better performance than the MySQL & 3x better Performance than the  PostGreSQL Database
 instances.
Aurora Costs you 1/10th of any other commercial database engines.
Aurora Storage supports self-healing feature, which can recover the storage Disk from the minor issues automatically.
Aurora supports Back-Track feature, at an extra cost.
Automatic monitoring with failover
```
## Read Replicas in Amazon RDS:
```sh
Read replicas in Amazon RDS are copies of your primary (source) database that are asynchronously replicated to a 
different AWS region or within the same region.
Read replicas can be used to offload read queries from your primary database, improving read scalability and
performance.
They can also be promoted to become standalone databases in the event of a failure of the primary database.
```
## Snapshots in Amazon RDS:
```sh
Snapshots in Amazon RDS are backups of your database instance that capture the entire state of your database
 at the time the snapshot was taken.
Snapshots are stored in Amazon S3 and can be used to restore your database to a specific point in time.
You can also create automated snapshots that are taken at regular intervals.
```
## Point-In-Time Recovery (PITR) in Amazon RDS:
```sh
Point-In-Time Recovery (PITR) in Amazon RDS allows you to restore your database to any second during your backup
 retention period, up to the last five minutes.
PITR uses your automated database backups and transaction logs to restore your database to the specified point in time.
```

## Demo1
```sh
1. Create an Aurora Database instance with MySQL Compatibility Edition using Single-AZ deployment.
2. Create an Aurora Database instance with MySQL Compatibility Edition using Multi-AZ deployment.
```
## Demo2
```sh
1.	Create an Aurora DB and Connect your MySQL WorkBench and create an table.
2.	Create an Manual Snapshot of AuroraDB
3.	Copy snapshots from N.Virginia to Mumbai Region.
```



