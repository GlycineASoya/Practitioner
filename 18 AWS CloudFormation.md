# AWS CloudFormation

* It's template-based infrastructure management system
* We use **Declarative** approach
* We can create a library for the automation
* Typical workflow: Template -CreateStack()-> AWS CloudFormation -> Stack
* Typical GIT workflow for IaaC Templates: Team Members -Commit-> Tempalte -PR-> Source Control -Hooks-> CI/CD Pipeline (-> Test -> Feedback -> Build -> AWS CloudFormation -> Feedback -> Stack -> Test -> Feedback)
