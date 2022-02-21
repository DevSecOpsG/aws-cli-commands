# aws-cli-commands

AWS Command
● aws ​configure
AWS Access Key ID​ [None]:​ accesskey AWS
Secret Access Key​ [None]:​ secretkey
Default region name​ ​[None]:​ us-west-2
Default output format​ ​[None]:json

VPC Configuration
● aws​ ​ec2​ ​create-vpc​ --cidr-block​ ​10.0.0.0/16
● aws​ ​ec2​ ​create-subnet​ ​--vpc-id ​vpc-1234567890​ ​--cidr-block
10.0.1.0/24
● aws​ ​ec2​ ​create-subnet​ ​--vpc-id​ ​vpc-1234567890​ ​--cidr-block
10.0.2.0/24
● aws​ ​ec2​ ​create-internet-gateway
● aws​ ​ec2​ ​attach-internet-gateway​ ​--vpc-id​ ​vpc-1234567890
--internet-gateway-id​ ​igw-1234567890
● aws​ ​ec2​ ​create-route-table​ ​--vpc-id​ ​vpc-1234567890
● aws​ ​ec2​ ​create-route​ ​--route-table-id​ ​rtb-1234567890
--destination-cidr-block​ 0.0.0.0/0 ​--gateway-id​ ​igw-1234567890
● aws​ ​ec2​ ​describe-route-tables​ ​--route-table-id​ rtb-1234567890
● aws​ ​ec2​ ​describe-subnets​ ​--filters
"Name=vpc-id,​Values​=vpc-2f09a348" ​--query
'Subnets[*].{ID:SubnetId,CIDR:CidrBlock}'
● aws​ ​ec2​ ​associate-route-table​ ​--subnet-id​ subnet-b46032ec
--route-table-id​ rtb-c1c8faa6
EC2 Instance
● aws ​ec2​ ​describe-instance-status
● aws ​ec2​ ​start-instances​ --instance-ids​ ​i-123456789
● aws ​ec2​ ​stop-instances​ ​--instance-ids​ ​i-123456789

● aws​ ​ec2 ​terminate-instances​ ​--instance-ids​ i-1a2b3c4d
● aws​ ​ec2 ​describe-volumes
● aws​ ​ec2​ create-key-pair ​--key-name​ MyKeyPair ​--query
'KeyMaterial' --output text > ​MyKeyPair​.​pem
● aws ec2 create-security-group --group-name SSHAccess
--description "Security group for SSH access" --vpc-id
vpc-1234567890
● aws ec2 authorize-security-group-ingress --group-id sg-e1fb8c9a
--protocol tcp --port 22 --cidr 0.0.0.0/0
● aws ec2 run-instances --image-id ami-a4827dc9 --count 1
--instance-type t2.micro --key-name MyKeyPair
--security-group-ids sg-e1fb8c9a --subnet-id subnet-b46032ec
●
● aws ​s3 ​mb​ ​s3://sansbound
● aws ​s3 ​rb​ ​s3://bucket-name
● aws ​s3​ ls
● aws​ ​s3​ ​cp​ ​C:\Users\test\Desktop\test.png​ ​s3://bucketname ​copy
file
●
● aws​ iam​ ​create-user​ ​--user-name​ Employee1
● aws ​s3​ ​sync​ ​c:\tub​ ​s3://bucketname
