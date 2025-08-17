Assignment 1: Automated Instance Management Using AWS Lambda and Boto3
Objective: In this assignment, you will gain hands-on experience with AWS Lambda and Boto3, Amazon's SDK for Python. You will create a Lambda function that will automatically manage EC2 instances based on their tags.
Steps:- 
1.	Created 2 instances and tagged them as auto start and auto stop where one of the ec2 instance which was tagged as auto start was in stopped state and the other ec2 instances which was tagged as auto stop was in running state.
Here i-0f38a58ec7341c52e is tagged as auto stop and i-01e59b85e565507e1 as auto start.
 
 ![Screenshot](https://github.com/SAGA-1102/serverless-architecture/blob/main/Screenshot%202025-08-17%20182439.png)
 

2.	We create a role for the lambda named as “SAGALamdbarole”
 

3.	After creating this role we created lambda function named as”sagadunction08”
 



4.	The below code states that the instance which is running will be stopped and the server which is stopped will be started.
 
 
5.	After coding we deployed the code and tested it and below is the screenshot of the cloudwatch logs.
 
6.	Now after this you can auto stop and auto start is working on both the instances as seen below.
 
  


Assignment 2: Automated S3 Bucket Cleanup Using AWS Lambda and Boto3
Objective: To gain experience with AWS Lambda and Boto3 by creating a Lambda function that will automatically clean up old files in an S3 bucket.
1.	We created a bucket named as “SAGAbucket1102”
Where we uploaded 4 files.
 
2.	We crated a role for above bucket named as “s3lambda”
 
3.	After creating role we crated a function for this role named as “s3fuction”
 
4.	Below code shows that we are going to delete files older than 0 days.
 
 
5.	After coding we deployed our code and tested now you can see the logs are created for the successful deletion of the files which were 0 days older.
 
6.	For verification we will go to our s3 bucket and see if it was actually successfully done or not.
 



Assignment 3: Monitor Unencrypted S3 Buckets Using AWS Lambda and Boto3
Objective: To enhance your AWS security posture by setting up a Lambda function that detects any S3 bucket without server-side encryption.
Task: Automate the detection of S3 buckets that don't have server-side encryption enabled.

1.	Create s3 bucket for this named as “saga-bucket16” which we have encrypted .
 
 
2.	We create a role for above bucket as “lamdbas3readonlyrole”
 
3.	We have created function for above role named as”lamdbaunencryptedbucket”


 
4.	Below is the code which shows it find all the bukcets which are unencrupyed in the region –“ca-central-1”
 
 
5.	After coding we deployed the code and below are the logs for the unencryption check
 
 
 
 
 
 
 






Assignment 4: Automatic EBS Snapshot and Cleanup Using AWS Lambda and Boto3
Objective: To automate the backup process for your EBS volumes and ensure that backups older than a specified retention period are cleaned up to save costs
1, We have created an EBS volume for this named as “sagasnapshot”
 
2. we created a rule for snapshot.
 
3. We also created a role to run.
 
6.	For executing successfully we created a lambda function name as”saga-snapshot-manager”
 
7.	For taking the snapshot below is code which we used
 
 
8.	After running the script we were able to find the logs of the snapshot as below
 
7.	Below is the snapshot created.
 
