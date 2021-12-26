# Service Pricing

## RDS

* The price is related to:
  * Instance type
  * Licence of DB Engine
  * Reserved instance discount
  * Amount of storage
* Multi-AZ deployments 2x charged, because this implies two different machines
* Stotage charges based on:
  * $/GB/month for EBS volumes
  * $/provisioned IOPS/month

## DynamoDB

* Charged for *provisioned* throughput
* Charged for *storage consumed* (pay for what is in use)
