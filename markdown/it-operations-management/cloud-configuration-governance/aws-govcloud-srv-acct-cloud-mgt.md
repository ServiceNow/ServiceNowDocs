---
title: Create a service account for AWS GovCloud
description: If your organization uses AWS GovCloud \(US\) region, you must create a service account in the region where you provision the resources. These credentials that you create are used for Cloud Discovery, Cloud Provisioning and Governance, and Cloud Cost Management.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create AWS GovCloud credentials for Cloud Provisioning and Governance, Day 1 setup guide for Amazon Web Services on Cloud Provisioning and Governance, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a service account for AWS GovCloud

If your organization uses AWS GovCloud \(US\) region, you must create a service account in the region where you provision the resources. These credentials that you create are used for Cloud Discovery, Cloud Provisioning and Governance, and Cloud Cost Management.

## Before you begin

**Note:** Skip this procedure if your organization does not use AWS GovCloud \(US\).

-   Role required: sn\_cmp.cloud\_admin
-   AWS GovCloud \(US\) credentials for each GovCloud region.
-   AWS GovCloud \(US\) account ID \(from the AWS Management Console\).

## About this task

A service account holds the credential and account information that you created in your provider account. Discovery uses the information to access your provider account and then obtain information on each logical datacenter that is associated with the account.

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal** &gt; **Service Accounts**.

2.  Click **New**, enter a unique and descriptive name for the account \(for example, `AWS GovCloud SA O1`\) and then fill in the Cloud Service Account form.

    |Field|Description|
    |-----|-----------|
    |Account ID|Account ID to which this credential belongs.|
    |Discovery credentials|Select the name of the credentials that you created in the [Create AWS GovCloud credentials for Cloud Provisioning and Governance](aws-govcloud-creds-cloud-mgt.md) procedure. In the example, you used the name `AWS GovCloud Creds O1`.|
    |Datacenter URL|URL of the datacenter. For example, [https://ec2.us-gov-west-1.amazonaws.com](https://ec2.us-gov-west-1.amazonaws.com)|
    |Datacenter type|Select the CMDB table that represents the type of datacenter. For example, the \[`cmdb_ci_aws_datacenter`\] table.|
    |Datacenter discovery status|Auto-generated value: Status and timestamp of the last execution of Discovery on the datacenter.|

3.  Click **Update** or **Submit**.

    The system creates the service account and displays the list of all discovered datacenters.


## What to do next

Repeat the process to create additional service accounts as needed. Run Discovery for each datacenter.

