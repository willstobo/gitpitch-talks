[comment]: <> (https://gitpitch.com/willstobo/gitpitch-talks/master?p=devops-on-aws)
## Enabling DevOps 
### with 
## @color[#FF9900](Amazon Web Services)
---
### Key takeaways
- @size[32px](DevOps / Continous Integration / Continous Delivery)
- @size[32px](AWS DevOps Services)
- @size[32px](Implementing DevOps on AWS)
---

### What is DevOps?
@ul
-  @size[32px](Combination of practices and tools, enabling an organisation to deliver applications and services at high velocity.)
-  @size[32px](The ability to more comfortably and quickly deploy software and infrastructure resources than traditional practices.)
@ulend
+++

### Why use DevOps?
@ul
- @size[32px](To remain competitive. )
- @size[32px](Managing evolving security & performance requirements. )
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
![AWS DevOps Services](devops-on-aws/aws-devops-services.jpg)
Note:
- 1. Fully Managed Git based source control service.
- 2. Fully Managed Artifact repository service
- 3. Managed CI Service for Build / Testing
- 4. Deployment Service
- 5. CD Service
+++

### AWS CodeCommit
![width=150px](devops-on-aws/aws-codecommit.png)
@ul
- @size[32px](Fully Managed secure Git based source control service.)
- @size[32px](Comprehensive access management provided via IAM.)
- @size[32px](Centralised location for code storage with version control.)
@ulend
+++

### AWS CodeArtifact
![width=150px](devops-on-aws/aws-codeart-sub.png)
@ul
- @size[32px](Fully Managed Artifact repository service.)
- @size[32px](Supports multiple repository types, e.g NPM/Maven/Python.)
- @size[32px](Allows access to both public & privately hosted repositories.)
- @size[32px](Centralised location for dependency storage.)
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
- @size[32px](Managed CI service for building & testing application code.)
- @size[32px](Build steps are run in containers managed by AWS.)
- @size[32px](Execution steps defined via the 'Buildspec.yaml' file.)
- @size[32px](Build & test reports can be automatically consumed for display.)
@ulend
+++?code=devops-on-aws/buildspec.yml&lang=YAML

@snap[north-west span-50]
### Buildspec.yaml                         
@snapend
@snap[north-east span-50]
@[4-12](&nbsp; Installation Steps)
@[13-24](&nbsp; Build & Post Build Steps)
@[26-30](&nbsp; Defining Reporting Artifacts)
@[32-36](&nbsp; Defining Output Artifacts)
@snapend
+++

## AWS CodeDeploy 
![width=150px](devops-on-aws/aws-codedeploy.png)]
@ul
- @size[32px](Managed application deployment service.)
- @size[32px](Capable of deploying to both cloud & on-premise infrastructure.)
- @size[32px](Deployment steps defined via the 'Appspec.yaml' file.)
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
- @size[32px](Managed continuous delivery service.)
- @size[32px](Automates the build, test & deploy steps into reusable pipelines.)
- @size[32px](Capable of integrating with third-party services.)
@ulend
+++

### CodePipeline Example
![AWS Pipeline](devops-on-aws/codepipeline.jpg)
Note:
- Show Pipeline
- Show App
- Show pipeline in progress, cover codebuild/codedeploy
- Show changed app.
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
