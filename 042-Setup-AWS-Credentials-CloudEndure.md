Generating the Required AWS Credentials
https://docs.cloudendure.com/#Generating_and_Using_Your_Credentials/Working_with_AWS_Credentials/Generating_the_Required_AWS_Credentials/Generating_the_Required_AWS_Credentials.htm#Generating_the_Required_AWS_Credentials%3FTocPath%3DNavigation%7CGenerating%2520and%2520Using%2520Your%2520Credentials%7CWorking%2520with%2520AWS%25C2%25A0Credentials%7CGenerating%2520the%2520Required%2520AWS%2520Credentials%7C_____0

To generate the required AWS credentials to use with the CloudEndure User Console, you need to create at least one AWS Identity and Access Management (IAM) user, and assign the proper permission policy to this user. You will obtain an Access key ID and a Secret access key, which are the credentials you need to enter into the CloudEndure User Console.

For detailed explanations and instructions on the creation of IAM users, refer to the AWS documentation.

The instructions below describe the necessary steps for creating an IAM user with the required policy for CloudEndure User Console credentials. These steps include the following:

Creating a policy for the CloudEndure solution.
1. Creating a new IAM user and generating AWS credentials
2. Creating a Policy for CloudEndure
The AWS policy you need to create for running CloudEndure solution is based on a pre-defined CloudEndure policy. This CloudEndure policy contains the necessary permissions for using AWS as your Target infrastructure.


To create an AWS policy for CloudEndure solution:
1. Sign in to AWS Console with your AWS account.
![image](https://user-images.githubusercontent.com/86204106/224573533-7ab01afb-0e18-4e79-b702-d4364152f9c9.png)


2. In the AWS Console, click on Services and then navigate to Security, Identity & Compliance > IAM.
![image](https://user-images.githubusercontent.com/86204106/224573561-12f52d48-76b9-4399-852a-e6f3a2c4eef1.png)
3. On the Welcome to Identity and Access Management page, select the Policies option from the left-hand navigational menu.
![image](https://user-images.githubusercontent.com/86204106/224573568-6ff74d8b-5cfe-409b-9376-0ad75072f906.png)

4. On the Policies page, click the Create policy button.
![image](https://user-images.githubusercontent.com/86204106/224573621-7285dd8a-29e3-4429-91a6-793cfd15795f.png)

5. On the Create Policy page, click the JSON tab.
![image](https://user-images.githubusercontent.com/86204106/224573643-db4584d7-4120-43c0-8237-78172e5a2926.png)

6. Navigate to the CloudEndure IAM Policy. Copy the policy code.
Note: Customers that are migrating into the AWS China region should copy the China IAM Policy code

7. Paste the copied code into the JSON field. Paste the code over any text that currently exists in the field.
8. Click on Review policy at the bottom right of the page.
![image](https://user-images.githubusercontent.com/86204106/224573700-66aeb39c-5a27-423e-9ba4-45aafd2b32a1.png)

9. On the Review policy page, enter a name for the new AWS-CloudEndure policy in the Name field. Enter an optional description in the Description field.
![image](https://user-images.githubusercontent.com/86204106/224573727-1584bf5d-7c91-4d9d-b223-741d657c852b.png)

10. Click the Create policy button at the bottom right of the page.
![image](https://user-images.githubusercontent.com/86204106/224573744-d28dc969-3eab-49e2-a182-0b3a1ff58ba0.png)

11. You will be redirected back to the main Policies page and a confirmation stating that your new policy has been created will appear at the top of the page.
![image](https://user-images.githubusercontent.com/86204106/224573758-d2112581-e955-43b7-bf0d-03510eddd36e.png)

The next step is to create a new user, and then attach the policy you created to this user. During this procedure, you will be provided with an Access key ID and a Secret access key, which are the credentials you will need to enter into CloudEndure User Console.

Creating a New IAM User and Generating AWS Credentials
After creating an AWS policy which is based on CloudEndure's pre-defined policy, you will need to create a new IAM user and to attach the new policy to this user. You also need to provide this user with a Programmatic access type to enable the use of the new policy. At the end of this procedure, you will be provided with an Access key ID and Secret access key. It is important to save these values in an accessible and secured location, since they are required for running your CloudEndure solution.

Creating a new IAM User and generating AWS credentials
1. Navigate to Users on the left-hand navigational menu within IAM.
2. Add users
![image](https://user-images.githubusercontent.com/86204106/224573814-07282389-63a7-48d3-b8fe-e4d52166832e.png)
3. On the Add user page, set the following:
  - User name - add a username for the new user.
  - Access type - check the Programmatic access option.
4. On the Set permissions page, select the Attach existing policies directly option
![image](https://user-images.githubusercontent.com/86204106/224573838-145e2043-59ec-4f1f-a77b-bfde0bc84b95.png)

5. Locate the policy you created in the previous Create a Policy for CloudEndure section. You can either search for the policy in the Search box or locate it manually by scrolling through the policy list.
![image](https://user-images.githubusercontent.com/86204106/224573852-27ef502b-c6c1-422e-b452-4eba9b4de7fb.png)



12. 
