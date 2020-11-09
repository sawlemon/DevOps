[aws docs VPCs and subnets](https://github.com/awsdocs/amazon-vpc-user-guide/blob/master/doc_source/VPC_Subnets.md#vpc-subnet-basics)

## [VPC](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html)

**subnet is mandatory**

https://youtu.be/rQvl-V3tLiQ

A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud


When you create a VPC, you must specify a range of IPv4 addresses for the VPC in the form of a Classless Inter-Domain Routing (CIDR) block; for example, 10.0.0.0/16

Availability Zones are multiple, isolated locations within each Region.

![](2020-10-02-23-49-11.png)



1. An internet gateway enables communication over the internet, and a virtual private network (VPN) connection enables communication with your corporate network.

If a subnet's traffic is routed to an internet gateway, the subnet is known as a public subnet




## [Subnet](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Subnets.html#vpc-subnet-basics)

Range of IP Adresses in the VPC.



![](2020-10-02-23-52-05.png)

### Aws uses the first 4 and last 1 IP Address in a subnet forr internal purposes. So the subnet count is reduced by 5

![](2020-10-03-01-02-31.png)

If you create a VPC or subnet using a command line tool or the Amazon EC2 API, the CIDR block is automatically modified to its canonical form. For example, if you specify 100.68.0.18/18 for the CIDR block, we create a CIDR block of 100.68.0.0/18



[Tenancy Values]
## Dedicated Instances

Dedicated Instances are Amazon EC2 instances that run in a virtual private cloud (VPC) on hardware that's dedicated to a single customer

## Dedicated Host

A Dedicated Host is also a physical server that's dedicated for your use. With a Dedicated Host, you have visibility and control over how instances are placed on the server.

### [Difference b/w Dedicated Instance and Dedicated Host](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-hosts-overview.html#dedicated-hosts-dedicated-instances)

## Elastic IP Address
 
**public IPv4 address or an Elastic IP address**

An Elastic IP address is a static IPv4 address associated with your AWS account in a specific Region.


## [EBS](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html)
    
*The volume and instance must be in the same Availability Zone.*

    Elastic Block Store


Load Balancer

[AWS - ALB - Application Load Balancer - Setup & DEMO - Differences from Classic ELB](https://youtu.be/OKnd03nxu3k)

[AWS ELB Tutorial | Elastic Load Balancer Tutorial | AWS Tutorial | AWS Training Video | Simplilearn](https://youtu.be/YO4L_9poF3g)