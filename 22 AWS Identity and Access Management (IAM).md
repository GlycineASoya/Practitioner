# AWS Identity and Access Management (IAM)

* Groups cannot be nested

## Credentials types

* Email address + Password -> Master account (root) access
* Username + Password -> AWS Web Console
* Access Key + Secret key -> CLI, SDK

## Policies

* Evaluation logic:
  * Defaults - implicit deny (implies all is NOT allowed)
  * Explicit deny (written that something is NOT allowed)
  * Explicit alow (written that something is allowed)

## DON'Ts

* Use credentials in
  * Code
  * Environment variables
* Share credentials with
  * 3rd parties
  * Enterprise users
  * Web users

## Roles

* To avoid above [DON'Ts](##DON'Ts)
* Roles use *temporary credentials*
* Roles *delegate* permissions to:
  * EC2 instance
  * AWS Service
  * A user (elevate privileges)
  * Separate account
* Same account Workflow: Policy -Apply to a Role-> Role -Assign to instance-> EC2 Instance -Gets temporary credentials from STS (**S**ecurity **T**oken **S**ervice) based on Role-> App on EC2 Instance, that accesses an SDK/other service
* Inter account Workflow:

`Admin` account|`Production` account
-|-
user1|`prodAdminRole` Role give *Trust Relationship*
|Policy to get access to `Production` services is assigned to `prodAdminRole` Role
Policy to *AssumeRole* `prodAdminRole` Role assinged to user1|
user1 gets STS token (temporary credentials)|
user1 has `Production` services access|

## Federated users

* The wellknown users that are outside AWS account
* They can use STS temporary credentials as well
