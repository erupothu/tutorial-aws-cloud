Hello  
&emsp; harish

<pre>
<details>
<summary> Monitoring </summary>
  AWS CloudTrail:
    Continuously log your AWS account activity
    Compliance aid, Data exfiltration, Operational issue troubleshooting, Security analysis
</details>

<details>
<summary> Security </summary>
IAM:
  Securely manage access to AWS services and resources per AWS account.
  Access Managements
    Users
    Groups
    Polices
    Roles
    MFA
    CloudShell
  Access Reports
    Security Tools
    IAM Acces Advisor
    Reports
Certificate Manager:
  A service that provides a highly available private CA without the upfront investment and ongoing maintenance costs of operating your own private CA.
Key Management Service(KMS)
  A service that helps you create and manage keys and control the use of encryption across a wide range of AWS services and in your applications.
  Easily create keys and control encryption across AWS and beyond
  Centralized key management, Encryption for all your applications, Built-in auditing, Secure, Compliance
Organizations:
  AWS Organizations is a service that enables you to centrally manage billing, control access, compliance, security and share resources across your AWS accounts.
  Centrally manage and govern your environment as you scale your AWS resources.
  A service that helps you to provision, manage, and deploy public and private SSL/TLS certificates for use with AWS services and your internal connected resources.
Security Hub
  Manage your compliance and security.
Amazon GuardDuty
  Threat detection and continuous monitoring of your AWS Accounts.
  Intelligent threat protection for accounts and workloads
  Analyze VPC Flow logs, AWS CloudTrail management event logs, DNS query logs, AWS CloudTrail S3 data event logs, and Kubernetes (EKS) audit logs to generate security findings.
  Protect your compute workloads
    Detect when your EC2 instance are used to mine cryptocurrency or communicate with IP addresses and domains associated with known malicious actors.
  Protect your AWS credential
    Detect when your AWS credentials are used in a suspicious way, such as from IP addresses associated with known malicious actors, or in an a way that deviates from their expected behavior.
  Protect your data stored in Amazon S3 buckets
    Detect when data stored in your Amazon S3 buckets is accessed in a highly suspicious manner, such as when an unusual volume of objects are retrieved form an unusual location
Amazon Inspector:
  automated and continual vulnerability management at scale
  Assess, audit, and evaluate the configurations of your AWS resources.
  Automated and continual vulnerability management at scale
Amazon Macie
  Macie helps you discover and analyze sensitive data in S3 at scale, including personal identifiable information (PII) such as names, addresses, and credit card numbers.
  Continually strengthen your data security posture
  Discover sensitive data across your Amazon S3 environment to enable visibility and automated remediation of data security risks.
  Discover sensitive data for compliance
    Schedule data analysis on a one-time, daily, weekly, or monthly basis to ensure sensitive data is discovered and protected.
  Detect and protect sensitive data during migration to AWS
    Use Macie during data ingestion to determine if sensitive data has been appropriately protected.
  Increase visibility into where your most business-critical data exist in Amazon S3.
    Use Macie to automatically and continually evaluate all your sensitive data stored in S3 buckets.
Amazon Detective
  Investigate potential security issues or suspicious activities
  Analyze, investigate, and quickly identify the root cause of potential security issues or suspicious activities. Amazon Detective is directly integrated with GuardDuty making it easy to kickstart incident investigations when a threat is detected.
AWS Security Hub
  Automate security checks, manage security findings, and identify the highest priority security issues across your AWS environment. If enabled, All GuardDuty findings are automatically sent to AWS Security Hub.
Trusted Advisor:
  Cost optimization, Performance, Security, Fault tolerance, Service limits
AWS Shield:
  Managed DDoS protection service
AWS WAF:
  Protect your web applications from common web exploits Global 
</details>

<details>
<summary> Networking: </summary>
VPC:
  VPC endpoint to access Amazon SQS
  An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between instances in your VPC and the internet
  AWS Site-to-Site VPN (aka VPN Connection) enables you to securely connect your on-premises network or branch office site to your Amazon Virtual Private Cloud (Amazon VPC).
  You can use a network address translation (NAT) instance in a public subnet in your VPC to enable instances in the private subnet to initiate outbound IPv4 traffic to the Internet or other AWS services, but prevent the instances from receiving inbound traffic initiated by someone on the Internet
VPN CloudHub
  If you have multiple AWS Site-to-Site VPN connections, you can provide secure communication between sites using the AWS VPN CloudHub
  This enables your remote sites to communicate with each other, and not just with the VPC.
Network ACLs: 
  A network access control list (ACL) is an optional layer of security for your VPC that acts as a firewall for controlling traffic in and out of one or more subnets
Security group
  A security group acts as a virtual firewall that controls the traffic for one or more instances.)
VPCs: 
  Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined.
Subnets:
  A subnet is a range of IP addresses in your VPC. After creating a VPC, you can add one or more subnets in each Availability Zone.
Route tables: 
  A route table contains a set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed.
Internet gateways: 
  An internet gateway is a horizontally scaled, redundant, and highly available VPC component that enables communication between your VPC and the internet.
Egress only internet gateways: 
  An egress-only internet gateway is for use with IPv6 traffic only. To enable outbound-only internet communication over IPv4, use a NAT gateway instead.
DHCP option sets: 
  The Dynamic Host Configuration Protocol (DHCP) provides a standard for passing configuration information to hosts on a TCP/IP network.
Elastic IP addresses: 
  An Elastic IP address is a static IPv4 address designed for dynamic cloud computing
VPC endpoints: 
  A VPC endpoint enables connections between a virtual private cloud (VPC) and supported services, without requiring that you use an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection. Therefore, your VPC is not exposed to the public internet.
VPC endpoint services: 
  You can create your own application in your VPC and configure it as an AWS PrivateLink-powered service (referred to as an endpoint service). Other AWS principals can create a connection from their VPC to your endpoint service using an interface VPC endpoint or a Gateway Load Balancer endpoint, depending on the type of service
NAT gateways: 
  You can use a network address translation (NAT) gateway to enable instances in a private subnet to connect to services outside your VPC but prevent such external services from initiating a connection with those instances. There are two types of NAT gateways: public and private.
  A public NAT gateway enables instances in private subnets to connect to the internet but prevents them from receiving unsolicited inbound connections from the internet. You should associate an elastic IP address with a public NAT gateway and attach an internet gateway to the VPC containing it.
  A private NAT gateway enables instances in private subnets to connect to other VPCs or your on-premises network but prevents any unsolicited inbound connections from outside your VPC. You can route traffic from the NAT gateway through a transit gateway or a virtual private gateway.
  
</details>

<details>
<summary> Disaster Recovery </summary>
</details>

<details>
<summary> Compute: </summary>
EC2:
  Instances:
    EC2: connect (EC2 connect,session manager, ssh client, EC2 serial console), Roles, EFS or FSx Support within subnet for EFS or FSx /mnt/efs/fs1/
    Spot, Reserved, Dedicated, saving plan, scheduled, capacity reservation
    types: General purpose(M7g,T4g), Memory Optimised(R7g, X2gd), compute optimized (C7g), Storage Optimized(I4g, D3), accelarated Computing(P4, DL1, G5g), HPC Optimized(HPC7g) 
    Free Tier: Time:720hrs, Type:t2micro or t3 micro, EBS: 30GB, IO's: 1milllion, snapshot: 1GB, Bandwidth Internet: 100GB
    Template
  Images:
    AMI
    EC2 image builder (docker image, Amazon image)
  EBS:
    Volumes
    snapshots
    Life cycle manager (Create, delete, retension, copy of snapshots and AMI)
  Network & Security:
    SG
    EIP
    Placement Groups: cluster, partition and spread
    key pairs
    Network Interface:
  LB:
    ALB (HTTP, HTTPS), NLB (TCP, UDP, TLS), GLB (On Pemises)
    Target group: EC2, IP, ALB, Lambda
  ASG: templates, size, policies, notifications
  
ECS (Elastic container service):
  Launch Types: 
    EC2 with ECS agent and Docker
    integrations ECR, Cloud watch logs, S3, Dynamodb
    Roles for each task
  Fargate: serverless, no ec2 instances, not infrastructure
  ALB integration
  NLB for high throughput
  Mount EFS Data volumes for ECS both fargate and EC2
  external EC2 integration
  ASG default
  ECS cluster
  Task Definition (Docker files for build image)
  service for deploying the image
  
ECR:
  Docker registry, Elastic kubernates cluster
  maintain versions
  maintains security and scanns images
  
EKS:
  Public Load balancer
  private master node and worker nodes
  ASG
  uses EC2 or Forage
  need storage class
  container storage interface
  Data Volumes like EBS for EC2 and Fargate for EFS, FSx luster, NetApp ONTAP
  
App Runner:
  Container Registry or Source Repository
  provider ECR or Amazon ECR public
  container image
  instace type and infra
  Autoscaling
  health check
  security
  Networking
  Observability
SQS:
	consumer pull data
	data deleted after consumed
	can have many workers
	Orering guarentied with FIFO

SNS:
	push data to many subscribers
	upto 12,000,000 subscribers
	not persistant (may lose data)
	pub/sub
	upto 100,000 topics
	integrates with SQS

Amazon MQ:
	Managed broker service for Onpremises applications RabbitMQ, ActiveMQ 
	no autoscaling
	run on multi AZ's
	has feature like SQS and SNS
Global Accelerator:
	accelerates traffic based on user accessed regions. ex two ec2 instances ec2A in ap-south-1 ec2B in us-east-1 india user access ap-south-1 
	Fit for Non-HTTP i.e TCP and UDP
	Anycast
	Scale for increased application utilization
	Accelerate latency-sensitive applications
	Disaster recovery for multi-Region & multi-Availability Zone resiliency
	Elastic IP, EC2, ALB, NLB, public or private 
	Security protects from DDOS
Cloud Front:
	fit for HTTP, HTTPS
	Global
	Telemetry
	Reports & Analysis
	Security & Key management
	S3: 
		Create control setting, 
		shield, 
		cache behaviour, 
		restrict viewer acces, 
		cache policy, 
		lambda function association, 
		WAF, 
		SSl Certificate, 
		Invalidate cache
	API Gateway
	LB
	Media Contianer
	MediPackage
</details>

<details>
<summary> Serverless </summary>
Lambda:
  short execution
  autoscaling automated
  multi programming language
  128MB to upto 10GB Ram
  max execution time 15min
  env variable 4KB
  capacity 512MB to 10GB
  concurrent executions 1000
  zip 50MB, uncompressed code + dependencies 250MB
  cloud watch
  
API Gateway:
  Integrates with Lambda, HTTP, Mock, AWS Services, VPC link
  support Web socket
  Api Versioning
  Security Authentication and Authorization
  request throttling
  swagger
  transform and validate api request and response
  cache api response
  SDK
  End point Types:
    Edge Optimized: for global clients
    Regional: same region,  combines cloud front 
    Private: access within VPC
  Security:
  
Step Function:
  integrates SQS, SNS, Lambda, EC2 etc
  create a work flow
  
Cognito:
  Gives users identity to interact with Web and Mobile APplicaitons
  Congito USer pool: sign in functionality for App users
  Congnito Identity Pool: Provide AWS credentials to users
  authenticate with SAML
  serverless database for User login 
  password reset
  Authencation and Authorization Server that provide Token to authenticate with API Gateway
  User pools provide: 
    1. Sign-up and sign-in services. 
    2. A built-in, customizable web UI to sign in users. 
    3. Social sign-in with Facebook, Google, Login with Amazon, and Sign in with Apple, as well as sign-in with SAML identity providers from your user pool. 
    4. User directory management and user profiles. 
    5. Security features such as multi-factor authentication (MFA), checks for compromised credentials, account takeover protection, and phone and email verification. 
    6. Customized workflows and user migration through AWS Lambda triggers.
  Identity Pools - 
    Identity pools provide AWS credentials to grant your users access to other AWS services. 
    To enable users in your user pool to access AWS resources, you can configure an identity pool to exchange user pool tokens for AWS credentials. So, identity pools aren't an authentication mechanism in themselves
Elastic BeanStack:
	end to end web application management
	web server emd
	worker env
	creates ASG
	Creates LB
	Creates EC2 instance
	Cloud formation
EMR:
	Hadoop cluster
	vast amound of Data
	Apache spark, HBase, Pestro, Flink
	Autoscalling
	data processing, machine learning, web indexing, big data
	core node, task nodes
Glue:
	ETL extract, Transform and Load
	s3 to RDS, CSV to PDF etc
	one database to another DB
	glue jobs
	glue databrew
	glue studio
	glue streaming ETL
</details>

<details>
<summary> Sharing: </summary>
EFS:
  NFS (Network file syste)
  supports only Linux (not windows)
  Region or zone
  pay per use Auto storage update
  unlimited client, max PB, elastic throughput
  storage classes:
    standard: frequently accessed
    EFS-IA: life cycle policy
  EC2 location: /mnt/efs/fs1/
  Backup
  Data Sync
  Data Transfer

FSx:
  for NetApp ONTAP 
    aws or onpremises
    accessable from windows, linux, mac
    SMB, NFS, iSCSI protocols,
    multi region replication, 
    3GB/s throughput, 
    IA access,
    1TB to 192TB
    Integrate Microsoft Active Directory (AD)
  for OpenZFS:
    aws or onpremises
    accessable from  windows, linux, mac NFS protocol v3, v4, v4.1, v4.2
    21GB/s throughput
    single AZ's
    64Gb to 512TB
  for Windows:
    aws or onpremises
    accessable from  windows, linux,
    single and Multi Az deploy
    Active Directory Integration
    32Gb to 65TB
  for Luster:
    aws or onpremises
    accessable from Linux over POSIX protocol
    integrates with S3, Sage Maker, EKS, Batch, AWS parallelCluster
    100+/GB/s throughput
    1.2RB and 2.4TB storage support
</details>

<details>
<summary> Databases: </summary>
RDBMS: RDS, Aurora great for joins
NoSql : Dynamodb (JSON), Elasticache(key/value pair) Neptune (Graph), Document DB(MongoDB), Keyspaces(Cassendra)
Object Store: S3
Data warehouse: Redshift, Athena, EMR
Search: OpenSearch(JSON), free text, unstructured searches
Graphs: Neptune
Ledger: Quantom Ledger Database
Time seeries: Amazon Time series
RDS:
  RDS Proxy
  RDS Security
  Aurora MySql:
    5time throughput than MySql
    update 128TB autoscaling
    6way replication accross 3AZ's
    Upto 15 read replicas with 10ms lag
    Automatic Monitor on failore
  Aurora Postgres:
    3time throughput than MySql
    update 128TB autoscaling
    6way replication accross 3AZ's
    Upto 15 read replicas with 10ms lag
    Automatic Monitor on failore
  MySql:
    upto 64TB
    15 read replicas per instance
    point in time recovery
    support general purpose memory optimized
  Postgres:
    high volume environments
    15 read replicas per instance
    point in time recovery
    support general purpose memory optimized
  Oracle:
    deploys in Oracle cloud
  MariaDB:
    upto 64TB
    point in time recovery
    15 read replicas per instance
    support general purpose memory optimized
    Supports global transaction ID (GTID) and thread pooling.
  MS Sql Server
Elasticache:
  Redis cluster: Multi AZ, Read Replicas, High availability, on premises support, SSL connection, 13GB to 2TB storage. 
  memchache cluster:
    
DynamoDB:
  NoSQL,
  distributed DB
  handles millions of request and trillions of rows
  autoscalling
  Multizone deployment
  tables, items(rows),max item size 4KB, 
  scalare type, Document type, Set Type of Data types
  pay on use not fixed storage or ram
  RCU and WCU autoscalling
  Dynamodb Accelerator:
    inmemory cache for DynamoDB
    solve read congesion by cacheing
    contains nodes to call DynamoDB tables
  Dynamodb Stream:	
    Order stream item level modification in table
    react to changes
    real time analytics
    implements cross region replication
    invoke lamdbda on change to DynamoDB
    24 hours retension
    Dynamodb kinesis adapter
    Dynamodb -> Dynamodb Stream -> kinesis Data Stream -> Kinesis Firehose -> (Redshift or S3 or Opensearch)
  Global Table:
    two replication in multiple regions
    active-active replication
    Must enable DynamoDB Stream as pre requisite
  DynamoDB TTL:
    automatically expire items after a while
  backups and point in time recovery
  export backup to s3 will not effect DB performance
  
Document DB:
  Aurora Verions for MongoDB
  store query and index
  Automatic scale to workload with millions of request
Neptune:
  Social network
  Highly connected datasets
  Billions of relations
  Knowledge graphs, fraud detection, social network
  
Keyspaces:
  Cassendra type of service
  serverles
  automatic scale
  Using Cassendra Query language (CQL)
  Encryption, backup, point in time recovery 35 days
  
QLDB(Quantum Ledger Database)
  replicates accross 3 availabilty zones
  once written cannot be modified
  ledger is book of financial transactions
  immutable system no entry can be removed
  ledger block chain framework
Time series:
  Serverless DB
  Automatically scale
  store and analyse trillions of records
  IOT apps, operation applicaitons, real time analytics
  
Redshift:
  OLAP database
  Datawarehouse
  columinar storage data
  serverless, automatically scale data,
  pay as you go
  SQl interface
  BI Tool integration like Quicksight, Tablue
  Redshift Spectrum
  query on S3 without loading it.
  query submitted to 1000s of Redshift spectrum nodes
Lake formation:
	central place to have all data to Analyze
	Discover, cleans, transform ingest, 
	S3, RDS, NoSql, Fine grained Access Controll
	Centralized Access control
	Data lake in S3
</details>

<details>
<summary> Storage </summary>
DataSync:
  Onpremises 
  install Agent
  transfer from Onpremises  DataSync to s3, EFS, FSx
  transfer from (S3, EFS, FSx, HDFS, NFS, SMB) DataSync to (S3, EFS, FSx)
Transfer Family:
  FTP. SFTP, FTPS,AS2
  
Storage Gateway:
  Transfer On-premises data
  disaster recovery
  backup and restore
  (S3 file gateway) - storage gateway device - (s3 storage - Glacier)
  (FSx file gateway) - storage gateway device - (FSx storage - S3 storage)
  volume gateway - storage gateway device - (s3 storage - EBS), 
  tape gateway - storage gateway device - (s3 storage - Glacier Deep archive)
  S3 File Gateway:
    supports s3 All types
    support NFS and SMB
  FSx File Gateway:
    for windows server data transfer
    support Active Directory
    NFS and SMB
  Volume Gateway:
    supoort iSCSI protocol backed by s3
    EBS snapshots
  Tape Gateway:
    physical tapes
    backed by s3 Glacier
  
Snow family:
  import or export to S3, compute and storage only, import tape into storage gateway
  snowcone:
    2CPU, 4GB Ram, 8TB HDD to 14TB SSD
  snowball:
    storage optimized (40CPU, 80GB RAm, 80TB HDD 1 TB SSD), Compute Optimized(52CP, 208RAM, 40TB HDD, 8TB SSD)
  snowmobile:
    PB of Data

S3:
  names are globally unique but bucket is created within a region
  ACL's
  versioning
  Encryption: SSE-KMS, SSE-S3, DSSE-KMS, SSE-C (User upload key + object), client side encryption( user encrypts the file and upload to S3)
  bucket key
  Object lock
  MFA
  max Obj size 5TB
  upload >5GB multipart upload
  presigned url
  cloud trail
  Notificatin
  Transfer Accelarator
  static website hosting
  requester pay
  Bucket policy (statement [{Sid:"UniqueID", Effect: "Allow/Deny", principal: "Account", Action:"GET/PUT/POST/UPDATE", Resources: "bucket path"}]
  CORS
  Performance: 
    3500 PUT/DELET/Create requests per sec
    5500 GET Head request per sec per prefix in bucket
  
  Life Cycle Rule
    Automate rules when to move data to which storage classes
    
  Replication Rule
  storage classes: 
    standard,: multi AZ's, immediate access
    intelligent-IA: multi zone, Automate convert to Infrequent access classes
    standard-IA: multi zone, can access after 30 days min storage duration
    one zone IA: one zone, 30days
    Glacier instant retrival: multizone, min storage 90 days
    Glacier flexible retrival: multizone, 90 days
    Glacier Deep Archival: multi AZ, min storage 180 days
    reduced redendency
</details>

<details>
<summary> Sererless </summary>
</details>

<details>
<summary> Logs: </summary>
</details>

<details>
<summary> Logs: </summary>
</details>
