# Elastic Compute Cloud (EC2)

## Amazon EC2 overview

* Vurtal Machine (so called __instance__)
* Guest OS are
  * Linux or Windows
  * MacOS (since Feb 23, 2021, [source](https://aws.amazon.com/about-aws/whats-new/2021/02/amazon-ec2-mac-instances-now-support-macos-big-sur/))
* Hypervisors are:
  * Xen
  * Nitro
* Bare metal availability
* EC2 types that variously combine CPU, memory, disk, network IO
* 20 EC2 software limit - to increase raise AWS support ticket
* EC2 hourly fee includes OS license

### Amazon EC2 Architecture

AWS responsibility (""):

* Rack, chassis, etc.
* Intel Xeon (basically CPU)
* Hypervisor (Xen/Nitro)

Customer respnsibility:

* Instance

Normally, the "physical part" is shared by multiple customers - `Multitenant environment`.

`Single tenant environment` - so-called `Dedicated Instance` - the host that hosts customer's EC2 instances belongs only to one customer.

`Dedicated Host` - a host, "physical part", that belongs to the only customer. It allows to bring the applications where the licensing tied to the physical portion of the host (Core count, etc.)

### AMI - Amazon Machine Image

* It's a bit-for-bit copy of root
* It can represents Linux, Windows, FreeBSD
* It may also include additional software/packages
* It represents the state of the machine when the AMI was created

## EC2 Best Practice

* Any EC2 instance has to be treated as disposable - due to failure of any reason
* The EC2 infrastructure has to be immutable - once EC2 instance is failed the next in line should have the same state and behaviour as its predecessor. If changes are required the AMI has to be adjusted accordingly and reused for the new EC2 instances - not log in to the EC2 instance and doing something manually
* Logs may dissapear once EC2 is gone. The logs has to be sent to proper destination for the further analysis and has to be treated as a stream
* Each deployment has to be automated to make the processes more efficient and secure
* Monitoring the EC2 instances with CloudWatch
* Enable scaling and self-healing with Auto Scaling
