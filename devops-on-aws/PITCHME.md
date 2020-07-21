[comment]: <> (https://gitpitch.com/willstobo/gitpitch-talks/master?p=devops-on-aws)
## DevOps on AWS
---
### Key takeaways
- @size[32px](DevOps / Continous Integration / Continous Delivery)
- @size[32px](AWS DevOps Services)
- @size[32px](Implementing DevOps on AWS)
---

### Small slide on DevOps? Intro to new section?
+++

### What is DevOps?
- Combination of practices and tools, enabling an organisation to deliver applications and services at high velocity.
- The ability to more comfortably and quickly deploy software and infrastructure resources than traditional practices
+++

### Why use DevOps?
@ul
- Remaining competitive. - rapidly changing environment, companies are releasing faster then before.
- Evolving security & performance requirements. - Things change quickly, its important to be able to remain on top of application requirements
- Maintain stability, increase velocity. - Enables higher reliability on processes and stability, whilst shortening your release cycles.
@ulend
---

### Small slide on CI/CD? Intro to new section?
+++

### Continous Integration (CI)
@ul
- Practice of regular building, testing and validation of code.
- Enables developers to build one to many times a day, pushing out and testing changes as they are finished.
- The key goals of CI are to find bugs, improve software quality and reduce the turn around time of new software updates.
@ulend
+++

### Continous Delivery (CD)
@ul
- Practice of automatically building, testing and preparing code for production releases.
- Expands upon CI by deploying all changes to a testing environment.
- Can be fully automated, or partially automated with manual gates for critical steps.
@ulend
---

### AWS DevOps Services
@snap[south]
![AWS-DevOps-Services](devops-on-aws/aws-devops-services.jpg)
@snapend

@ul
- CodeCommit - Fully Managed Git based source control service.
- CodeArtifact - Fully Managed Artifact repository service
- CodeBuild - Managed CI Service for Build / Testing
- CodeDeploy - Deployment Service
- CodePipeline - CD Service
@ulend
+++

### AWS CodeCommit
Fully Managed Git based source control service.
Access management provided via IAM
+++

### AWS CodeArtifact
Fully Managed Artifact repository service
Supports Node, Maven, etc etc repositories

Artifact Storage for applications
Repos are placed in domains, IAM permissoins can be applied at the domain level.
Can add NPM repo into CodeArtifact, can then download from NPM Repo in CodeBuild
Publish NodeJs app
1. Login to code artifact repo
2. npm set scope to codeartifactory repo
3. use npm publish with scope
+++

### AWS CodeBuild
Build steps are run in containers managed by AWS.
Buildspec yaml is used to define the build task, can be sourced in by an S3 bucket or be located alongside the sourcecode
Can create reports and store them in builds.

---?code=devops-on-aws/buildspec.yml&lang=YAML&title=Build Spec
+++

### AWS CodeDeploy
AWS CD Service 
Capable of deploying to ECS, Lambda & EC2 (Including on-premise machines)

1. Make EC2
2. Setup Deployment Group
3. Define deployment steps?

+++?code=devops-on-aws/appspec.yml&lang=YAML&title=App Spec
+++

### CodePipeline
Fits all the pieces together into a single pipeline
CodeCommiit -> CodeBuild -> CodeDeploy
Handles the automated starting of the pipelines
---

### Diagram of flow?
Maybe Demo, show pipeline, start pipeline then...
Show Diagram of what pipelines are doing in the background
Show pipeline results
Have already green pipeline as a backup for live failure
---

### Demo
Show App Running
Build
Test - Store artifact into build?
Deploy
---

### IaC
Ability to define infrastructure resources as code.
Can provide the code to a services that will automatically provision these assets.
Allows for consistently defined resources with instant provisioning.
- show how pipelines in aws can be setup via code.
---

### Recap
- @size[32px]()
- @size[32px]()
- @size[32px]()
---
# Questions?

Note:
- What flow of presentation makes sense?
- Intro
- Quick intro to CI/CD/Devops and its benefits?
- Then onto AWS DevOps services
-     How we can use AWS to easily enable CI/CD practices
-     AWS DevOps suite is available
-     Quick overviews of available services.
- Quick show of services in console, kick off pipeline.
- Diagram of how services link together?
-     Same as what will be displayed in the demo
-     Try show it is easy to use & setup.
- Back to demo for result.
- Show how its implemented in AWS using the services, make it look easy
-     Live Demo? 
-     Pipeline Samples? Buildspec?
-     IaC for pipeline setup?
- Questions