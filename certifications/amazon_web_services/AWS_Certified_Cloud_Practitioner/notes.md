# Ultimate AWS Certified Cloud Practiotiner - Udemy
### Stephaen Mareek


## Section 4 : Identity Access Management

IAM 

	IAM Roles are like Users, but to grant permission for an aws service
	
	IAM Credentials Report and IAM Access Advisor

## Section 5 : EC2
    Take a loot at what the letter t2 c2 and all means --?
    How to switch between 
        Ec2 ondemand, ec2 reserved instance --?
    AMI  - Amazon Machine Image

## Section 6: EC2 Instance Storage

    EBS is similar to network pendrive
    Can attach to only one instance 
    An instance can have multiple ebs attached
    Locked to AZ's like us-east-1a
        To transfer from one AZ to another, take a snapshot and transfer
            While creating a volume from snapshot, specify the new AZ
        Can even transfer across region
    EC2 Instance Store 
        Like Physical Hard disk
            Ephemeral storage
                If instance is stopped, data will be lost, not for long term storage
        Has very high performance

## Section 7 : ELB and Auto Scaling

Vertical Scaling
	Increasing the instance size
		T2.micro to t2.large

Horizontal Scalability
	Increase the number of instance

High Availability
	Running Application in at least two AZ

Elasticity
	Ability to scale up and down based on demand
Agility
	Create and destroy instances when needed

## Section 8 : S3 Storage
	
	There are no folders in S3, Just a single bucket and folders are just file names but  with slashes
		If so , can we create a empty directory --?
			They are not folders, They are objects
	
	When versioning is enabled, and an object is deleted, it just adds delete marker making the file inaccessible, delete the delete marker to retain the object
	
	Switch between Storage class in Additional Upload Options
		Standard, Glacier, One zone IA etc .. Slide 124 --!
			
	Hybrid Storage can be enabled with
		AWS Storage gateway
			Types of Storage Gateway: • File Gateway • Volume Gateway • Tape Gatewayy
		
		
## Section 9 : Database and Analytics
	
	RDS
		RDS is similar to EBS, in order to move b/w AZ's a snapshot must be taken and then restored into a different AZ
		Used for OLTP
	
	Amazon Aurora
		PostgreSQL or MySQL based
	
	AWS Elasticache 
		In memory databases - high performance , low latency
		Caches the queries to reduce the strain on repeated queries
		Works combined with RDS
			
		
	DynamoDB
		Fully manage NoSQL Database
		Serverless
		Single digit mow latency
		
	Redshift
		Based on PostgreSQl, not used for OLTP - Online Transaction Processing
		Used for OLAP - Online Analytical Processing (data warehousing)
		Load data once every hour
		Columnar Data
		
	AWS EMR
		Elastic MapReduce
			 to create Hadoop Cluster
		Data processing, big data etc ..
	
	Athena
		Serverless DB with SQL capabilities
		To query data in s3
	
	DMS 
		Database Migration Service
	
	Glue
		ETL - Extract Transform and Load
		Prepare data for analytics
		Serverless
	
	
		
		
## Section 10 : ECS, Lambda , Lightsail , Batch

	ECS
		Elastic Container Service
		User has to run the ec2 instances providing infrastructure for the containers
			Runs Docker containers
	
	Fargate
		Also to run containers
		No need to manage the infrastructure (Serverless)
		
	ECR 
		Elastic Container Registry
		Private Image registry for Docker containers
	
	AWS Batch
		• Fully managed batch processing at any scale 
		• Efficiently run 100,000s of computing batch jobs on AWS 
		• A “batch” job is a job with a start and an end (opposed to continuous) 
		• Batch will dynamically launch EC2 instances or Spot Instances 
		• AWS Batch provisions the right amount of compute / memory 
		• You submit or schedule batch jobs and AWS Batch does the rest! 
		• Batch jobs are defined as Docker images and run on ECS 
		 Helpful for cost optimizations and focusing less on the infrastructure
		
	Amazon Lightsail
		Alternative to ec2, rds, elb etc.
		For people with less cloud experience
		Use case
			Simple web service
			Wordpress, magento etc.
		
## Section  11 Deployment and Managing Infrastructure at scale

	Typical Web app 3 tier Architecture
		
	
	Bean Stalk
		Platform As A Service (PAAS)
			Just choose platform
			Upload Code
				Done
		Creates a cloud formation template and executes it
		It is application focused
		
	AWS Code Deploy
		Deploy application automatically
		Independent from cloud formation or beanstalk
		Works with ec2insances or on-premise servers (Hybrid)
		Allows to upgrade from v1 to v2 in a single interface
		
	Systems Manager (SSM)
		Apply patches on a large scale
		Run a command on all instances
		Can work in any system with SSM Agent installed (Hybrid)
		
	Ops Works
		Basically Chef + puppet
		Similar to SSM but for organizations already using chef and puppet
		Instance configuration is obtained from cookbook repository

## Section 12 : leveraging the AWS Global Infrastructure 
	
	
