# Veeam in the Cloud 

This week Veeam have made another major release to their Veeam Data Platform. A minor release in 12.1. It is packed with a lot of new features and functionalities specifically related to security and cyber resilience. 

These new features can be found on the [Veeam blog](https://www.veeam.com/blog/radical-resilience-with-veeam.html)

But in this post, I want to talk about the Cool Technologies, I mean Cloud Technologies focus that I have in my role here. I will also save another blog for the Kubernetes focused release as well as 6.5 which landed a few weeks ago also brings some impressive new features to the landscape. 

In this post I will focus on the three hyperscaler clouds and the key features now available in each within the Veeam Data Platform. 

Before we get into each cloud and the new capabilities, we should also mention a wider new massive feature that landed within the Veeam Data Platform, this is the ability to protect Object Storage buckets and blobs. Over the last few years, we have seen an increase of the industry use Object Storage for first class production use cases, this could be from storing Content Delivery Network content to storing large scale streaming data such as video footage. This capability allows us to back up to and from Object Storage locations, whilst also I feel an opportunity to migrate your object storage data to a new location. 

This new functionality looks remarkably similar to the NAS backup functionality released a few versions ago. 

![](https://helpcenter.veeam.com/docs/backup/vsphere/images/nas_components.png)

## AWS Backup & Recovery (7.0)

[Veeam Data Platform - AWS Backup & Recovery](https://www.veeam.com/aws-backup.html?ad=workloads)

AWS is the most mature offering when it comes to Veeam capabilities in the clouds, simply because this was the first cloud that we started with regarding protection. With the ability to protect VPC configurations, EC2, RDS, EFS services up until this latest release. 

As we investigate this latest release Veeam continues to enhance the services that can and should be protected. 

### Immutable RDS Backups 

As mentioned, Veeam has had the ability to protect Amazon RDS for a number of releases now, but this release allows for the ability to offload those backups to S3, not only S3 but to an immutable S3 bucket location. 

### Amazon DynamoDB Backup 

Veeam have added the ability to protect DynamoDB tables, the backups are then stored in a specified backup vault in the same AWS region. Although if you wish to have a copy in a different location then this is possible to change in the backup policy. 

## Azure Backup & Recovery (6.0)

[Veeam Data Platform - Azure Backup & Recovery](https://www.veeam.com/backup-azure.html?ad=workloads)

### Azure Virtual Network Backup 

I may get fired for saying this is like the capability we have within AWS where we can protect the VPC, but the Azure Virtual Network ... 

With Azure the configuration is captured through and API and saves this data to the configuration database. This can capture each of the Azure tenant and subscription. 

This backup includes configuration types for 

- Network peering 
- Network interface
- Virtual network 
- Subnet 
- Public IP address 
- Security Group 

## Google Backup & Recovery (5)

[Veeam Data Platform - Google Backup & Recovery](https://www.veeam.com/google-cloud-backup.html?ad=workloads)

### Google Cloud Spanner Backup 

Before we get into what Veeam does here, not will have heard of Cloud Spanner. 

Cloud Spanner is a managed, horizontally scalable, and globally distributed relational database service from Google. A fully managed service from Google which is highly-available and scalable.  

Cloud Spanner is a relational database that supports SQL queries and provides ACID transactions, foreign keys, and SQL compatible schemas. 

Veeam uses native Google Cloud capabilities to protect these instances without requiring an agent inside the instances. Veeam will create a cloud-native snapshot of each database within the instance. From this snapshot it is possible to send to an archive repository. 

### Enhanced File-Level Recovery 

Veeam have had this capability across existing versions for AWS and Azure. File-Level recovery ensures you are only restoring the data that you need, meaning that our restore process can be extremely fast. 

Think of the below like a shopping list, you can select the files you wish to restore and then download. 

![](https://helpcenter.veeam.com/docs/vbgc/guide/images/item_restore_download.png)

Lots of great new features in this major release, I am looking forward to creating some more in-depth walkthroughs both blogs and video content. 

