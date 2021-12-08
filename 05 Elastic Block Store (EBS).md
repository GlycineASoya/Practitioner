# Elastic Block Store (EBS)

* The main benefit of EBS is the access to the a block of information in the large file which allow to manipulate particular peace of information, not the whole file (comparing to object storage)
* It can be mounted, comparing to the object storage
* The best solution of random IO, comparing to object storage

## Benefits of EBS

* EBS data is independent of EC2 instance
* It's connected via network
* It's paid for the __provisioned__ storage
* EC2 and EBS should exists in one AZ
* Point-in-time snapshots are available and stored in S3
* Can be detached and attached
* Can be encrypted
* Can be used in RAID or LVM
