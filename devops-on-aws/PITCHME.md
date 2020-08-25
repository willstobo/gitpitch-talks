[comment]: <> (https://gitpitch.com/willstobo/gitpitch-talks/master?p=devops-on-aws)
## Enabling DevOps 
### with 
## @color[#FF9900](Amazon Web Services)
---
### Key takeaways
- @size[30px](DevOps / Continous Integration / Continous Delivery)
- @size[30px](AWS DevOps Services)
- @size[30px](Implementing DevOps on AWS)
---

### What is DevOps?
@ul
-  @size[30px](Combination of practices and tools, enabling an organisation to deliver applications and services at high velocity.)
-  @size[30px](The ability to more comfortably and quickly deploy software and infrastructure resources than traditional practices.)
@ulend
+++

### Why use DevOps?
@ul
- @size[30px](To remain competitive. )
- @size[30px](Managing evolving security & performance requirements. )
- @size[30px](Maintain stability, increase velocity. )
@ulend
Note:
- 1. Rapidly changing environment, companies are releasing faster then before by using modern software development practices. If you dont adapt, you will fall behind.
- 2. With such a fast pace environment things can change quickly, its important to be able to remain on top of application requirements and security threats as they arise. With a DevOps model, youll be able to react faster and stay on top.
- 3. Enables higher reliability on processes and stability giving confidence to your testing and deployment processes, whilst shortening your release cycles.
+++

###  How do you do DevOps?
@ul
- @size[30px](DevOps isn't one persons job.)
- @size[30px](Large variety of DevOps tools can be used, e.g Jenkins, Ansible, Docker)
- @size[30px](Implemented via modern software development practices)
@ulend
Note:
- 1. Encourage the entire team to adopt the DevOps culture. Encourage the devs to build frequently. Encourage the testers to build out automation suites and to run them frequently.
- 2. The tools and technologies may change, but the overarching goal remains the same, there is no specific tools to achieve DevOps, it is encouraged to think about and research what tools might be best for the job and to use those.
- 3. Linking to the upcoming CI/CD
+++

### Continous Integration (CI)
@ul
- @size[30px](Practice of regular building, testing and validation of code.)
- @size[30px](Enable & encourage developers to build one to many times a day, pushing out and testing changes as they are finished.)
- @size[30px](Key goals: find bugs, improve software quality and reduce the turn around time of new software updates.)
@ulend
+++

### Continous Delivery (CD)
@ul
- @size[30px](Practice of automatically building, testing and preparing code for production releases.)
- @size[30px](Expands upon CI by deploying all changes to a testing environment.)
- @size[30px](Typically automated, or partially automated with manual gates for critical steps.)
- @size[30px](Continous Delivery not Continous Deployment.)
@ulend
+++

### CI / CD
![Source: https://blog.gds-gov.tech/that-ci-cd-thing-principles-implementation-tools-aa8e77f9a350 ](devops-on-aws/devops.png)
@ul
- @size[30px](DevOps never stops!)
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
- @size[30px](Fully Managed secure Git based source control service.)
- @size[30px](Comprehensive access management provided via IAM.)
- @size[30px](Centralised location for code storage with version control.)
@ulend
+++

### AWS CodeArtifact
![width=150px](devops-on-aws/aws-codeart-sub.png)
@ul
- @size[30px](Fully Managed Artifact repository service.)
- @size[30px](Supports multiple repository types, e.g NPM/Maven/Python.)
- @size[30px](Allows access to both public & privately hosted repositories.)
- @size[30px](Centralised location for dependency storage.)
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
- @size[30px](Managed CI service for building & testing application code.)
- @size[30px](Build steps are run in containers managed by AWS.)
- @size[30px](Execution steps defined via the 'Buildspec.yaml' file.)
- @size[30px](Build & test reports can be automatically consumed for display.)
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
- @size[30px](Managed application deployment service.)
- @size[30px](Capable of deploying to both cloud & on-premise infrastructure.)
- @size[30px](Deployment steps defined via the 'Appspec.yaml' file.)
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
@[7-8](Before Installation script.)
@[9-10](After Installation script.)
@[11-13]Application Start script.)
@[14-17](Application Validation script.)
@snapend
+++

### AWS CodePipeline
![width=150px](devops-on-aws/aws-codepipeline.png)
@ul
- @size[30px](Managed continuous delivery service.)
- @size[30px](Automates the build, test & deploy steps into reusable pipelines.)
- @size[30px](Capable of integrating with third-party services.)
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
- @size[30px](DevOps / Continous Integration / Continous Delivery)
- @size[30px](AWS DevOps Services)
- @size[30px](Implementing DevOps on AWS)
---
#  @color[#FF9900](Questions?)
