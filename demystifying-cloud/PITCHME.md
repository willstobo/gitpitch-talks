[comment]: <> (https://gitpitch.com/willstobo/gitpitch-talks/master?p=demystifying-cloud)
## Demystifying-Cloud
---
### About me
- @size[32px](2017 SMS/ASG graduate)
- @size[32px](3 years experience with cloud services)
---
### Contents
- @size[32px](On-premise computing)
- @size[32px](Cloud computing)
- @size[32px](Cloud service models)
- @size[32px](Cloud providers)
---
### On-premise Computing
Traditional Web Application 
@ul
- @size[32px](Webserver / Proxy server)
- @size[32px](Application server)
- @size[32px](Database server)
- @size[32px](Networking hardware)
@ulend
Note:
- Before we cover cloud computing, lets take a look at what on-premise infrasturcture would look like.
- On-premise computing is still very much the norm and the shift to cloud is still in progress.
- Lets go with your typical website as an example, youd expect this to be compromised of the following.
- Webserver, App Server, and a database server.
+++
### Traditional Web Application
![Traditional Architecture](demystifying-cloud/on-prem.jpg)
+++
### What happens when...
@ul
- @size[32px](Hardware fails?)
- @size[32px](Huge increase in traffic?)
- @size[32px](Deploy to another country?)
@ulend
Note:
- Hardware failure will cause your applications to go down and if you don't have any spare servers to offer your service, cause an outage.
- When you rely on physical servers, you rely on a team of people to keep these running for you. What happens if you want to deploy your application on the other side of the world? New hardware, more workers, more cost.
- If your traffic suddenly surges beyond your maximum capacity, you can potentially miss out on an increase in business.
- This also increases your inital cost as you need to have servers capable of with standing the peak usage.
+++
### The Downside with On-premise
@ul
- @size[32px](Significant upfront cost.)
- @size[32px](Always accomodating for maximum load.)
- @size[32px](Slow provisioning.)
- @size[32px](Physical security.)
- @size[32px](High maintanence.)
- @size[32px](Takes up physical space.)
@ulend
---
### Cloud Computing
- @size[32px](The on-demand delivery of IT resources via the internet.)
- @size[32px](Cloud services come in a variety of models.)
Note:
- Cloud computing is the next generation of infrastructure.
- Instead of buying and setting up servers on-premise, simply request on-demand resources from cloud providers over the internet.
- There is a variety of different cloud models that offer different aspects of the cloud.
+++
### Cloud Web Application
![Cloud Web App](demystifying-cloud/cloud.jpg)
+++
### Cloud Service Models
![Source: https://dachou.github.io/](demystifying-cloud/cloud-models.png)
Note:
- Here was can see a breakdown of the cloud service models and on-premise.
- As you can see, at each different level we can see the level of responsiblity for the customer changes.
- This can bring simplicity to the services used, but also reduce the control you have.
- Each model has their own benefits and can be used in different situations, based on your needs.
+++
### Infrastructure as a service (IaaS)
- @size[32px](The cloud provider hosts your infrastructure components that would traditionally be present in an on-site data center.)
- @size[32px](Users maintain control over the operating systems, storage, networking & deployed applications.)
- @size[32px](Products: AWS EC2, Rackspace, Google Compute Engine.)
+++
### Benefits of the IaaS
@ul
- @size[32px](On-demand compute resources.)
- @size[32px](Pay-as-you-go, no capital expenses.)
- @size[32px](Reduced responsibility.)
- @size[32px](Most flexible cloud model.)
- @size[32px](Complete, scalable control of infrastructure.)
@ulend
+++
### Platform as a service (PaaS)
- @size[32px](Provides a managed platform to develop and run applications.)
- @size[32px](Eliminates need to install software or hardware, allowing the user to focus on the application.)
- @size[32px](Products: AWS Elastic Beanstalk, Heroku, Windows Azure.)
Note:
- Some exmaples of PaaS AWS Elastic Beanstalk, Heroku, Windows Azure
+++
### Benefits of the PaaS
@ul
- @size[32px](On-demand application hosting.)
- @size[32px](Pay-as-you-go.)
- @size[32px](Further reduced responsibiltiy.)
- @size[32px](Rapid time-to-market.)
@ulend
+++
### Software as a Service (SaaS)
- @size[32px](Provider sells a finished application as a service.)
- @size[32px](Fully hosted and managed by the provider.)
- @size[32px](Immediate access to full application services.)
- @size[32px](Products: Salesforce, Slack, Dropbox, Pega.)
Note:
- Some exmaples of SaaS systems, 
+++
### Benefits of the SaaS
@ul
- @size[32px](On-demand applications.)
- @size[32px](Pay-per-user or Pay-per-license.)
- @size[32px](Accessible anywhere.)
- @size[32px](Scales as required.)
@ulend
+++
### Serverless
- @size[32px](Cloud provider manages and orchestrates the execution of your application code to serve requests.)
- @size[32px](Consumers are only billed for the duration of code execution.)
- @size[32px](Products AWS Lambda, Azure Functions, Cloud Functions.)
Note:
- Serverless computing is a cloud computing code execution model in which the cloud provider fully manages starting and stopping virtual machines as necessary to serve requests
- Consumers billed by an abstract measure of the resources required to satisfy the request, rather than per virtual machine, per hour
+++
### Benefits of the Serverless
@ul
- @size[32px](Significantly cheaper, most cost-effective cloud model.)
- @size[32px](Pay-as-you-go, billed by the millisecond.)
- @size[32px](Only focus on the code.)
- @size[32px](Scalable by default.)
@ulend
---
## Cloud Service Providers
@ul
- @size[32px](Amazon Web Services)
- @size[32px](Microsoft Azure)
- @size[32px](Google Cloud Platform)
@ulend
+++
## Cloud Service Providers Services
![Source: https://www.cloudhealthtech.com/](demystifying-cloud/cloudvscloud.png)
---
# Questions?

