# Core Services

## AWS VPC

* Logically isolated network
* VPC is per account per Region
* VPC can use AZ of the Region
* VPC can peer with another VPCs
* VPC allows to create Internet/VPN gateways
* VPC provides security mechanisms, like Firewalls
* Default limit of VPCs per Region is 5, which can be increased via AWS Support
* It's possible to get VPC with overlapped/same IP ranges - no peering for them
* VPC has to be divided to Subnet per AZ

## Routing and Firewalls

### Routing

1. A Routing Table (rtb) contains a routing information based on the network IP ranges
2. Default route is 0.0.0.0/0 - all traffic - should be at the end and points to the Internet Gateway (igw)
3. rtb has to be explicitly associated to the Subnet of a VPC. The Subnet with the access to the Internet is called "Public"
4. A EC2 Instance in the "Public" subnet is assigned with a public IP address. This EC2 Instance is rechable from the Internet as well as Internet can be reached from this EC2 Instance
5. "Public" Subnet is considered DMZ

### NACL (nackle) - Network Access Control List

1. NACL is a Firewall for the WHOLE Subnet

### Security Groups

1. Security Group is a Firewall for a particilar machines
2. Normally Security Groups are created for the particular service the machine serves

## DNS - AWS Route 53

* Globally distributed service
* It allows registering domains
* Use AWS nameservers - reliable
* Allows to configure public, available from the Internet, and private, from VPC, DNS zones
* Automated via API
* Supports Health Checks - HTTP/S heartbeat
* Provides different routing methods:
  * Latency based routing
  * Geographic (in USA can be orginized by state)
  * Failover - when something failed the end user is sent to a failover point
  * Weighted Sets - based on percentage of traffic from one location to a service in another

## VPN - Virtual Private Network

* Useful to leverage Hybrid Cloud
* Uses AWS Hardware
* Establishes Hardware-enabled IPSEC VPN tunnel

### Direct Connect

* Provides better network performance
* Leverages AWS Direct Connect Point of Presence (POP) to run a dedicated fiber connection from our office to a Region
* Uses local ISPs
* A Connection is 1/10 Gb/s __fiber__ connection
