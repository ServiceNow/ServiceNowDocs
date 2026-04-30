---
title: Configure Twilio to send notifications in SRM
description: Establish a connection between your SRM instance and your Twilio account so your teams can receive notifications.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Configure Twilio to send notifications in SRM

Establish a connection between your SRM instance and your Twilio account so your teams can receive notifications.

## Before you begin

Before you begin, you must have a SID and authentication token for an active Twilio account.

**Note:** Performing this action requires advanced ServiceNow expertise.

Role required: admin

## About this task

You can adjust what gets sent from Twilio by editing the on-call workflow in the system.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Select **Service Reliability Management.**

3.  Under **Integrations**, select **Twilio API Key**.

4.  Select **Twilio Config**.

5.  In the new window, select the **here** link to edit the record.

    ![Select here to edit the record.](../image/sr-twilio-edit.png)

6.  Enter the **Account SID** value.

7.  Enter a **Validity Period** value.

8.  Select **Connect** to activate the key or **Save** to save your changes without activating.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Approve a change request for SRM team approval](sr-approve-change-req.md)

**Next topic:**[Install the Alert automation rules application](sr-install-aa-store-app.md)

