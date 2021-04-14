## The AWS Developer Challenge for Data Engineers
### Instructions

In general feel free to expand/change the challenge in any way you like, just explain your solution and decision making, any concerns around it or limitations etc.

Some information/content is left out intentionally to validate your working experience, please fill in the missing parts.

> Fork this repo with your solution. Ideally, we'd like to see your progression through commits, and don't forget to update the README.md to explain your thought process.

**Please do not reference any websites or published articles. We are looking for original content!**

Please let us know how long the challenge took you. We're not looking for how fast or detailed you are. It's just to give us a clearer idea of what you've produced in the time you decided to take. Feel free to go as big or as small as you want.

### AWS Data Engineer | Challenge Information

This company is ingesting data into a 'data lake' running AWS. Below find a picture of the AWS components used for this company's architecture. 

![AWS-COMPONENTS](/media/awscp.png)

## Section A
### Design an Architecture Diagram - We want to see a picture.
Use the components shown above and create an architecture with your tool of choice (powerpoint / draw.io / etc) showing how to ingest data from an on-premise site into AWS. 

Upload the diagram/picture into the Git repository and indicate where it's saved. Use the given components as far as possible to illustrate your solution.

##### Hints
* Focus on *low cost & high* performance.
* All the data are stored in S3 buckets.
* Athena is used to query the data.
* Show how you will use Step Functions to orchestrate the *ingest* process.
* AWS DynamoDB / CloudWatch must be used.
* Glue Jobs should be used to do the ingest.
* CloudFormation output is a CodeBuild Project
* Git is used to save the terraforms and python / pyspark code.
* You do not have to design/depict the CI/CD, assume that it's already in place.
* Look at the available .tf files to get an understanding of the architecture.
___

## Section B
### Describe the Section A - Architecture Diagram 

Within this Readme.md describe the architecture above, giving detail when and how you would use the selected components.

**Please do not reference any websites or published articles.** 
**We are looking for original content!** 
**We do not want to see definitions of the AWS components.**
**
describe the architecture:
Availability:

Using dual zone deployment, the high availability is achieved at all the layers.
MySQL DB configured in sync mode will keep the data highly available.
Load balancers are used to distribute the load in both the zones.
Auto scaling, configured, would handle the high load situation for the application.

Security:

Various firewall layers have been replaced by security groups and providing the same features of security.
All the app servers and web servers were kept as hardened templates and can be used to create more instances if need be.

Cross cutting concerns:

Logs can be redirected to S3 and further old logs can be moved to Glacier.
Cloud Watch can be used for monitoring and alerting in case of any incident.

We can utilize amazing features of cloud like multi zone deployment, unlimited and various cheaper mode of storage, auto scaling, RDS, security groups and by using same, we can get a little better version of deployment in cloud compared to on prem deployment.


##### Hints
* Consider aspects like security (iam / firewalls / vpc / security groups / roles)
* To each component used, give a detailed description on how it fits into the solution, please do not reference existing AWS documentation, use your own words! Feel free to document your thought process. We are interested to find out how you think.
___

## Section C
**Try your best do not keep the section open, we want to see how you apply yourself**

Within the Git Repository Structure:
* Modify the CloudFormation Template [CFN/seed.yaml] in order to create a CodeBuild Project.
* Update the _glue_jobs.tf_, _main.tf_ and _output.tf_ terraform files. 
* Provide the python script that will be used within the glue job, using either python shell or spark, think here about using DynamoDB to keep certain job settings and table structures for S3.
___

## Submit it

Please use a private repo just email us when you are done. 

## Your Solution Starts HERE!!!
Use this area to describe your solution as requested in *_Section B_*. 


## Additional Comments / Information / Concerns
Add info here.
