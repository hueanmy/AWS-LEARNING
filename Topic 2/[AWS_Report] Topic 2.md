# Identity and Access Management (IAM)
##1. Definition
  - AWS Identity and Access Management (IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources.
  - IAM is a feature of your AWS account offered at no additional charge. You will be charged only for use of other AWS services by your users.
![](imgs/iam_architecture.png)
####Terms
  - **Resources**: The user, role, group, and policy objects that are stored in IAM. As with other AWS services, you can add, edit, and remove resources from IAM
  - **Identities**: The IAM resource objects that are used to identify and group. These include users, groups, and roles.
  - **Entities**: The IAM resource objects that AWS uses for authentication. These include users and roles. Roles can be assumed by IAM users in your or another account as well as users federated through a web identity or SAML.
  - **Pricipals**: A person or application that uses an entity to sign in and make requests to AWS
####Principal
  - A principal is a person or application that can make a request for an action or operation on an AWS resource.
####Request

###1.1 Users
  - IAM Users
    + An account can have many users
    + An user can be present by an application, not a person
  - Federating Existing Users
    + If the users in your organization already have a way to be authenticated, such as by signing in to your corporate network, you don't have to create separate IAM users for them. Instead, you can federate those user identities into AWS.
![](imgs/iam-intro-federation.png)
    + To use identity federation with Internet identity providers, we recommend you use [Amazon Cognito](https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html)
###1.2 Permission and Policies
  - A policy is an object in AWS that, when associated with an identity or resource, defines their permissions. AWS evaluates these policies when a principal uses an IAM entity (user or role) to make a request. Permissions in the policies determine whether the request is allowed or denied. Most policies are stored in AWS as JSON documents
  - **Policies and Accounts**
  - **Policies and Users**
    ```json
    {
      "Version": "2012-10-17",
      "Statement": {
        "Effect": "Allow",
        "Action": "dynamodb:*",
        "Resource": "arn:aws:dynamodb:us-east-2:123456789012:table/Books"
      }
    }
    ```
    + Policies are summarized in three tables: the [policy summary](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_understand-policy-summary.html), the [service summary](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_understand-service-summary.html), and the [action summary](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_understand-action-summary.html). The policy summary table includes a list of services. Choose a service there to see the service summary. This summary table includes a list of the actions and associated permissions for the chosen service. You can choose an action from that table to view the action summary. This table includes a list of resources and conditions for the chosen action
    ![](imgs/policy_summaries-diagram.png)
  - **Policies and Groups**
  - **Federated Users and Roles**: Federated users don't have permanent identities in your AWS account the way that IAM users do. To assign permissions to federated users, you can create an entity referred to as a role and define permissions for the role. When a federated user signs in to AWS, the user is associated with the role and is granted the permissions that are defined in the role
  - **Identity-based and Resource-based Policies**
    + Identity-based policies
      - Managed policies: AWS managed policies & Customer managed policies
      - Inline policies:
    + Resource-based policies: control what actions a specified principal can perform on that resource and under what conditions. Resource-based policies are inline policies, and there are no managed resource-based policies
###1.3 Security Features Outside of IAM
  - The user can access resource of AWS without IAM such as Amazon EC2, Amazon RDS, Amazon WorkSpaces, Amazon WorkDocs by key pair or username, password
##2. How to use?
  - AWS Management Console
  - AWS Command Line Tools
  - AWS SDKs
  - IAM HTTPS API

Note: [AWS Services That Work with IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_aws-services-that-work-with-iam.html)
##3. Topics
##4. Practices
In this document, we will use [AWS Management Console](https://console.aws.amazon.com/iam/home#/home) to demo
- Firstly, you should create Administrator user
![](imgs/create-user/create_user_1.PNG)

###Note:
- Don't use Root user for every tasks, just use to create first IAM users
- There are some tasks we need to use root user, please refer to [AWS Tasks That Require AWS Account Root User Credentials](https://docs.aws.amazon.com/general/latest/gr/aws_tasks-that-require-root.html)
- We should create an IAM user for yourself and then assign yourself administrative permissions for your account. You can then sign in as that user to add more users as needed
- Should add multi-factor authentication (MFA)
####References
[AWS IAM introduction](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)