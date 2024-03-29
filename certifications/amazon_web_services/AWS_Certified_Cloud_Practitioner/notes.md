# Ultimate AWS Certified Cloud Practiotiner - Udemy
### Stephaen Mareek

---
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
		
## Section 11 Deployment and Managing Infrastructure at scale

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
	
	Route 53
		Global Domain
			Buying a domain name 
	
	Cloud Front
		Content Delivery Network
			S3 buckets
			Http websites
	
	Global Accelerator
		Does not cache, Simply acts as a proxy between edge network and the actual server

## Section 13 : Cloud integrations
	
	SQS
		Simple Queue Service
			Send messages and Consumers can poll for messages
				Can Retain messages up to 14days
			To Decouple the application
			
	SNS
		Simple Notification Service
			Consumers Subscribes to a topic, and Publisher can send one notification which is pushed to all the subscribers
	
## Section 14: Cloud Monitoring

	Cloud Watch Metrics
		Billing Metrics (only in us-east-1)
	
	Cloud Watch Alarm
		Trigger notifications on a metric
	
	Cloud Watch Logs
		Cloud watch log agent can be installed on ec2 or on premise servers
		Real-time monitoring of logs
	
	Cloud Watch Events
		Schedule CRON Job
		Event pattern
			If a ec2 instance is terminated
	
	Event Bridge
		Logs What happened
		Same as Cloud Watch Events, but New version
	
	Cloud Trail
		Who did a thing
		Provides governance, compliance and audit
		Enabled by default
	
	X-Ray
		Visual Analysis of Application
		There are lot of services involved in an application, monitoring it with event bridge is difficult, Therefore use X-Ray
	
	Service Health Dashboard 
		status.aws.amazon.com
		To check whether a service works correctly
	
	Personal Health Dashboard
		phd.aws.amazon.com
		Only show the health of services that we use
		

## Section 15 : VPC & Networking
	
	Refer slides or videos
	
	NACL 
		Network Access Control List
			Has Allow and Deny Rules
			Attached to subnets
			Only IP address
	
	Security Group
		Only Allow Rules
		Can be IP or other security groups
	
	VPC Endpoint
		To connect to AWS service using private internet
		
		VPC Endpoint Gateway 
			S3 and DynamoDB
		VPC Endpoint interface
			All other AWS Services
	
	Site-to-Site VPN
		Connect On-Premise VPN to AWS
		Connected through public internet
	
	Direct Connect (DX)
		Physical connection between on-premise and AWS
		Private Network
		
		Customer has CGW (Customer Gate Way)
		Aws has : VPW (Virtual Private Gateway)
		
	Trasnsit Gateway
		To Perring between VPC's , because VPC peering is transitive (A - B - C means A cannot talk with C )

## Section 16: Security and Compliance
		
		DDOS Protection in AWS
			
			AWS Shield Standard
				Free service
					
			AWS Shield Advanced
			
			WAF
				Web Application Firewall
				Filter Incoming request based on rules
				
				AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources.
				
			Cloud Front and Route 53
			
			
			
		AWS KMS
			Key Management Service
			AWS manages software for encryption
			
			Customer managed CMK - Customer Managed Keys
			
			AWS Managed CMK 
			
			
				
		Cloud HSM
			AWS provisions encryption hardware
		
		AWS Secrets Manager
			
			Can integrate with RDS
			Can automatically rotate key in x days
			
		AWS Artifact
			On-demand access to AWS Compliance documents and AWS agreements, such as PCI, ISO etc ..
	
		AWS Guard Duty
			Intelligent threat discovery mechanism using machine learning 
			Protects VPC DNS and Cloud Trail Logs
			Continuously monitors
			
		AWS Inspector
			Automated security assessment for ec2 instances
			Inspector agent is installed on ec2instance
		
		AWS Config
			Helps with auditing and recording compliance of AWS account
			
		AWS Macie
			Fully managed data security and data privacy service that uses machine learning to protect sensitive data 
				Sensitive data - PII - Personal Identifiable Information
			
			
## Section 17: Machine Learning
	
	AWS Rekognition
		Find objects, people, text, scenes in images and videos using ML • 
		Facial analysis and facial search to do user verification, people counting •
		 Create a database of “familiar faces” or compare against celebrities
	
	AWS Transcribe
		To convert speech into text
	
	AWS Polly
		Text to speech
	
	Amazon Translate
		Translate from one language to another
		
	Lex + Connect
		Lex
			Powers Alexa
			ASR - Automatic Speech Recognition
			Can build chatbots
		
		Connect
			Virtual Contact Center
			Receive phone calls , create contact flows etc.
			Connects with existing CRM Customer Relationship Management Services
			
	Amazon Comprehend
		Natural Language Processing
	
	Amazon SageMaker
		Managed service for data scientists to build ML Models
		Can be used to Label, train , and Deploy model
		
## Section 18: Account Management, Billing and Support 
	
	AWS Organizations
		To manage multiple accounts
			Aggregated usage - therefore discounts from large usage
		SCP can be implemented to limit resources
		
	Pricing Models in AWS
		4 Pricing models
		aws.com/free
	============
	
	Estimating Cost in cloud
		TCO Calculator
			Shows how much we save on aws vs on-premise
		
		AWS Pricing Calculator
			Shows How much a resource in AWS Costs for the given configurations
	
	Tracking Costs in cloud
			Billing Dashboard
			Cost Allocation Tags
			Cost and Usage Reports
				Delivers to storage service
				Most details
			Cost Explorer
				Dashboard in graphs
				Forecast based on previous usage
			
	Monitor Against Cost plans
		Billing Alarm
			Simple graph showing budget
			Billing data metric stored in us-east-1
			
		AWS Budget
			Can create alerts based on usage or forecast
	
	Trusted Advisor
		Analyze AWS Account and provide suggestions
		
		Core check
			For all customer
		
		Full trusted Advisor
			For Business and Enterprise support
			Also API support is enabled
		
## Section 19: Advanced Identity
	
	IAM
		Identity Access Management
			Within an AWS account
	AWS Organizations
		To manage multiple accounts
		SCP Limiting
		
	Amazon Cognito
		Identity for web and mobile applications
		Has sign in with fb, google, twitter options too
	
	Microsoft Active Directory
		Database of objects
			User account, computer, printers etc ..
	
	AWS Directory Services
	
	AWS Single-Sign-on (SSO)
		To access multiple accounts or 3rd party apps like slack etc.
		
		
## Section 20: AWS Architecting and Ecosystem  -- refresh
	
	Stop Guessing and Start Scaling
	
	Well Architected Framework 5 Pillars 
	 1) Operational Excellence 
	 2) Security 
	 3) Reliability 
	 4) Performance Efficiency 
	 5) Cost Optimization
	
	Operational Excellence
		Perform operations as a code
		Annotate documentation
		Frequent and small changes
		Learn from failures




