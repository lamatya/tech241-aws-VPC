# VPC- Virtual Private Cloud

VPC has a door known as Internet Gateway to enter the VPC. Inside the VPC it has Subnets. 

Public Subnet- people coming from internet has access to public subnet which is app VM. 

Private subnet: public cannot access. DB VM. 

Internet Gateway has route which uses route table 

IP address CIDR Block: 

- 10.0.2.0/16: This CIDR block represents a range of IP addresses starting from 10.0.2.0 to 10.0.255.255. It allows for a large number of available IP addresses for devices or resources within the network.

- 10.0.3.0/24: This CIDR block represents a range of IP addresses starting from 10.0.3.0 to 10.0.3.255. It has a slightly smaller range compared to the previous one, allowing for fewer available IP addresses within the network.

*CIDR blocks help in defining and managing IP address ranges within a network, ensuring efficient allocation of addresses to different components such as subnets, devices, or resources.*


      

# How to create VPC
1. Search for VPC on search bar
2. Go to create VPC
 ![Alt text](<create vpc.png>)

3. Select VPC only 
 ![Alt text](<VPC settings.png>)

4. Change IPv4 CIDR block to mannual input and input 10.0.0.0/16 on IPv4 CIDR and select create VPC
 ![Alt text](<VPC settings 2.png>)

5. Then Select on Internet gateway and create internet gateway once filled all the details select create internet gateway.
 ![Alt text](<Create internet gateway.png>) 

6. Once created Internet gateway select action and select attach to VPC. 
 ![Alt text](<attach to vpc.png>)

7. Attach the VPC created and select attach internet gateway.
 ![Alt text](<Create internet gateway.png>)

8. Select Subnets on right hand side and and go to create subnets.
 ![Alt text](subnets.png)

9. On subnet settings create public subnet and at bottom select add subnet and create subnet.
 ![Alt text](public.png)
 ![Alt text](private.png)

10. Then select route tables on right and create route table give the name and select VPC and create route table. 
![Alt text](<route table.png>)

11. Once created go to edit subnet association and select public subnet.
![Alt text](<edit subnets.png>)

12. Now go to route tab and select edit route and add edit routes. Put the destination and the targeti and select internet gateway(choose your one) and selecet save changes. 
![Alt text](<edit routes.png>) 

13. Now select your VPCs on right select the VPC created and check the resource map. 
![Alt text](<resource map.png>)


# How to add app VM in public subnet on VPC

1. go to ec2 and instances and lauch instances.
2. give name tech241-larisha-app-only-vpc
3. use image for asg ami app
4. on network setting use the right option
5. chooce your vpc
6. choose your public subnet
7. enable public ip
8. create a new security group and use the name of vm and add-sg-SSH-HTTp-3000
9. select asg-ami for image which has all the dependecies installed
10. add http rule and source type anywhere
11. custome tcp to anywhere source type port 3000 and for sparta app
12. go to advcanced detail and user data and add the only required script and launch instance.
13. select the instance and copy the public ip address. 



       



 # Virtual Private Cloud 


A VPC is a virtual network environment within the cloud that allows users to provision a logically isolated section of the AWS (Amazon Web Services) cloud where they can launch resources like EC2 instances, databases, and load balancers. It provides control over the network configuration, including IP address ranges, subnets, route tables, and network gateways.

# Benefits of VPCs:

1. Isolation and Security: VPCs offer a private network environment, allowing businesses to isolate their resources and securely connect to their on-premises infrastructure or other cloud services. 

2. Customization and Control: Users can define their IP address range, subnets, and routing tables, enabling them to design their network architecture according to their specific needs.

3. Scalability: VPCs allow businesses to scale their resources easily. Users can add or remove subnets, change IP address ranges, and expand their network as their requirements grow.

# Benefits for Business:

VPCs benefit businesses by providing a secure, customizable, and scalable network environment. They enable businesses to securely host their applications and data in the cloud while maintaining control over network configuration and access.

# Benefits for DevOps:

 VPCs empower DevOps teams to have control, security, and scalability over the networking aspects of their cloud infrastructure. They facilitate the deployment, management, and automation of application environments while adhering to best practices and ensuring efficient collaboration between development and operations teams. 

# Why AWS introduced VPCs:

AWS introduced VPCs to address the need for secure and customizable networking capabilities in the cloud. Use of VPCs allowed customers to create virtual networks that are logically isolated from each other and from the rest of the AWS infrastructure. This has improved the security, control, and flexibility, enabling businesses to migrate their infrastructure to the cloud and build complex application architectures.

