# AWS Relational Database Service (RDS)

## Benefits

* Automated underlying processes:
  * OS and DB engine installation
  * OS patches and security compliance
  * DB engine minor patches
  * Backups (retained for 35 days), are deleted along with instance
  * Manual Smnapshots, retained indifentely, pushed to S3
  * Failover of DB
  * Multi AZ deployment, which prevents loss of network, compute failure, storage failure
  * Syncronous replication
  * RTO/RPO (Recovery Time Objective/Recovery Time Objective) are reduced to minutes.
    * Recovery Time Objective - data lost for a period of time does not exceed the maximum threshold, or tolerance, specified in Business Continuity Plan. Answers the question: `How much data will be lost after fail notification recieved`
    * Recovery Time Objective - period of time during which the process must be restored after a disaster. Answers the question: `How long does it take after fail notification recieved`

## Amazon Aurora

* Compatible MySQL 5.6, PSQL 9,6
* Increased performance, x3-5
* Storage up to 64TB
  * Autoscaled
  * Six copies across three AZs, maintaned by Aurora service
* Up to 15 read replicas
* Supports Multi-Master (write access)
* Aurora Serverless - get access to the SQL

## Data Migration

* Dump and import
* Backup/restore
* AWS Database Migration Service
  * Supports many DBs
  * Hetero/Homogeneous DBs
  * Depending on engines zero downtime can be achieved
  * Schema convertion tool
  * Continuous repliaction
