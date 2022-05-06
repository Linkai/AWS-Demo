# AWS-Demo
This repo is for AWS learning and hands-on tutorial.

1, how to create EC2 and login with key pair from windows, linux, and mac
EC2 instance can be created in different regions, you can only display the instance in one region at the same time and cannot see the instance in other region, unless region is changed to specific one.

login Windows instance: rdp-->key pair will decrypt password for it.

login Linux instance: openssh-->putty, and puttygen, load private key file .pem and generate private key .ppk; public IP or public DNS

AWS account best practice:
1, root user should be only used when create the account and create admin user(policy: administratoraccess) in IAM. Then all the work should be done under admin user or other user.
2, config SSM to manage EC2 instance: create the role(IAM) for SSM(policy:AmazonEC2RoleforSSM), and associate the role with EC2 instance. All EC2 instance should install amazon ssm agent; some EC2 image has SSM agent already installed, some doesn't, need to manully install. Then in SSM(the region instance are)-->Mode management-->fleet manager, all the associated instance will list there.


