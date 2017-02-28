---
layout: post
title:  "AWS"
subtitle: "Solution Design"
date: 2017-02-12 01:00:00
categories: [tech]
---


Demistifying Amazon Web Services

<!--
Solutions Architect - Exam Blue Print

Objectives
 - Designing highly avaliable, cost efficient, fault tolerant, scaleable systems.
 - Implementing/Deploying
 - Data Security
 - Troubleshooting

Exam Brief
 80 Minutes
 60 Questions
 MCQ
 Aim for 75%
 Qualification is valid for 2 years
 Senario based questions. -->



- 10,000 Foot Overview of AWS Platform
  - Game Development, Aritficial Intellegence, **Messaging**
  - Business Productivity, Internet of Things, **Desktop & App Streaming**
  - Application Services, Developer Tools, Mobile Services
  - Analytics, **Security & Identity**, **Management Tools**
  - Migration, **Storage**, **Databases**
  - **Networking & Content Delivery**, **Compute**
  - **AWS Global Infrastructure**

Let's take a look at what is coverd in some of these services

- **AWS Global Infrastructure**
  - Regions
    - Geographical area
    - Region has 2 or more availability zones
  - Avalibility Zones
    - Is a data center, are often seprated/seprated from other availibility zones
  - Edge Locations
    - CDN endpoints for cloudfront
    - For caching

- **Networking & Content Delivery**
  - VPC
    - Virtual Private Cloud
    - Virtual data center
  - Route 53
    - DNS service
  - Cloud Front
    - Part of Content delivery network
    - For large media files
  - Direct Connect
    - Connecting physical datacenters directly with aws

- **Compute**
  - EC2
    - Virtial machines
  - ECS - EC2 Container service
    - Docekr container services
  - Elastic Beanstalk
    -
  - Lambda
    - Serverless
  - Lightsail
    - Out of the box cloud.

- **Storage**
  - S3
    - Object based storage
  - Glacier
    - File archival
    - Extremely lowcost.
  - EFS
    - Elastic file service
    - Block based and volume can be shared
  - Storage Gateway

- **Databases**
  - RDS
    - Relational database
    - MySQL
    - PostgreSQL
    - Aurora
  - DynomoDB
    - Non relational database
  - Redshift
    - Datwarehousing
  - Elasticache
    - Caching service
    - Memcache
    - Redis

- **Migration**
  - Snowball
    - Snowball edge
  - DMS
    - Database migration services
  - Server Migration Service (SMS)
    - Replicate virtual machines

- **Analytics**
  - Athena
    - SQL queries on csv files
  - EMS
    - Elastic Map Reduce
    - Process large amount of data
  - Cloud Search
  - Elastic Search
  - KInesis
    - Stream and analyze TB of data realtime
  - Data Pipeline
  - Quick Sight
    - Business Analysis tools

- **Security & Identity**
  - IAM
    - Fundamental componet
    - Identity and access management
  - Inspector
    - Inspects virtual machines and reports problems
  - Directory Service
  - WAF
    - Application level protection
  - Artifacts
    - Documentation related to ISO certification

- **Management Tools**
  - Cloud Watch
    - Monitor infrastructure
  - Cloud Formation
    - Infrastructure into code
  - Cloud Trail
    - Auditing
  - Opsworks
    - Autmate deployment using chef
  - Config
    - Auditing
    - Config management, set alerts
  - Trusted Advisor
    - Gives tips on optimization

- **Application services**
  - Step Functions
  - SWF
    - Simple workflow framework
  - API Gateway
    - Maintain APIs
  - AppStream
    - Streaming desktop apps to users
  - Elastic Tanscoder
    - Transcode vides to different formats

- **Developer Tools**
  - CodeCommit
  - CodeBuild
  - CodeDeploy
  - CodePipeline

- **Mobile Services**
  - Mobile Hub
    - Backend for mobile app developer
  - Cognito
    - Signup / Signin to apps
  - Device Farm
    - Testing app in 100s of real physical devices
  - Mobile Analytics
    - Collect and analyze mobile data
  - Pinpoint
    - Like google analytics for mobile apps

- **Business Productivity**
  - WorkDocs
  - WorkMails

- **iOT**
- **WorkSpaces**
  - Desktop & App Streaming
  - AppStream 2.0

- **Artificial Intelligence**
  - Book by nick
  - Alexa
    - Voice service in cloud
  - Lex
  - Polly
    - Text to speech
  - Machine Learning
    - Give datasets and outcome - analyze
  - Rekognition
    - Tell you what is there in picture.

- **Messaging**
  - SNS
    - Notification service
  - SQS
    - Simple queue service
  - SES
    - Simple email service