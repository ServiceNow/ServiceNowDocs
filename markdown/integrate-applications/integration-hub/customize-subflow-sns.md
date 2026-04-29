---
title: Customize event management
description: Customize the management of events \(Notification, Subscription Confirmation, and Unsubscribe Confirmation\) you receive for your ServiceNow instance from Amazon SNS.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Amazon SNS Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Customize event management

Customize the management of events \(Notification, Subscription Confirmation, and Unsubscribe Confirmation\) you receive for your ServiceNow instance from Amazon SNS.

## Before you begin

Role required: admin.

## Procedure

1.  In Workflow Studio, create a copy of the default subflow, Amazon SNS Subscription and customize the subflow as per your requirement.

    For more information about creating subflows, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

2.  Copy and record the internal name of the customized subflow.

3.  Navigate to **AWS Configuration** &gt; **All Configurations**.

4.  Open the record you had created to receive events.

    In this record, the internal name of the default Amazon SNS Subscription subflow is specified in **Property Value**.

5.  Update this record by replacing the internal name of default subflow with the internal name of the customized subflow in **Property Value**.

    **Note:** Use the same **Client Secret**.


## Result

The event management is customized as per your requirement.

