# Clickops_Armageddon

### Step 1)

Create a VPC:

- Go to VPC Dashboard > Your VPCs > Create VPC and more with 2 AZs

- VPC Name: armageddon-demo

- CIDR: 10.180.0.0/16

- Public and private subnets in 2 different AZs.

- Tag for good office practice: <name> <armageddon-demo>

- Create

![](/2026.1.12clickopsdoc/attachments/vpc.png)

### Step 2)

Create Security Groups:

- In the left pane of VPC Dashboard, select Security groups from the Security secton

- Pulic Subnet sg is for ec2 instance

- SG name: armageddon-public-sg
    Inbound rules: HTTP > Port 80 > from anywhere 0.0.0.0/0 > Homepage
    SSH > Port 22 > 

    ![](/2026.1.12clickopsdoc/attachments/public-sg.png)

    In this security group we would normally use My IP for SSH.

- Tag for good office practice: <name> <armageddon-public-sg>

![](/2026.1.12clickopsdoc/attachments/sg-2.png)

- Create

- Now Create Private DB SG: <armageddon-db-sg>

- In both of these sg ensure you are choosing the proper VPC.

- Only allow access form the ec2 instance sg > <armageddon-public-sg> It will just be the sg-id

![](/2026.1.12clickopsdoc/attachments/db-sg.png)

- Create

![](/2026.1.12clickopsdoc/attachments/db-sg-2.png)

### Step 3)











