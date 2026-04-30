---
title: Setting up AWS service accounts
description: Create and configure cloud service accounts at ServiceNow AI Platform for the corresponding Amazon Web Services \(AWS\) service accounts.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up a cloud service account, Access to cloud environments for ITOM products, IT Operations Management]
---

# Setting up AWS service accounts

Create and configure cloud service accounts at ServiceNow AI Platform for the corresponding Amazon Web Services \(AWS\) service accounts.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

Ensure that you are familiar with the hierarchy of AWS service accounts in your environment. For example, if there are AWS Organizations, set up the management and member accounts at ServiceNow AI Platform to reflect that hierarchy. You can set up the AWS service accounts of the following types:

-   **Discrete account**: Standalone account, with no management account.
-   **Management account**: Management account that may or may not contain member accounts \(subaccounts\).

    **Note:** Some ServiceNow UI screens may refer to management accounts as master accounts.

-   **Member account**: Subaccount that belongs with the \(management\) account.

-   **[Access setup for AWS service accounts](access-aws-accounts.md)**  
Cloud Discovery and Cloud Provisioning and Governance need access to resources in the Amazon Web Services \(AWS\) service accounts. Learn about different methods of configuring such access.
-   **[Configure access to the AWS accounts using permanent AWS credentials](../task/aws-create-creds-cloud-mgt.md)**  
To securely access data on your provider account, the Discovery process must present appropriate credentials. To make the credentials available to Discovery and Cloud Provisioning and Governance, you first create a user with programmatic access in the AWS Management Console. You then securely store the credentials in a service account at ServiceNow AI Platform.
-   **[Create AWS service accounts](../task/create-aws-service-accounts.md)**  
Create AWS service accounts on the ServiceNow AI Platform to access your AWS account during AWS discovery.
-   **[Configure access using temporary credentials based on trusted AWS accounts with AWS credentials](../task/configure-iam-role-aws-account.md)**  
Configure the trusting account whose resources need to be accessed, to rely on the trusted account using the Identity and Access Management \(IAM\) role.
-   **[Configure access using temporary credentials based on trusted AWS accounts without AWS credentials](../task/aws-trusted-credential-less.md)**  
Set up a trusted credential-less account that other AWS accounts can rely on for access.
-   **[Configure access using temporary credentials for trusting AWS member accounts in management-accessor trust chain](../task/configure-iam-role-aws-member.md)**  
Configure access for AWS member accounts by using a trust chain from the accessor through the management account.
-   **[Configure the MID Server for AWS IAM roles](../task/config-mid-iam-roles.md)**  
Configure the MID Server to retrieve the temporary security credentials associated with an IAM role.
-   **[Control AWS access and permissions using policies](../task/aws-create-user-policy-cloud-mgt.md)**  
Configure policies with the necessary level of permissions to provide access to the AWS resources for Cloud Discovery and Cloud Provisioning and Governance.

**Parent Topic:**[Set up a cloud service account](setup-cloud-service-account.md)

