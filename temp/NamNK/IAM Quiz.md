## IAM Quiz
1. Which of the following is NOT a feature of IAM?
   - Centralised control of your AWS account
   - Integrates with existing active directory account allowing single sign on
   - Fine-grained access control to AWS resources
   - `Allows you to setup biometric authentication, so that no passwords are required`

2. AWS recommends that EC2 instances have credentials stored on them so that the instances can access other resources (such as S3 buckets).
   - True
   - `False`

3. Which IAM entity can you use to delegate access to your AWS resources to users, groups or services?
   - IAM User
   - IAM Web Identity Federation
   - `IAM Role`
   - IAM Group

4. In AWS, what is IAM used for?
   - Secure VPN access to AWS
   - `Creating and managing users and groups, managing access to AWS services & assigning permissions to allow and deny access to AWS resources.`
   - To move large amounts of data (Terrabytes) in to AWS.
   - IAM is a serverless compute platform.

5. What is an IAM Policy?
   - A csv file which contains a users Access Key and Secret Access Key
   - `A JSON document which defines one or more permissions`
   - A file containing a user's private ssh key
   - The policy which determines how your AWS bill will be paid.

6. Which is the best way to enable your EC2 instance to read files in an S3 bucket?
   - Create a new IAM user and grant read access to S3. Store the user's credentials locally on the EC2 instance and configure your application to supply the credentials with each API request.
   - Configure a bucket policy which grants read access based on the EC2 instance name.
   - `Create an IAM role with read access to S3 and assign the role to the EC2 instance.`
   - Create a new IAM role and grant read access to S3. Store the role's credentials locally on the EC2 instance and configure your application to supply the credentials with each API request.

7. Which statement best describes IAM?
   - `IAM allows you to manage users, groups, and roles and their corresponding level of access to the AWS Platform.`
   - IAM allows you to manage users' passwords only. AWS staff must create new users for your organization. This is done by raising a ticket.
   - IAM allows you to manage permissions for AWS resources only.
   - IAM stands for Improvised Application Management, and it allows you to deploy and manage applications in the AWS Cloud.
