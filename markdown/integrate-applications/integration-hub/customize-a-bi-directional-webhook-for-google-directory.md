---
title: Set up a bi-directional webhook for the Google Directory spoke
description: Create a webhook routing policy and subflow according to your requirement.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Google Directory Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up a bi-directional webhook for the Google Directory spoke

Create a webhook routing policy and subflow according to your requirement.

## Before you begin

Role required: admin

## About this task

The default routing policy in the Google Directory WebHook Routing Policies module triggers the Process Google Directory User Webhook Subflow and notifies the ServiceNow app when certain events occur in the Google Directory. To use any other fields in your custom subflow and customize conditions in the routing policy, perform these steps.

## Procedure

1.  Navigate to **All** &gt; **Flow Designer**.

2.  Select Subflows.

3.  In the name field, enter `Process Google Directory User Webhook Subflow` and press **Enter**.

4.  Select the subflow.

5.  On the Process Google Directory User Webhook Subflow page, select the More Actions Menu icon \(![More Actions Menu icon.](../image/flow-copy-icon.png)\).

6.  Select **Copy Subflow**.

7.  Customize the subflow according to your requirement and publish it.

8.  In the filter field, enter `Google Directory Webhook Routing Policies`.

9.  Select **New**.

10. Fill the form.

    |Field|Description|
    |-----|-----------|
    |Label|A unique label to identify the routing policy.|
    |Application|The application is set to Global.|
    |Order|The order in which the request is processed.|
    |Answer|Subflow that must be triggered when the specified conditions are met.|
    |Default answer|Option to specify if the answer is the default answer.|
    |Condition|Conditions to be met when the required events occur in the Google Directory.|

11. Select **Submit**.


