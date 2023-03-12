In order to use AWS CloudEndure Migration Service, you must create a Replication Server template. The template defines configuration of the server, that is responsible for receiving data sent by CloudEndure Migration Service agents and persisting the data on EBS volumes in your AWS account.

1. Go to AWS CloudEndure Migration console.
![image](https://user-images.githubusercontent.com/86204106/224569044-2d66c2dd-48f5-4ec4-98ca-129bfcc9d6c4.png)

2. Create an AWS CloudEndure project.
![image](https://user-images.githubusercontent.com/86204106/224570266-1a6d9d4b-75d0-4815-a019-6143cd27d759.png)

![image](https://user-images.githubusercontent.com/86204106/224570607-c5877f91-4939-432b-be4b-3ce157f8bbc1.png)

3. Populate Set up CloudEndure Migration Service screen with the following value.
![image](https://user-images.githubusercontent.com/86204106/224570278-0ccb4602-2c18-45eb-9557-74e0722f22af.png)

This is the subnet where AWS Application Migration Service will create Replication Servers.

Use default values for other parameters (click on the Info link next to them to understand their purpose).
