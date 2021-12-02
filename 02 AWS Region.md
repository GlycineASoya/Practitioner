# AWS Global Infrastructure

## Region

* Region is the primary building block of the AWS infrastructure
* Not every region has particular service
* Cost of services differs depends on Region
* Depends on the Region to the end user there is latency
* Each Region has it's own security and law peculiarities
* Each Region has 3 Availablity Zones

## Availability Zone

* Each Availbility Zone represents Data Centers (=>2)
* AZs are connected by a private fiber - low latency, high bandwidth

## Edge Location

* Gives such services as DNS
* Edge Location is located outside the Region
* There is NO direct access to the Edge Location
* Content Delivery Network leverages Edge Location cache in order to provide the seemless access to end users to services in a different Region
