# Identity and Access Management (IAM)
## What is IAM?
 - IAM allows you you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources. 
 - IAM is a feature of your AWS account offered at no additional charge. You will be charged only for use of other AWS services by your users.

## Critical Terms:
 - User - the people logging into the AWS Console
   - The `root account` is simply the account created when first setup your AWS account. It has complete Admin access.
   - New users have no permission when first created.
   - New users are assigned `Access Key ID` and `Secret Access Keys` when first created. You only get to view these one. If you lose them, you have to regenerate them.
   - The Access Key ID and Secret Access Keys are not same as a password and you cannot use to login into the AWS Management Console. However, you can use these to access AWS via the APIs and command line.

 - Group - A collection of users under one set of permissions
   - For example the marketing team might need access to read and write certain files stored in an S3 bucket and that might be logos or images et cetera and they're going to need a specific set of permissions to allow them to do this. So it makes sense to create a group with the required permissions and then all you need to do is add the relevant users into that group and they will all have permissions to read us S3 buckets.

 - Role - An entity that has its own set of permissions, but that isn't a user or group. 
   - Roles also don't have their own permanent set of credentials the way IAM users do. In the case of Amazon EC2, IAM dynamically provides temporary credentials to the EC2 instance, and these credentials are automatically rotated for you.
   - Roles Can be assigned to AWS resources (ie EC2 instance) or third party accounts (ie. another AWS account or SAML 2.0).For example, when you launch an EC2 instance, you can specify a role for the instance as a launch parameter
   - Roles CANNOT be assigned to Users or Groups

 - Policy - A document (in JSON format) that defines one or more permissions (describe the level of access applied to an AWS resource by an AWS resource or user)

   - A policy can be attached to either a user, group or role. And then the user, group or role will have the permission defined within that policy.
   - An example policy below
   
   <code>
sdfsdf

   </code>

## Limitations on IAM Entities and Objects
Refer: https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_iam-limits.html

## IAM features

 - <b>Enhanced security</b>

   IAM enables security best practices by allowing you to grant unique security credentials to users and groups to specify which AWS service APIs and resources they can access. 
   
   IAM is secure by default; users have no access to AWS resources until permissions are explicitly granted.

 - <b>Granular control</b>

   IAM provides the granularity to control a user’s access to specific AWS services and resources using permissions. For example, terminating EC2 instances or reading the contents of an S3 bucket.

 - <b>Temporary credentials</b>
 - <b>Flexible security credential management</b>
 - <b>Leverage external identity systems</b>
 - <b>Seamlessly integrated into AWS services</b>
 - <b>Intended usage & restrictions</b>

 ## Demotration 
T.B.D


## Best practices
Refers: https://docs.amazonaws.cn/en_us/IAM/latest/UserGuide/best-practices.html

 - <b>Lock Away Your AWS Account Root User Access Keys</b>

   You use an access key (an access key ID and secret access key) to make programmatic requests to AWS. However, `do not use your AWS account root user access key`. The access key for your AWS account root user gives full access to all your resources for all AWS services, including your billing information. You cannot reduce the permissions associated with your AWS account root user access key

 - <b>Create Individual IAM Users</b>

   By `creating individual IAM users` for people accessing your account, you can give each IAM user `a unique set of security credentials`. You can also grant different permissions to each IAM user. If necessary, you `can change or revoke an IAM user's permissions any time`. (If you give out your root user credentials, it can be difficult to revoke them, and it is impossible to restrict their permissions.)

 - <b>Use Groups to Assign Permissions to IAM Users</b>
    
   Instead of defining permissions for individual IAM users, it's usually more convenient to create groups that relate to job functions (administrators, developers, accounting, etc.). Next, define the relevant permissions for each group. Finally, assign IAM users to those groups. `All the users in an IAM group inherit the permissions assigned to the group`. That way, you `can make changes for everyone in a group in just one place`.

 - <b>Grant Least Privilege</b>
    
   When you create IAM policies, follow the standard security advice of granting least privilege, or `granting only the permissions required to perform a task`. Determine what users need to do and then craft policies for them that let the users perform only those tasks. 
   
   Start with a minimum set of permissions and grant additional permissions as necessary.

 - <b>Get Started Using Permissions With AWS Managed Policies</b>
   
   Providing your employees with only the permissions they need requires time and detailed knowledge of IAM policies. Employees need time to learn which AWS services they want or need to use. Administrators need time to learn about and test IAM.

   `AWS managed policies` are designed to `provide permissions for many common use cases`. AWS managed policies make it easier for you to assign appropriate permissions to users, groups, and roles than if you had to write the policies yourself. These policies are already available in your account and `are maintained and updated by AWS`.

 - <b>Use Customer Managed Policies Instead of Inline Policies</b>
   
   Inline policies are policies that exist only on an IAM identity (user, group, or role). Managed policies are separate IAM resources that you can attach to multiple identities.

 - <b>Use Access Levels to Review IAM Permissions</b>
   
   To improve the security of your AWS account, you `should regularly review and monitor each of your IAM policies`. Make sure that your policies grant the least privilege that is needed to perform only the necessary actions.

 - <b>Configure a Strong Password Policy for Your Users</b>
   
   You can `use the password policy to define password requirements`, such as minimum length, whether it requires non-alphabetic characters, how frequently it must be rotated...

 - <b>Enable MFA for Privileged Users</b>

   For extra security, `enable multi-factor authentication (MFA) for privileged IAM users`.  The response is generated in one of the following ways:
   - Virtual and hardware MFA devices generate a code that you view on the app or device and then enter on the sign-in screen.
   - U2F security keys generate a response when you tap the device. The user does not manually enter a code on the sign-in screen.

 - <b>Use Roles for Applications That Run on Amazon EC2 Instances</b>

   Applications that run on an Amazon EC2 instance need credentials in order to access other AWS services. `To provide credentials to the application in a secure way, use IAM roles`. Applications that run on the EC2 instance can use the role's credentials when they access AWS resources. The role's permissions determine what the application is allowed to do.

 - <b>Use Roles to Delegate Permissions</b>

   `Don't share security credentials between accounts` to allow users from another AWS account to access resources in your AWS account. Instead, use IAM roles.

 - <b>Do Not Share Access Keys</b>

   Access keys provide programmatic access to AWS. `Do not embed access keys within unencrypted code or share these security credentials between users` in your AWS account. 

 - <b>Rotate Credentials Regularly</b>
   
 - <b>Remove Unnecessary Credentials</b>

   Remove IAM user credentials (passwords and access keys) that are not needed.

 - <b>Use Policy Conditions for Extra Security</b>
   
   Restrict privileged access further with conditions. For example, you can write conditions to specify a range of allowable IP addresses that a request must come from. You can also specify that a request is allowed only within a specified date range or time range. You can also set conditions that require the use of SSL or MFA (multi-factor authentication). 

 - <b>Monitor Activity in Your AWS Account</b>

   You can use logging features in AWS to determine the actions users have taken in your account and the resources that were used. The log files show the time and date of actions, the source IP for an action, which actions failed due to inadequate permissions, and more.

   Logging features are available in the following AWS services:
   - Amazon CloudFront – Logs user requests that CloudFront receives. 
   - AWS CloudTrail – Logs AWS API calls and related events made by or on behalf of an AWS account.
   - Amazon CloudWatch – Monitors your AWS Cloud resources and the applications you run on AWS. You can set alarms in CloudWatch based on metrics that you define.
   - AWS Config – Provides detailed historical information about the configuration of your AWS resources, including your IAM users, groups, roles, and policies. For example, you can use AWS Config to determine the permissions that belonged to a user or group at a specific time.
   - Amazon Simple Storage Service (Amazon S3) – Logs access requests to your Amazon S3 buckets.













