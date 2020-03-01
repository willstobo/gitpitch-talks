[comment]: <> (https://gitpitch.com/willstobo/gitpitch-talks/master?p=demystifying-cloud)
## Demystifying-Cloud
---
### About me
- 2017 SMS/ASG graduate
- 3 years experience with cloud services
---
### Contents
- On-premise computing
- Cloud computing
- Cloud service models
- Cloud providers
---
### On-premise Computing
Traditional Web Application 
@ul
- Webserver / Proxy server
- Application server
- Database server
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
### Traditional Web Application
@size[12px](What do you do when...)
@ul
- Hardware fails?
- Huge increase in traffic?
- Deploy to another country?
@ulend
Note:
- Hardware failure will cause your applications to go down and if you don't have any spare servers to offer your service, cause an outage.
- When you rely on physical servers, you rely on a team of people to keep these running for you. What happens if you want to deploy your application on the other side of the world? New hardware, more workers, more cost.
- If your traffic suddenly surges beyond your maximum capacity, you can potentially miss out on an increase in business.
- This also increases your inital cost as you need to have servers capable of with standing the peak usage.
+++
### The Downside with On-premise
@ul
- Upfront cost
- Accomodating for maximum load
- Slow provisioning
- Physical security
- High maintanence
@ulend
---
### Cloud Computing
- The on-demand delivery of IT resources via the internet.
- Cloud services come in a variety of models.
Note:
- Cloud computing is the next generation of infrastructure.
- Instead of buying and setting up servers on-premise, simply request on-demand resources from cloud providers over the internet.
- There is a variety of different cloud models that offer different aspects of the cloud.
+++
### Cloud Service Models
![Ref https://dachou.github.io/](demystifying-cloud/cloud-models.png)
Note:
- Here was can see a breakdown of the cloud service models and on-premise.
- As you can see, at each different level we can see the level of responsiblity for the customer changes.
- This can bring simplicity to the services used, but also reduce the control you have.
- Each model has their own benefits and can be used in different situations, based on your needs.
+++
### Infrastructure as a service (IaaS)
- The cloud provider hosts your infrastructure components that would traditionally be present in an on-site data center (such as servers, storage and networking hardware).
- Users maintain control over the operating systems, storage, networking & deployed applications.
- Products: AWS EC2, Rackspace, Google Compute Engine
+++
### Benefits of the IaaS
@ul
- On-demand compute resources
- Pay-as-you-go, no capital expenses
- Shared responsibility
- Most flexible cloud model
- Complete, scalable control of infrastructure
@ulend
+++
### Platform as a service (PaaS)
- Provides a managed platform to develop and run applications
- Eliminates need to install software or hardware, allowing the user to focus on the application.
- Products: AWS Elastic Beanstalk, Heroku, Windows Azure
Note:
- Some exmaples of PaaS AWS Elastic Beanstalk, Heroku, Windows Azure
+++
### Benefits of the PaaS
@ul
- On-demand application hosting
- Pay-as-you-go
- Reduced responsibiltiy
- Rapid Time-to-market
@ulend
+++
### Software as a Service (SaaS)
- Provider sells an application as a service
- Fully hosted and managed by the provider
- Immediate access to full application services
- Products: Salesforce, Slack, Dropbox, Uber, Pega
Note:
- Some exmaples of SaaS systems, 
+++
### Benefits of the SaaS
@ul
- On-demand applications
- Pay-per-user or Pay-per-license
- Accessible anywhere
@ulend
+++
### Serverless
- Cloud provider manages and orchastrates the execution of your application code to serve requests
- Consumers are only billed for the duration of code execution
- Products AWS Lambda, Azure Functions, Cloud Functions
Note:
- Serverless computing is a cloud computing code execution model in which the cloud provider fully manages starting and stopping virtual machines as necessary to serve requests
- Consumers billed by an abstract measure of the resources required to satisfy the request, rather than per virtual machine, per hour
+++
### Benefits of the Serverless
@ul
- Significantly cheaper
- Pay-as-you-go, billed by millisecond
- Only focus on the code
@ulend
---
## Cloud Service Providers
@ul
- Amazon Web Services
- Microsoft Azure
- Google Cloud Platform
@ulend
+++
## Cloud Service Providers Services
![Ref https://www.cloudhealthtech.com/](demystifying-cloud/cloudvscloud.png)
---
# Questions?

