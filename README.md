# Proviioning-EMR-cluster-using-terraform

## What is Amazon EMR?
Amazon EMR (previously called Amazon Elastic MapReduce) is a managed cluster platform that simplifies running big data frameworks, such as Apache Hadoop and Apache Spark, on AWS to process and analyze vast amounts of data. Using these frameworks and related open-source projects, you can process data for analytics purposes and business intelligence workloads. Amazon EMR also lets you transform and move large amounts of data into and out of other AWS data stores and databases, such as Amazon Simple Storage Service (Amazon S3) and Amazon DynamoDB.


## Benefits of using Amazon EMR
- Cost savings
- AWS integration
- Deployment
- Scalability and flexibility
- Reliability
- Security
- Monitoring
- Management interfaces

## Why Do Developers Use AWS EMR?
EMR is based on Apache Hadoop. MapReduce allows developers to process massive amounts of unstructured data in parallel across a distributed cluster of processors or stand-alone computers. The ‘elastic’ in EMR means it has a dynamic and on-demand resizing capability, allowing it scale resources up and down quickly depending on the demand.

## Configuring EMR Cluster on AWS using terraform
The figure alongside will helps you to give the tree representation of the folders and modules of terraform code.

The aws terraform code is included in module format. You will find four modules.
1. Create Bucket → Creating s3 bucket
2. emr → Creating emr cluster
3. iam → Creating uers and policies
4. Security → Creating security groups.

First we will use aws provider so that terraform can go to aws to provision the resources. Blow you find the architecture of the code. I have created Create Bucket, emr, iam, Security modules which will helps you to launch the resources over aws.


<p align="center">
  <img width="700" height="600" src="https://miro.medium.com/max/617/1*CBSJ4jK2BecAnnRwWfHECA.png">
</p> 

First we will use aws provider so that terraform can go to aws to provision the resources. Blow you find the architecture of the code. I have created Create Bucket, emr, iam, Security modules which will helps you to launch the resources over aws.

<p align="center">
  <img width="1000" height="1400" src="https://miro.medium.com/max/712/1*9x5oevHfgSJ2WB6GByaKhQ.png">
</p> 

Creating Bucket: This module will helps us to create the bucket. Here, i will be creating only one bucket. This bucket will be used by emr users to put the data and retrieve the data after each job run in emr cluster.

<p align="center">
  <img width="800" height="400" src="https://miro.medium.com/max/475/1*XQgGMNhXO-trOUEBf4HYIw.png">
</p> 

Below code will helps you to launch an emr cluster on aws. Here i am launching 1 master and 1 core node.

<p align="center">
  <img width="1000" height="16000" src="https://miro.medium.com/max/712/1*2mDytl4D3JPEWM89uTz8Dw.png">
</p> 

iam: This module will helps us to create an iam users as well as the respective policy of fetching the data from buckets as well as emr resource. Below is the code of iam module is mentioned.

<p align="center">
  <img width="1000" height="35000" src="https://miro.medium.com/max/933/1*7wzmNFX6Jr4NBp4ZjSd6xQ.png">
</p> 

Security_Group: This module will helps us to create security rules for respective services needed by emr.

<p align="center">
  <img width="1000" height="16000" src="https://miro.medium.com/max/933/1*UFXNqUdXEgWOMjSslAmsLg.png">
</p> 

Terraform apply:
<p align="center">
  <img width="1000" height="400" src="https://miro.medium.com/max/933/1*4d0ztGU20IyKLtLwkggK4A.png">
</p> 

<p align="center">
  <img width="1000" height="400" src="https://miro.medium.com/max/933/1*4d0ztGU20IyKLtLwkggK4A.png">
</p> 
