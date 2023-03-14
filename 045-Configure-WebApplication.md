Configure the Webserver to access the target database
When the Cutover is finished and CloudEndure Migration Service has created a running instance of the Webserver in your AWS account, it's time to update the web application configuration to use your replicated AWS RDS database (created in the Database Migration step).
1. Update the Webserver security group

a. Go to AWS Console -> EC2 and select the Webserver on the list
b. Go to Security tab and click on the security group that webserver has assigned

![image](https://user-images.githubusercontent.com/86204106/224885299-737741a3-5742-40c4-a4f7-8e14c7a34de1.png)


Connect via SSH to the Webserver created by the Application Migration Service

Use the same username (ubuntu) and SSH .ppk key as for the Source Environment.

If you're not sure how to use SSH to access servers, check the following:

For Microsoft Windows users view this article .

For Mac OS users view this article .

Alternatively to SSH, you can use Session Manager capability that lets you manage Amazon EC2 instances through a browser-based shell. To connect to a Linux instance using Session Manager using the Amazon EC2 console:

Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/ 
In the navigation pane, choose Instances.
Select the instance and choose Connect.
For Connection method, choose Session Manager.
Choose Connect.
Modify the wordpress configuration

Edit the /var/www/html/wp-config.php file, modifying

DB_HOST - Endpoint of the created RDS instance (from the DMS step)
DB_USER - the username configured in the Database Migration step
DB_PASSWORD - the password configured in the Database Migration step
Also add the following two lines, replacing TARGET_WEBSERVER_PUBLIC_DNS with your Target Webserver EC2 Public DNS (IPv4), to make sure links in your wordpress site point to the new webserver.


=========================================

define('WP_SITEURL', 'http://TARGET_WEBSERVER_PUBLIC_DNS');        
define('WP_HOME',    'http://TARGET_WEBSERVER_PUBLIC_DNS');

=========================================


==========Sample=========================

define('WP_SITEURL', 'http://ec2-34-208-233-184.us-west-2.compute.amazonaws.com');
define('WP_HOME',    'http://ec2-34-208-233-184.us-west-2.compute.amazonaws.com');

=========================================


Validate the migration

Open the Webserver Public DNS (IPv4) name in your web browser, you should see a unicorn store.

If everything works fine - proceed to the next phase, so Move to Containers!

Troubleshooting
Make sure that RDS database related information configured on the Webserver in /var/www/html/wp-config.php is correct
Make sure that the RDS database is using the DB-SG security group
Make sure that the Webserver EC2 Launch Template points at a TargetVPC public-subnet-a
Use the RDS endpoint full name from AWS console -> RDS -> Databases -> database-1 -> Conectivity & security -> Endpoint & port copy the full name
