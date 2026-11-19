---
title: Setting up AWS cloud
description: This section covers all the topics required to set up AWS cloud. The topics are arranged based on configuration priority.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/setting-up-aws-cloud.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Set up AWS cloud with Cloud Workspace]
breadcrumb: [Configuring cloud providers, Configure, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Setting up AWS cloud

This section covers all the topics required to set up AWS cloud. The topics are arranged based on configuration priority.

AWS setup begins with the setup of the root email and an IAM account for ServiceNow. The most important steps are the AWS side account and IAM setup:

1.  Verifying the root email.
2.  Creating an IAM user ideally using a CloudFormation template in the management account.
3.  Creating the cloud account and service account in ServiceNow with the correct credentials and management-account link.

Everything downstream, including provisioning, scanning, and certification, depends on these being right. The AWS configuration steps require the AWS administrator role in the AWS Management Console. A ServiceNow AI Platform Admin completes the ServiceNow-side steps. These steps include populating dependent tables, configuring scans for data visualization, and reviewing the default certification policy.

-   **[Setting up a root email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/setting-up-root-email.md)**  
The app creates accounts with a unique request ID and root email, promoting distinct emails for each account and simplifying management.
-   **[Set up an IAM account for a ServiceNow user in AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/set-up-iam-account-in-aws.md)**  
AWSCreate an AWS CloudFormation Identity Access Manager \(IAM\) user in the management account using the CloudFormation template \(CFT\). This allows you to manage multiple AWS accounts with a centralized IAM user.
-   **[Set up an Identity Access Manager in AWS GovCloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/set-up-iam-account-in-aws-govcloud.md)**  
Create AWS CloudFormation Identity Access Manager \(IAM\) resources for three AWS account types in the management account. Use CloudFormation templates \(CFT\) to integrate ServiceNow Cloud Account management \(CAM\) with AWS GovCloud.
-   **[Configuring Service Control Policy in AWS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/about-service-control-policy.md)**  
The AWS admin configures a Service Control Policy \(SCP\) and shares its ID with the ServiceNow AI Platform admin for Cloud Account Management setup. Cloud Account Management enforces the SCP via API calls to block resource creation in the account.

**Parent Topic:**[Configuring cloud providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configuring-cloud.md)

