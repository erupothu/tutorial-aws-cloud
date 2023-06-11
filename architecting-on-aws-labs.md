
#### Create Aws S3 bucket and upload object to s3

1. on services menu, search for s3
2. In the Navigation pane, selct bucket from left hand side of console.
3. Choose create bucket
4. for Bucket name Enter lab-bucket-global-unique
5. select region
6. leave all other setting as default configurations
7. Choose create bucket
8. In the amazon s3 console choose the lab-bucket
9. choose upload then add file, browse for image from the local machine
10. choose upload
11. close

#### AWS s3 with AWS CLI
1. open Terminal
2. aws confiure
  1. access key:
  2. secret key:
  3. region
3. aws s3 ls
4. aws s3 mb s3://lab-bucket-global-unique
5. aws s3 cp /home/downloads/happy.jpeg s3:/lab-bucket-gloabal-unique/
6. aws s3 ls s3://lab-bucket-global-unique

#### Creating to connection to EC2 command host using session manager  
1. search for EC2 instance
2. In the naviagtion pane left hand side, choose instancces, select command host 
3. Connect to instance, choose session manager tab.
4. choose connect

#### Build you AWS VPC Infrastructure

##### Creating Amazon VPC in a region
1. At the top of Aws management console, search for VPC
2. In the navigation pane left-hand-side your vpcs
3. enter tag Name: lab-vpc
4. IPV4 CIDR: 10.0.0.0/16
5. Choose create VPC
6. Edit VPC settings
7. From DNS setting section enable DNS Hostname
8. save

##### Creating Priavte subnet(remain isolate from internet) and Public Subnets (internet facing resources)

1. in the left Nagivation pane, choose subnet
2. Choose create subnet and Configure settings
3.  VPC ID: lab-vpc
4.  subnet name: public subnet
5.  Available zone: select first Available zone
6.  CIDR Block: 10.0.0.0/24
7.  Choose create subnet
8.  Edit Subnect settings
9.  Auto asign IP settings: enable auto-asign Public ipv4
10.  choose save
11.  Choose create subnet
12.  VPC ID: lab-vpc
13.  subnet name:   Private Subnet
14.  Availability zone: Select first Az
15.  IPV4 CIDR Block: 10.0.2.0/23
16.  Choose create subnet

##### Creating Internet Gateway (internet traffic can access public subnet
1. In the left navigation pane, choose Internet gateway
2. Choose create Internet gateway and configure the following
3. Name tag: Lab IGW
4. Choose Create Internet Gateway
5. choose Actions, and Choose Attach to VPC
6. Select lab-vpc from the dropdown
7. Choose Attach Internet gateway

##### Routing Interet Traffic to public subnet to Internet gateway
1. In the left navigation pane, choose route tables
2. Choose create table and configure the following
3. Name: Public routing table
4. VPC: lab-vpc
5. create routing table
6. Choose Edit Route
7. Choose add Route and configure the following
8. Destination: 0.0.0.0/0
9. Target: saved Internet Gateway from dropdown
10. choose save changes
11. Choose Subnet Association Tab
12. Choose Edit subnet associatons
13. select Public subnet
14. save association

#### Creating Public Security Group (users can access resource, traffic is allowed to and from resources)
1. In the left navigation page choose security group
2. Choose create security group and configure the following
3. Security group name: public SG
4. VPC: lab-vpc
5. Inbound rules: type: HTTP source: anywhere
6. Tags: Key: Name, value: Public SG
7. Choose create security group

##### Launch EC2 Instance into public subnet
1. From EC2 Dashboard, Launch instance section
2. Choose Launch instance
3. Name: public Instance
4. Select AMI
5. Amazon Linux OS
6. Amazon Linux 2023 AMI
7. t3.micro
8. Key pair Name: proceed without keypair
9. Network section, choose edit
10. VPC: lab-vpc
11. subnet: public subnet
12. Auto Assign public IP: enable
13. choose Public Security group
14. Default Storage
15. IAM Instance profile: EC2 Instance Profile
16. User Data: script to install apache2
17. create instance
18. Choose public DNS name and browse
19. connect to EC2 instance in public subnet through session manager

#### Create NAT Gateway and configure routinh in the Private Subnet (allows resource in private subnet to connect to the internet or other aws services)
1. search for VPC and choose vpc
2. in the left navigation pane, choose NAT Gateway
3. Choose NAT Gatewaya and Configure the following
4. Name: Lab NGW
5. Subnet: public subnet
6. Elastic IP AllocationID: choose allocate elasic ip
7. choose create NAT Gateway
8. In the left navigation pane, choose route tables
9. choose routing table and configure the following
10. Name: private routing table
11. VPC: lab-vpc
12. Choose create routing table
13. Choose the routes tab
14. Choose Edit routes
15. Choose add route and configure the following
16. Destination: 0.0.0.0/0
17. Target: saved NAT Gateway from the dropdown
18. Choose save changes
19. Choose Subnet Association tab
20. Choose edit subnet associations
21. select private subnet
22. choose save association

##### Create security group for private Resources
1. In the left navigation pane, choose security group
2. SG Name: private SG
3. VPC: lab-vpc
4. Inbound rules: type: HTTP, source: custom, Public SG
5. tag Name: name value: private SG
6. Choose create security group

##### Launch Amazon Ec2 instance in private Subnet
1. search for EC2 instance, EC2 Dashboard
2. Launch Instance section, Launch Instance
3. Location Tag and Name Private Instance
4. Select AMI, Type, keypair
5. VPC: lab-vpc
6. subnect: private Subnet
7. Auto Assign public IP: disable
8.  choose SG: private SG
9.  Default Storage
10.  IAM profile: Ec2-isntance-profile
11.  create instance
12.  Connect with aws session manager
13.  connect to CLI
14.  curl -i http://google.com
15.  




