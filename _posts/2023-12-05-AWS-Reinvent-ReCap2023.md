# AWS Re:Invent 2023: Navigating the Cloud Frontier

The AWS Re:Invent 2023 conference unfolded as my last travel for the year, drawing an impressive crowd of over 50,000 attendees. (I heard that it could have been closer to 65,000) the walkways and every corner of the Venetian would accept those sorts of numbers. 

## What did i get up to?

This was a busy week, lots of press interviews and I had two breakout sessions and one session on the Veeam booth. When they all become available I will post here. 

My take on this conference every year and continues with this edition, this is the best conference for me to attend and close out the year. 

It is the best because of basically every persona of the community is here to meet and speak with, we have every vendor spanning all technology spaces and by all accounts any cloud and cloud native technology... is the cool technology to be around. 

The first session to plug is where we delved into the intricacies of safeguarding Kubernetes environments. We shed some light on the role of Kasten K10 in securing and scaling data within Kubernetes clusters, offering valuable insights for attendees navigating this critical aspect of modern cloud architectures.

[![Kubernetes Data Management and Scaling with Kasten K10 (CON204)](https://img.youtube.com/vi/6UOXXMd_U6Y/0.jpg)](https://www.youtube.com/watch?v=6UOXXMd_U6Y)

My second session was with Julia. We discussed "Cloud Securitym Data Responsibility and Recovery: 10 Key Strategies" In this session we took the well known 6Rs blog which was updated in 2017 to be the 7Rs and we went through each one and added some hopefully interesting insights on how you should be making your data still recoverable as you as the end user is responsible for this data. 

In brief though we have 

- Retire - We have nothing to do here. 
- Retain - Keep protecting your workloads with Veeam on-premises. 
- Relocate - VWware Cloud on AWS, looks like a VM the same but different 
- Rehosting - Direct Restore to AWS EC2 (Actually can be any source and target image based backup to any cloud)
- Replatforming - Database Server on prem but now moving to PaaS (RDS, DynamoDB, EFS) or moving to managed service or  serverless
- Repurchasing - Offload admin and management to a service provider to look after things or move to SaaS 
- Refactoring - going from VMs / Physical to EKS / Containers 

Whilst the above are pathways to get into the cloud and continue that cloud journey, we also introduced three more Rs that should be top of mind. 

- Responsibility - Your data in the cloud is your responsibility 
- Resilience - Security is top of mind and more topical than ever you must be mindful of cloud configuration 
- Recovery - When it comes to your data you want to make sure that you have backups of this data but equally you want to make sure that you have granular recovery options as well disaster recovery plans that can be carried out when needed. 

## Generative AI Takes Center Stage

AWS Re:Invent was always going to have a huge focus on AI and LLMs because every other conference in the last 9 months has had to, as generative AI stole the spotlight. Amazon Bedrock and Amazon Q emerged as powerful players, introducing a new breed of generative AI-powered assistants. Notably, the intriguing Party Rock, a Bedrock playground, beckoned attendees to explore the capabilities of this novel AI paradigm hands-on.

## Diving into Databases

As someone who is focused on data, the areas to find out more for me at these events is going to be around databases and data services. 

The conference witnessed a robust exploration of database advancements. From the dynamic scalability of ElastiCache Serverless to the automated horizontal scaling of Aurora Limitless Database, attendees were introduced to solutions capable of handling millions of transactions per second. Notable mentions include IBM DB2 on RDS (Version 11.5) and the much-requested RedShift Serverless, a cloud data warehouse dynamically adapting to workload patterns and data complexity.

Vectors Everywhere! was the mantra, with offerings like DocumentDB and OpenSearch Serverless catering to diverse database needs. For data scientists, Neptune Analytics emerged as a dedicated analytics database, specializing in large-scale graph data analysis.

## Unveiling Cost Optimization Strategies

A critical aspect of cloud management, Cost Optimization took center stage with the introduction of the Cost Optimization Hub. This hub consolidates optimization recommendations across member accounts and regions, providing a centralized approach to managing costs effectively.

In conclusion, AWS Re:Invent 2023 proved to be a melting pot of Artificial Intelligence news or noise. I think on the other hand we are seeing AWS settle down a little in regardds to the massive amounts of services announced during the event. Do not get me wrong there are still plenty to get lost in for the next 12 months but are things consolidating a little... or could they be listening to customers. 

I was amazed to see a flurry of new companies representing AI as their new famed glory or existing big vendors cramming AI into their slogans. 

Meanwhile we stuck to our swimline and discussed data backup, recovery, freedom and security. 
