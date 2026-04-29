---
title: Add an AWS GovCloud service account
description: If your organization uses AWS GovCloud \(US\) regions, you create a service account for each region. The credentials that you create during the service account creation, are used for Cloud Discovery and Cloud Cost Management.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Cloud Cost Management for AWS, Configuring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Add an AWS GovCloud service account

If your organization uses AWS GovCloud \(US\) regions, you create a service account for each region. The credentials that you create during the service account creation, are used for Cloud Discovery and Cloud Cost Management.

## Before you begin

Role required: sn\_cmp.cloud\_admin

## About this task

A service account holds the credential and account information that you created in your provider account. A cloud\_admin can add an AWS GovCloud service account. Be sure to set up download jobs for billing and price sheet data for the service account.

## Procedure

1.  Navigate to **All** &gt; **Cloud Provisioning and Governance** &gt; **Cloud Admin Portal** &gt; **Service Accounts**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique and descriptive name for the service account. For example, `AWS GovCloud SA 01`.|
    |Account Id|Account ID to which this credential belongs.|
    |Discovery credentials|Name of the credentials that you created in the [Create an AWS IAM user policy for Cloud Cost Management](aws-user-policy-create-cloudin.md) procedure.|
    |Datacenter URL|URL of the datacenter. For example, [https://ec2.us-gov-west-1.amazonaws.com](https://ec2.us-gov-west-1.amazonaws.com/)|
    |Datacenter Type|The CMDB table that represents the type of datacenter.|
    |Datacenter discovery status|Status and timestamp of the last execution of the Discovery application on the datacenter.|

4.  Select **Submit**.


## Result

The service account gets created and displays the list of all discovered datacenters.

**Related topics**  


[Schedule and manage the jobs that download AWS billing data](aws-bill-dwnld-job-cloudin.md)

[Schedule and manage the Cloud Cost Management jobs that download AWS price sheets](aws-pricesht-sched-dwnld-cloudin.md)

