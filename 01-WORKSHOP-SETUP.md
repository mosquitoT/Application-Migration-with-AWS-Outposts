Option 1: Simple Deployment
1. Click here  to launch the CloudFormation stack.

2. On the Step 1 - Specify template confirm that the URL https://ee-assets-prod-us-east-1.s3.us-east-1.amazonaws.com/modules/migration/v1/migration_workshop_source_template.yml  is entered in the Amazon S3 URL field and press Next.
![image](https://user-images.githubusercontent.com/86204106/224564455-675cff31-4e50-44d3-a4f4-b733c3736e41.png)

3. On the Step 2 - Specify stack details screen make sure ApplicationMigrationWorkshop is entered in the Stack name field and press Next
![image](https://user-images.githubusercontent.com/86204106/224565132-f972af18-7123-484c-8071-41daa0262c82.png)

4. On the Step 3 - Configure stack options screen don't make any changes, just press Next

5. On the Step 4 - Review screen, scroll to the bottom of the page and check all checkboxes, as on the screenshot below, then press Create stack for the template to be deployed.
![image](https://user-images.githubusercontent.com/86204106/224565318-6ba0e170-c5cb-4b7c-b7cf-7874d48e9d86.png)

When the template is in the CREATE_COMPLETE you can find information about created source environment by going to AWS Console -> CloudFormation, selecting ApplicationMigrationWorkshop stack and going to the Outputs tab. You will see information like on the screenshot below.
![image](https://user-images.githubusercontent.com/86204106/224565483-13f35baa-a9eb-432d-b206-07fd098f935b.png)

Now you can review the deployed environment

