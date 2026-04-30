---
title: Create an assume role configuration
description: Create a service account assume role configuration to facilitate cross-account access that is from a management account to a member account or from a trusted account to a trusting account.
locale: en-US
release: yokohama
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Cloud Configuration Governance for AWS, Exploring Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create an assume role configuration

Create a service account assume role configuration to facilitate cross-account access that is from a management account to a member account or from a trusted account to a trusting account.

## Before you begin

Make sure that the accessor account credentials are configured in the ServiceNow AI Platform.

Role required: sn\_itom\_ccg.scheduling\_admin

## About this task

If permanent credentials aren't defined for the member account, Cloud Configuration Governance checks the Cloud Service Account Assume Role Config \[sn\_itom\_ccg\_service\_account\_assume\_role\_config\] table to identify the special configuration associated with the management account, and then uses the management account credentials to generate temporary credentials for the member accounts. If the configuration exists in the table, Cloud Configuration Governance uses the temporary credentials acquired by specifying a role and its configuration in the Amazon Web Services \(AWS\) Security Token Services API AssumeRole action.

## Procedure

1.  Navigate to **All** &gt; **Cloud Configuration Governance** &gt; **Assume Role Config**.

2.  Select **New**.

3.  Fill the values on the Service Account Assume Role Config form.

    For a description of the form fields, see [Cloud Configuration Governance Service Account Assume Role Config form](../../itom-cloud-accelerate/reference/ccg-service-account-assume-role-config-form.md).

4.  Select **Submit**.


**Parent Topic:**[Set up Cloud Configuration Governance for AWS](../../itom-cloud-accelerate/task/set-up-ccg-for-aws.md)

