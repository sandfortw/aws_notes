Ec2 (Electric Cloud Compute)

A VPC (Virtual Private Cloud) is a virtual network dedicated to your AWS Account.

An AMI (Amazon Machine Image) is a template that countains the OS and other settings for your virtual server. 

There are many Ec2 instance types:

- General Purpose is balanced, a good choice for web servers
- Compute Optimizied has high cpu%, for HPC (High performance computing)
- Memory optimized (Large Data sets big data)
- Storage optimized - (Sequential read and write access)
- Accelerated computing - Machine Learning, etc. 


**QUEST: Configure a routing table and attach an internet gateway. Fix VPC Connectivity issues**  
*Scenario:* Customer's Ec2 Instances cannot connect to the internet, and the databases are unable to communicate with instances
<img width="1003" alt="image" src="https://github.com/sandfortw/aws_notes/assets/80081206/9896e173-c4c0-4cca-a81d-4ea0bc4cf8f0">

Amazon VPC (Virtual Private Cloud)
- Private Cloud within AWS
- Logically Isolated
- Launch AWS resources in a virtual network that you define

VPCs are launched with a range of private IP addresses "(IPV4, IPV6)

A subnet is a partition of the IP address range.
Each Subnet has an availability zone


Gateways:

**Internet Gateway** is horizontally scaled, redundant, and highly available by default

**NAT Gateway** Connected to the internet but denies outside connections

**(IPV6 Only) Egress only internet gateway**

VPC key Concepts:
VPC: Creates a range of IP addresses using classless inter-domain routing blocks
Allowed CIDR Block /16 /28

To deploy a working internet gateway, the following must be completed: 
- The internet gateway must be attached to a VPC
- Route tables associated with your public subnet must have a route to your internet gateway
- security groups associated with your VPC must allow traffic to/from the internet
- Any instances inthe VPC must have a public IP or elastic IP address assigned
