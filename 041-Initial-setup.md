In order to use AWS CloudEndure Migration Service, you must create a Replication Server template. The template defines configuration of the server, that is responsible for receiving data sent by CloudEndure Migration Service agents and persisting the data on EBS volumes in your AWS account.

1. Go to AWS CloudEndure Migration console.
![image](https://user-images.githubusercontent.com/86204106/224569044-2d66c2dd-48f5-4ec4-98ca-129bfcc9d6c4.png)

2. Create an AWS CloudEndure project.
![image](https://user-images.githubusercontent.com/86204106/224570266-1a6d9d4b-75d0-4815-a019-6143cd27d759.png)

3. Populate Set up CloudEndure Migration Service screen with the following value.

4. Go to [AWS console management](https://us-east-1.console.aws.amazon.com/)
5. Go to VPC to create the VPC.
![image](https://user-images.githubusercontent.com/86204106/224571573-3ffc3634-f938-434d-8cf7-82220fb89c45.png)

6. Populate Set up and create the VPC by Name (OutpostVPC) and subnet (172.16-31.0.0/16)
![image](https://user-images.githubusercontent.com/86204106/224571722-7e40650d-695a-4db4-bd32-a5bc653db040.png)

7. Go to VPC to create the Subnet. 
![image](https://user-images.githubusercontent.com/86204106/224783169-66ed3986-7ae7-426d-a608-b01239ffe2d3.png)

8. Create the Subnet name(Outposts-basion)
![image](https://user-images.githubusercontent.com/86204106/224788386-092cc754-27a6-478a-b325-061ecdfa9120.png)
Repeat the action to create 7 subnets. (TVPC-Outpost-pri-a-db,TVPC-Outpost-pri-b-db, TVPC-Outpost-pub-a, TVPC-Outpost-pub-b,TVPC-Outpost-pri-a-web, TVPC-Outpost-pri-b-web)
![image](https://user-images.githubusercontent.com/86204106/224793185-745e45ac-8c48-4966-b87c-39a80d71cdec.png)

9. Create the InternetGateway(OutpostVPC-IGW)
![image](https://user-images.githubusercontent.com/86204106/224789102-ea9761ea-eec7-4d3e-b464-f4f9f8d349a4.png)

10. Create the route table (outposts-rtb)
![image](https://user-images.githubusercontent.com/86204106/224790976-10a7eb88-264a-4634-9cbe-c2cb8634f56f.png)


This is the subnet where AWS CloudEndure Migration Service will create Replication Servers.

Use default values for other parameters (click on the Info link next to them to understand their purpose).
