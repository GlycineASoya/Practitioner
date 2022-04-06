# Pricing

## On-Demand pricing

* No long-term commitments
* Transform large costs into small costs (pay-as-you-go)
* Includes OS licence
* Per hour - *hour forward*
* Per minute - minimum 60 seconds
* Good to use if:
  * Low cost and flexibility is required
  * No up-front payment or long-term commitment
  * For short-term application
  * For spiky or unpredictable workload applications
  * For applications, which workload cannot be interrupted

## Reserved Instances (RI) pricing

* It gives 75% of discount comparing to On-Demand
* Provides *capacity reservation* (as it's Reserved)
* 1/3 years term
* Ability to specify:
  * Instance type
  * Platform
  * Tenancy
  * AZ

### Types of Reserved Instances

* Standard RI
  * 75% of discount
  * Good to use for steady-state purpose (DB that has to be run 60% of all the time, for example)
* Convertible RI
  * Up to 54% of discount
  * The attributes can be changed
  * Good as same as Standard RIs
* Scheduled RI
  * Good to use for a schedule load - once RI is scheduled at this time the discount will be applied (time-window task, reports once per week, for example)

## Spot Pricing

* Up to 90% if discount comparing to On-Demand
* Gives a discoung based on a) size of machine, b) type of machine, c) particular AZ
* Spot instances *can be interrupted*
* How it works:
  * I say for the m4.large in Ireland (eu-west-1a) I can pay 10 cents/hour, for example
  * Customers come, request more resources from AWS and the price of my particular machine is going up, as demand is higher than offer
  * AWS sets for my machine type (m4.large) in chosen AZ (**eu-west-1a**) 11 cents/hour
  * If I won't pay this charge the machine *will be interrupted* and *terminated* and will be given to another customer who will be able to that charge
  * If I won't pay this charge the machine will show 2-minutes warning via Metaserver, which should be noticed by our application running on that machine
* Good for application that are flexible with start/end times
* Good for Dev/Test environments
* Examples: Image rendering, Video transcoding, Analytics
* Integrated with:
  * Amazon EMR
  * Auto Scaling
  * Elastic Container Service (ECS)
  * CloudFormation

## Lambda Pricing

* Charged per GB RAM per 100 ms
* Charged per 1M requests
* Free:
  * 1M requests/mth
  * 400 000 GB-s/mth
* Additional charges:
  * Bandwidth
  * S3 bucket (store the result)

## Transfer Pricing

* Inbound is free
* S3 to CloudFront is free
* Outbound to Internet is NOT free:
  * $/GB/mth
  * Cross-region traffic $/GB/mth
  * Cross-AZ traffic $/GB/mth
  * Cross-VPC traffic $/GB/mth
  * Tiered pricing (wholesale cheaper)
