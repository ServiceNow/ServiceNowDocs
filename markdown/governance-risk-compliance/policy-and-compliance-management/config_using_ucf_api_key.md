---
title: Configure the UCF integration using a UCF-supplied API key
description: UCF integrates with your ServiceNow instance through an authentication process which validates your subscription.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage the UCF integration, Use the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Configure the UCF integration using a UCF-supplied API key

UCF integrates with your ServiceNow instance through an authentication process which validates your subscription.

## Before you begin

Role required: admin

## About this task

Prior to configuring the UCF integration, you need a UCF basic subscription and use the API Key Manager in your account to acquire an API key from UCF. You must also define shared lists of UCF authority documents in your account.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Unified Compliance Integration**.

2.  Click the UCF configuration.

    ![UCF Configuration](../image/ucf-config.png)

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Shared List|Select the shared list from your UCF account.|
    |Authentication type|Select **API Key**.|
    |API Key|Enter the API key you acquired from your UCF account.|

4.  Click **Save Configuration**.


**Parent Topic:**[Manage the UCF integration](../concept/manage_compliance_frameworks.md)

