---
title: AWS policies
description: The Cloud Configuration Governance AWS policies are listed for your reference.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# AWS policies

The Cloud Configuration Governance AWS policies are listed for your reference.

<table id="table_ify_b3v_t2c"><thead><tr><th>

Policy Set

</th><th>

Policy Name

</th><th>

Resource Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

AWS IAM User Activity policy

</td><td>

Condition builder

</td><td>

Policy to check if the password is enabled for the AWS IAM user.To use this policy, ensure that the AWS IAM user account has the following permissions:

-   Iam:GetCredentialReport
-   Iam:GenerateCredentialReport

</td></tr><tr><td>

 

</td><td>

AWS S3 Enforce Bucket encryption

</td><td>

Condition builder

</td><td>

Policy to check if the AWS S3 buckets are encrypted.

</td></tr><tr><td>

 

</td><td>

AWS Sample flow policy

</td><td>

Integration Hub flow

</td><td>

Policy to illustrate an Integration Hub flow-based policy.

</td></tr><tr><td>

 

</td><td>

AWS VM HardwareType

</td><td>

Condition builder

</td><td>

Policy to check if the deployed EC2 VMs are using only the approved hardware types.

</td></tr><tr><td>

 

</td><td>

AWS VM IPAddress

</td><td>

Script

</td><td>

Policy to check if the IP address of the EC2 VM is matching with the Configuration Management Database \(CMDB\) record.

</td></tr><tr><td>

 

</td><td>

AWS VM Monitoring State

</td><td>

Condition builder

</td><td>

Policy to check if detailed monitoring is enabled for the EC2 VM.

</td></tr><tr><td>

AWS: IAM Security

</td><td>

Ensure multi-factor authentication \(MFA\) is enabled for all IAM users that have a console password \(Automated\)

</td><td>

IAM User

</td><td>

Multi-Factor Authentication \(MFA\) adds an extra layer of authentication assurance beyond traditional credentials. With MFA enabled, when a user signs in to the AWS Console, they will be prompted for their user name and password as well as for an authentication code from their physical or virtual MFA token. It is recommended that MFA be enabled for all accounts that have a console password.

 Enabling MFA provides increased security for console access as it requires the authenticating principal to possess a device that displays a time-sensitive key and have knowledge of a credential.

</td></tr><tr><td>

 

</td><td>

Ensure credentials unused for 45 days or greater are disabled \(Automated\)

</td><td>

IAM User

</td><td>

AWS IAM users can access AWS resources using different types of credentials, such as passwords or access keys. It is recommended that all credentials that have been unused in 45 or greater days be deactivated or removed

 Disabling or removing unnecessary credentials will reduce the window of opportunity for credentials associated with a compromised or abandoned account to be used.

</td></tr><tr><td>

 

</td><td>

Ensure there is only one active access key available for any single IAM user \(automated\)

</td><td>

IAM User

</td><td>

Access keys are long-term credentials for an IAM user or the AWS account 'root' user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API \(directly or using the AWS SDK\)

 Access keys are long-term credentials for an IAM user or the AWS account 'root' user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API. One of the best ways to protect your account is to not allow users to have multiple access keys.

</td></tr><tr><td>

 

</td><td>

Ensure access keys are rotated every 90 days or less \(automated\)

</td><td>

IAM User

</td><td>

Access keys consist of an access key ID and secret access key, which are used to sign programmatic requests that you make to AWS. AWS users need their own access keys to make programmatic calls to AWS from the AWS Command Line Interface \(AWS CLI\), Tools for Windows PowerShell, the AWS SDKs, or direct HTTP calls using the APIs for individual AWS services.It is recommended that all access keys be regularly rotated.

 Rotating access keys will reduce the window of opportunity for an access key that is associated with a compromised or terminated account to be used.

 Access keys should be rotated to ensure that data cannot be accessed with an old key which might have been lost, cracked, or stolen.

</td></tr><tr><td>

 

</td><td>

Ensure IAM Users Receive Permissions Only Through Groups \(Automated\)

</td><td>

IAM User

</td><td>

IAM users are granted access to services, functions, and data through IAM policies.

 There are three ways to define policies for a user:

1.  Edit the user policy directly, that is an inline, user, policy.
2.  Attach a policy directly to a user.
3.  Add the user to an IAM group that has an attached policy.

 Only the third implementation is recommended.

 Assigning IAM policy only through groups unifies permissions management to a single, flexible layer consistent with organizational functional roles. By unifying permissions management, the likelihood of excessive permissions is reduced.

</td></tr><tr><td>

 

</td><td>

Ensure IAM policies that allow full "\*:\*" administrative privileges are not attached \(Automated\)

</td><td>

IAM User

</td><td>

IAM policies are the means by which privileges are granted to users, groups, or roles. It is recommended and considered a standard security advice to grant least privilege-that is, granting only the permissions required to perform a task. Determine what users need to do and then craft policies for them that let the users perform only those tasks, instead of allowing full administrative privileges.

 It's more secure to start with a minimum set of permissions and grant additional permissions as necessary, rather than starting with permissions that are too lenient and then trying to tighten them later.

 Providing full administrative privileges instead of restricting to the minimum set of permissions that the user is required to do exposes the resources to potentially unwanted actions.

 IAM policies that have a statement with "Effect": "Allow" with "Action": "*" over "Resource": "*" should be removed.

</td></tr><tr><td>

 

</td><td>

Ensure a support role has been created to manage incidents with AWS Support \(Automated\)

</td><td>

IAM User

</td><td>

AWS provides a support center that can be used for incident notification and response, as well as technical support and customer services. Create an IAM Role to allow authorized users to manage incidents with AWS Support.

 By implementing least privilege for access control, an IAM Role will require an appropriate IAM Policy to allow Support Center Access in order to manage Incidents with AWS Support.

</td></tr><tr><td>

 

</td><td>

Ensure that all the expired SSL/TLS certificates stored in AWS IAM are removed \(Automated\)

</td><td>

IAM User

</td><td>

To enable HTTPS connections to your website or application in AWS, you need an SSL/TLS server certificate. You can use ACM or IAM to store and deploy server certificates. Use IAM as a certificate manager only when you must support HTTPS connections in a region that is not supported by ACM. IAM securely encrypts your private keys and stores the encrypted version in IAM SSL certificate storage. IAM supports deploying server certificates in all regions, but you must obtain your certificate from an external provider for use with AWS. You cannot upload an ACM certificate to IAM. Additionally, you cannot manage your certificates from the IAM Console.

 Removing expired SSL/TLS certificates eliminates the risk that an invalid certificate will be deployed accidentally to a resource such as AWS Elastic Load Balancer \(ELB\), which can damage the credibility of the application/website behind the ELB. As a best practice, it is recommended to delete expired certificates.

</td></tr><tr><td>

 

</td><td>

Ensure that IAM Access analyzer is enabled for all regions \(Automated\)

</td><td>

AWS::AccessAnalyzer::Analyzer

</td><td>

Enable IAM Access analyzer for IAM policies about all resources in each region.

 IAM Access Analyzer is a technology introduced at AWS reinvent 2019. After the Analyzer is enabled in IAM, scan results are displayed on the console showing the accessible resources. Scans show resources that other accounts and federated users can access, such as KMS keys and IAM roles. So the results allow you to determine if an unintended user is allowed, making it easier for administrators to monitor least privileges access. Access Analyzer analyzes only policies that are applied to resources in the same AWS Region.

 AWS IAM Access Analyzer helps you identify the resources in your organization and accounts, such as Amazon S3 buckets or IAM roles, that are shared with an external entity. This lets you identify unintended access to your resources and data. Access Analyzer identifies resources that are shared with external principals by using logic-based reasoning to analyze the resource-based policies in your AWS environment. IAM Access Analyzer continuously monitors all policies for S3 bucket, IAM roles, KMS\(Key Management Service\) keys, AWS Lambda functions, and Amazon SQS\(Simple Queue Service\) queues.

</td></tr><tr><td>

 

</td><td>

Ensure no 'root' user account access key exists \(Automated\)

</td><td>

IAM User

</td><td>

The 'root' user account is the most privileged user in an AWS account. AWS Access Keys provide programmatic access to a given AWS account. It is recommended that all access keys associated with the 'root' user account be removed.

 Removing access keys associated with the 'root' user account limits vectors by which the account can be compromised. Additionally, removing the 'root' access keys encourages the creation and use of role based accounts that are least privileged.

</td></tr><tr><td>

 

</td><td>

Ensure MFA is enabled for the 'root' user account \(Automated\)

</td><td>

IAM User

</td><td>

The 'root' user account is the most privileged user in an AWS account. Multi-factor Authentication \(MFA\) adds an extra layer of protection on top of a username and password. With MFA enabled, when a user signs in to an AWS website, they will be prompted for their username and password as well as for an authentication code from their AWS MFA device.

 Enabling MFA provides increased security for console access as it requires the authenticating principal to possess a device that emits a time-sensitive key and have knowledge of a credential.

</td></tr><tr><td>

 

</td><td>

Ensure hardware MFA is enabled for the 'root' user account \(Automated\)

</td><td>

IAM User

</td><td>

The 'root' user account is the most privileged user in an AWS account. MFA adds an extra layer of protection on top of a user name and password. With MFA enabled, when a user signs in to an AWS website, they will be prompted for their user name and password as well as for an authentication code from their AWS MFA device. For Level 2, it is recommended that the 'root' user account be protected with a hardware MFA.

 A hardware MFA has a smaller attack surface than a virtual MFA. For example, a hardware MFA does not suffer the attack surface introduced by the mobile smartphone on which a virtual MFA resides.

</td></tr><tr><td>

 

</td><td>

Eliminate use of the 'root' user for administrative and daily tasks \(Automated\)

</td><td>

IAM User

</td><td>

With the creation of an AWS account, a 'root user' is created that cannot be disabled or deleted. That user has unrestricted access to and control over all resources in the AWS account. It is highly recommended that the use of this account be avoided for everyday tasks.

 The 'root user' has unrestricted access to and control over all account resources. Use of it is inconsistent with the principles of least privilege and separation of duties, and can lead to unnecessary harm due to error or account compromise.

</td></tr><tr><td>

 

</td><td>

Ensure IAM password policy requires minimum length of 14 or greater \(Automated\)

</td><td>

IAM User

</td><td>

Password policies are, in part, used to enforce password complexity requirements. IAM password policies can be used to ensure password are at least a given length. It is recommended that the password policy require a minimum password length 14.

 Setting a password complexity policy increases account resiliency against brute force login attempts.

</td></tr><tr><td>

 

</td><td>

Ensure IAM password policy prevents password reuse \(Automated\)

</td><td>

IAM User

</td><td>

IAM password policies can prevent the reuse of a given password by the same user. It is recommended that the password policy prevent the reuse of passwords.

 Preventing password reuse increases account resiliency against brute force login attempts.

</td></tr><tr><td>

AWS: Data Security

</td><td>

Ensure that S3 Buckets are configured with 'Block public access \(bucket settings\)

</td><td>

AWS::S3::Bucket

</td><td>

Amazon S3 provides Block public access \(bucket settings\)and Block public access \(account settings\)to help you manage public access to Amazon S3 resources. By default, S3 buckets and objects arecreated with public access disabled. However, an IAM principal with sufficient S3 permissions can enable public access at the bucket and/or object level. While enabled, Block public access \(bucket settings\)prevents an individual bucket, and its containedobjects, from becoming publicly accessible. Similarly, Block public access \(account settings\)prevents all buckets, and contained objects, from becoming publicly accessible across the entire account.

 Amazon S3 Block public access \(bucket settings\) prevents the accidental or malicious public exposure of data contained within the respective bucket\(s\).

 Amazon S3 Block public access \(account settings\) prevents the accidental or malicious public exposure of data contained within all buckets of the respective AWS account.

 Whether blocking public access to all or some buckets is an organizational decision that should be based on data sensitivity, least privilege, and use case.

</td></tr><tr><td>

AWS: CloudTrail Logging

</td><td>

Ensure that Object-level logging for write events is enabled for S3 bucket \(Automated\)

</td><td>

AWS::S3::Bucket

</td><td>

S3 object-level API operations such as GetObject, DeleteObject, and PutObject are called data events. By default, CloudTrail trails don't log data events and so it is recommended to

 enable Object-level logging for S3 buckets.

 Rationale:

 Enabling object-level logging will help you meet data compliance requirements within your organization, perform comprehensive security analysis, monitor specific patterns of user

 behavior in your AWS account or take immediate actions on any object-level API activity within your S3 Buckets using Amazon CloudWatch Events.

</td></tr><tr><td>

AWS: CloudTrail Logging

</td><td>

Ensure that Object-level logging for read events is enabled for S3 bucket \(Automated\)

</td><td>

AWS::S3::Bucket

</td><td>

S3 object-level API operations such as GetObject, DeleteObject, and PutObject are called data events. By default, CloudTrail trails don't log data events and so it is recommended to

 enable Object-level logging for S3 buckets.

 Rationale:

 Enabling object-level logging will help you meet data compliance requirements within your organization, perform comprehensive security analysis, monitor specific patterns of user

 behavior in your AWS account or take immediate actions on any object-level API activity using Amazon CloudWatch Events.

</td></tr><tr><td>

AWS: Network Security

</td><td>

Ensure no Network ACLs allow ingress from 0.0.0.0/0 to remote server administration ports \(Automated\)

</td><td>

AWS::EC2::NetworkAcl

</td><td>

The Network Access Control List \(NACL\) function provide stateless filtering of ingress and egress network traffic to AWS resources. It is recommended that no NACL allows unrestricted ingress access to remote server administration ports, such as SSH to port 22and RDP to port 3389.

 Public access to remote server administration ports, such as 22 and 3389, increases resource attack surface and unnecessarily raises the risk of resource compromise.

</td></tr><tr><td>

AWS: Network Security

</td><td>

Ensure no security groups allow ingress from 0.0.0.0/0 to remote server administration ports \(Automated\)

</td><td>

AWS::EC2::SecurityGroup

</td><td>

Security groups provide stateful filtering of ingress and egress network traffic to AWS resources. It is recommended that no security group allows unrestricted ingress access to remote server administration ports, such as SSH to port 22 and RDP to port 3389

 Public access to remote server administration ports, such as 22 and 3389, increases resource attack surface and unnecessarily raises the risk of resource compromise.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

