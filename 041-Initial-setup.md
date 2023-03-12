In order to use AWS CloudEndure Migration Service, you must create a Replication Server template. The template defines configuration of the server, that is responsible for receiving data sent by CloudEndure Migration Service agents and persisting the data on EBS volumes in your AWS account.

1. Go to AWS CloudEndure Migration console.
![image](https://user-images.githubusercontent.com/86204106/224569044-2d66c2dd-48f5-4ec4-98ca-129bfcc9d6c4.png)

2. Create an AWS CloudEndure project.
![image](https://user-images.githubusercontent.com/86204106/224570266-1a6d9d4b-75d0-4815-a019-6143cd27d759.png)

3. Populate Set up CloudEndure Migration Service screen with the following value.

4. Go to [AWS console management](https://us-east-1.console.aws.amazon.com/)
5. Go to VPC to create the VPC.
![image](https://user-images.githubusercontent.com/86204106/224571573-3ffc3634-f938-434d-8cf7-82220fb89c45.png)

6. Populate Set up and create the VPC by Name (OutpostVPC) and subnet (172.31.0.0/16)
![image](https://user-images.githubusercontent.com/86204106/224571722-7e40650d-695a-4db4-bd32-a5bc653db040.png)

7.

This is the subnet where AWS CloudEndure Migration Service will create Replication Servers.

Use default values for other parameters (click on the Info link next to them to understand their purpose).
