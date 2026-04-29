---
title: Control AWS access and permissions using policies
description: I have reworked this topic to fit the new accessibility configuration structure. Per our discussion, please remove this topic from the CPG map and add a reference to the new access configuration anchor \(./../discovery/concept/access-aws-accounts.dita\) to the AWS Day 1 landing page. Configure policies with the necessary level of permissions to provide access to the AWS resources for Cloud Discovery and Cloud Provisioning and Governance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up AWS service accounts, Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Control AWS access and permissions using policies

Configure policies with the necessary level of permissions to provide access to the AWS resources for Cloud Discovery and Cloud Provisioning and Governance.

## Before you begin

Familiarize yourself with creating IAM users and user policies. Refer to the [AWS documentation](https://aws.amazon.com/documentation/).

Identify the level of permissions required for discovering the resources using Cloud Discovery and managing the resources with Cloud Provisioning and Governance. For example:

-   Additional S3 permissions are needed as AWS uses an S3 bucket to store and run the cloud formation templates to deploy stacks using CloudFormation. These permissions are needed even if you run the same CloudFormation template from the AWS console.
-   Read-only access is required to do pattern discovery with the custom policy.

AWS CloudFormation provisions and configures resources by making calls to the AWS services that are described in your template. For more information, see [How does CloudFormation work?](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-whatis-howdoesitwork.html)

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

Roles required:

-   AWS Management Console administrator
-   For Cloud Discovery: discovery\_admin
-   For Cloud Provisioning and Governance: admin or sn\_cmp.cloud\_admin

## About this task

The policy you configure defines the AWS permissions that you can assign to a user, group, or a role. Depending on the AWS services you use, specify actions for the service to perform discovery and provisioning and life-cycle actions using Cloud Provisioning and Governance.

## Procedure

1.  Log in to the AWS Management Console using the credentials of the relevant service account.

    If you used an IAM user or an IAM role to provide access using temporary credentials, log in using the same IAM user or IAM role.

2.  Open the user record in the instance for the relevant user.

3.  Define a user policy in AWS Management Console using either of the following methods:

    -   Grant administrator access to the instance. This method gives the same level of access as using the Access Key ID and Secret Access Key gives. Attach the `AdministratorAccess` policy to the user profile.

        **Note:** To create a user policy that supports only Cloud Discovery rather than the provisioning of cloud resources, attach the `ReadOnlyAccess` policy instead.

    -   Create a custom policy with a descriptive name. In the Policy Document field, write the code that includes the APIs that this policy allows running.

        **Note:** The following JSON sample is a partial example showing permissions for Cloud Discovery. It isn't a complete list of all required permissions.

        ```
        {
           "Version":"2012-10-17",
           "Statement":[
              {
                 "Sid":"PermissionsNeededForDiscovery",
                 "Effect":"Allow",
                 "Action":[
                    "account:ListRegions",
                    "apigateway:GET",
                    "application-autoscaling:Describe*",
                    "autoscaling-plans:Describe*",
                    "autoscaling:Describe*",
                    "autoscaling:DescribeAutoScalingGroups",
                    "autoscaling:DescribeLaunchConfigurations",
                    "cloudformation:Describe*",
                    "cloudformation:DescribeStack*",
                    "cloudformation:List*",
                    "cloudwatch:Get*",
                    "cloudwatch:List*",
                    "config:ListDiscoveredResources",
                    "dynamodb:Describe*",
                    "dynamodb:DescribeTable",
                    "dynamodb:ListGlobalTables",
                    "dynamodb:ListTables",
                    "ec2:Describe*",
                    "ec2:ReportInstanceStatus",
                    "ecs:Describe*",
                    "ecs:List*",
                    "eks:Describe*",
                    "eks:List*",
                    "elasticache:Describe*",
                    "elasticache:List*",
                    "elasticfilesystem:Describe*",
                    "elasticloadbalancing:Describe*",
                    "lambda:Get*",
                    "lambda:List*",
                    "organizations:Describe*",
                    "organizations:DescribeOrganization",
                    "organizations:List*",
                    "rds:Describe*",
                    "redshift:Describe*",
                    "route53:GetHostedZone",
                    "route53:List*",
                    "s3:GetAccountPublicAccessBlock",
                    "s3:GetBucket*",
                    "s3:GetBucketLocation",
                    "s3:List*",
                    "sdb:GetAttributes",
                    "sns:GetEndpointAttributes",
                    "sns:GetSubscriptionAttributes",
                    "sns:List*",
                    "sns:ListPlatformApplications",
                    "sns:ListSubscriptions",
                    "sns:ListSubscriptionsByTopic",
                    "sns:ListTopics"
                 ],
                 "Resource":"*"
              }
           ]
        }
        ```

    -   The following JSON sample is a partial example showing permissions for Cloud Discovery and Cloud Provisioning and Governance. It isn't a complete list of all required permissions.

        ```
        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Sid": "PermissionsNeededForCPG",
                    "Effect": "Allow",
                    "Action": [
                        "account:ListRegions",
                        "apigateway:GET",
                        "application-autoscaling:Describe*",
                        "autoscaling-plans:Describe*",
                        "autoscaling:Describe*",
                        "autoscaling:DescribeAutoScalingGroups",
                        "autoscaling:DescribeLaunchConfigurations",
                        "cloudformation:Describe*",
                        "cloudformation:DescribeStack*",
                        "cloudwatch:Get*",
                        "cloudwatch:List*",
                        "config:ListDiscoveredResources"
                        "dynamodb:Describe*",
                        "dynamodb:DescribeTable",
                        "dynamodb:ListGlobalTables",
                        "dynamodb:ListTables",
                        "ec2:Describe*",
                        "ec2:ReportInstanceStatus",
                        "ecs:Describe*",
                        "ecs:List*",
                        "eks:Describe*",
                        "eks:List*",
                        "elasticache:Describe*",
                        "elasticache:List*",
                        "elasticfilesystem:Describe*",
                        "elasticloadbalancing:Describe*",
                        "lambda:Get*",
                        "lambda:List*",
                        "organizations:Describe*",
                        "organizations:DescribeOrganization",
                        "organizations:List*",
                        "rds:Describe*",
                        "redshift:Describe*",
                        "route53:GetHostedZone",
                        "route53:List*",
                        "s3:GetAccountPublicAccessBlock",
                        "s3:GetBucket*",
                        "s3:GetBucketLocation",
                        "s3:List*",
                        "sdb:GetAttributes",
                        "sns:GetEndpointAttributes",
                        "sns:GetSubscriptionAttributes",
                        "sns:List*",
                        "sns:ListPlatformApplications",
                        "sns:ListSubscriptions",
                        "sns:ListSubscriptionsByTopic",
                        "sns:ListTopics"
                    ],
                    "Resource": "*"
                },
                {
                    "Sid": "MinimalPermissionsNeededForEc2ProvisioningThroughCloudFormation",
                    "Effect": "Allow",
                    "Action": [
                        "cloudformation:CreateStack",
                        "cloudformation:CreateUploadBucket",
                        "cloudformation:DeleteStack",
                        "cloudformation:DescribeStackEvents",
                        "cloudformation:DescribeStackResources",
                        "cloudformation:DescribeStacks",
                        "cloudformation:GetTemplate",
                        "cloudformation:GetTemplateSummary",
                        "cloudformation:List*",
                        "cloudformation:UpdateStack",
                        "cloudformation:ValidateTemplate"
                        "ec2:*",
                        "s3:CreateBucket",
                        "s3:DeleteBucket",
                        "s3:DeleteObject",
                        "s3:GetObject",
                        "s3:ListBucket",
                        "s3:PutObject"
                    ],
                    "Resource": "*"
                }
            ]
        }
        ```


**Parent Topic:**[Setting up AWS service accounts](../concept/setup-aws-service-accounts.md)

**Related topics**  


[https://docs.aws.amazon.com/IAM/latest/UserGuide/access\_policies\_create-console.html\#access\_policies\_create-start](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_create-console.html#access_policies_create-start)

[https://docs.aws.amazon.com/IAM/latest/UserGuide/access\_policies\_understand-service-summary.html](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_understand-service-summary.html)

