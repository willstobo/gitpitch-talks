[comment]: <> (https://gitpitch.com/willstobo/gitpitch-talks/master?p=devops-on-aws)
## Enabling DevOps with Amazon Web Services
---
### Key takeaways
- @size[32px](DevOps / Continous Integration / Continous Delivery)
- @size[32px](AWS DevOps Services)
- @size[32px](Implementing DevOps on AWS)
---

### What is DevOps?
-  @size[32px](Combination of practices and tools, enabling an organisation to deliver applications and services at high velocity.)
-  @size[32px](The ability to more comfortably and quickly deploy software and infrastructure resources than traditional practices.)
+++

### Why use DevOps?
@ul
- @size[32px](Remaining competitive. )
- @size[32px](Evolving security & performance requirements. )
- @size[32px](Maintain stability, increase velocity. )
@ulend
Note:
- 1. Rapidly changing environment, companies are releasing faster then before by using modern software development practices. If you dont adapt, you will fall behind.
- 2. With such a fast pace environment things can change quickly, its important to be able to remain on top of application requirements and security threats as they arise. With a DevOps model, youll be able to react faster and stay on top.
- 3. Enables higher reliability on processes and stability giving confidence to your testing and deployment processes, whilst shortening your release cycles.
+++

###  How do you do DevOps?
@ul
- @size[32px](DevOps isn't one persons job.)
- @size[32px](Large variety of DevOps tools can be used.)
- @size[32px](Implemented via modern software development practices)
@ulend
Note:
- 1. Encourage the entire team to adopt the DevOps culture. Encourage the devs to build frequently. Encourage the testers to build out automation suites and to run them frequently.
- 2. The tools and technologies may change, but the overarching goal remains the same, there is no specific tools to achieve DevOps, it is encouraged to think about and research what tools might be best for the job and to use those.
- 3. Linking to the upcoming CI/CD
+++

### Continous Integration (CI)
@ul
- @size[32px](Practice of regular building, testing and validation of code.)
- @size[32px](Enable & encourage developers to build one to many times a day, pushing out and testing changes as they are finished.)
- @size[32px](Key goals: find bugs, improve software quality and reduce the turn around time of new software updates.)
@ulend
+++

### Continous Delivery (CD)
@ul
- @size[32px](Practice of automatically building, testing and preparing code for production releases.)
- @size[32px](Expands upon CI by deploying all changes to a testing environment.)
- @size[32px](Can be fully automated, or partially automated with manual gates for critical steps.)
- @size[32px](Continous Delivery not Continous Deployment.)
@ulend
+++

### CI / CD
![Source: https://blog.gds-gov.tech/that-ci-cd-thing-principles-implementation-tools-aa8e77f9a350 ](devops-on-aws/devops.png)
@ul
- @size[32px](DevOps never stops!)
@ulend
---

### AWS DevOps Services
![AWS-DevOps-Services](devops-on-aws/aws-devops-services.jpg)

@ul
-  @size[32px](CodeCommit)
-  @size[32px](CodeBuild)
-  @size[32px](CodeDeploy)
-  @size[32px](CodePipeline)
-  @size[32px](CodeArtifact)
@ulend
Note:
- 1. Fully Managed Git based source control service.
- 2. Managed CI Service for Build / Testing
- 3. Deployment Service
- 4. CD Service
- 5. Fully Managed Artifact repository service
+++

### AWS CodeCommit
![AWS-DevOps-Services](devops-on-aws/aws-codecommit.png)
@ul
- @size[32px](Fully Managed secure Git based source control service.)
- @size[32px](Comprehensive access management provided via IAM.)
@ulend
+++

### AWS CodeArtifact
@ul
- @size[32px](Fully Managed Artifact repository service.)
- @size[32px](Supports multiple repository types, e.g NPM/Maven/Python.)
- @size[32px](Allows for private & public hosted repositories.)
@ulend
Note:
- Artifact Storage for applications
- Repos are placed in domains, IAM permissoins can be applied at the domain level.
- Can add NPM repo into CodeArtifact, can then download from NPM Repo in CodeBuild
- Publish NodeJs app
- 1. Login to code artifact repo
- 2. npm set scope to codeartifactory repo
- 3. use npm publish with scope
+++

### AWS CodeBuild
![width=150px](devops-on-aws/aws-codebuild.png)
@ul
- @size[32px](Managed CI service for building & testing.)
- @size[32px](Build steps are run in containers managed by AWS.)
- @size[32px](Execution steps defined via the Buildspec.yaml file.)
- @size[32px](Can store build & test reports for display.)
@ulend
+++?code=devops-on-aws/buildspec.yml&lang=YAML

@snap[north-west span-50]
### Buildspec.yaml                         
@snapend
@snap[north-east span-50]
@[4-12](Installation Steps)
@[13-24](Build & Post Build Steps)
@[26-30](Defining Reporting Artifacts)
@[32-36](Defining Output Artifacts)
@snapend
+++

@snap[north span-60]
### AWS CodeDeploy
@snapend     
@snap[north-east span-40]
![width=150px](devops-on-aws/aws-codedeploy.png)
@snapend
@ul
- @size[32px](AWS deployment service.)
- @size[32px](Capable of deploying to ECS, Lambda, EC2 and on-premise machines.)
- @size[32px](Deployment steps defined via the Appspec.yaml file.)
@ulend
Note:
- 1. Make EC2
- 2. Setup Deployment Group
- 3. Define deployment steps?

+++?code=devops-on-aws/appspec.yml&lang=YAML

@snap[north-west span-50]
### Appspec.yaml                         
@snapend
@snap[north-east span-50]
@[3-5](Determine Artifact output location.)
@[6-8](Define deployment scripts to be executed.)
@snapend
+++

### AWS CodePipeline
![width=150px](devops-on-aws/aws-codepipeline.png)
@ul
- @size[32px](AWS continuous delivery service.)
- @size[32px](Model and visualise deployment steps into pipelines.)
- @size[32px](Supports automatic pipeline triggers.)
@ulend
+++

### CodePipeline Example
![width=150px](devops-on-aws/codepipeline.jpg)
Note:
- Maybe Demo, show pipeline, start pipeline then...
- Show Diagram of what pipelines are doing in the background
- Show pipeline results
- Have already green pipeline as a backup for live failure
---

### Demo
Lets see it all in action!
---

### Recap
- @size[32px](DevOps / Continous Integration / Continous Delivery)
- @size[32px](AWS DevOps Services)
- @size[32px](Implementing DevOps on AWS)
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

Note:
- Title: Enabling DevOps with Amazon Web Services.
- With so many ways to implement 'DevOps', where do you actually start?
- Companies are going to market faster and more robustly with DevOps.
- In this talk we take a look at some modern DevOps practices, the benefits that DevOps can provide and how easily they can be implemented with Amazon Web Services.
- A basic knowledge of Cloud Services is recommended, but not required.
