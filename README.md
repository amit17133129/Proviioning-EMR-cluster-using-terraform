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

