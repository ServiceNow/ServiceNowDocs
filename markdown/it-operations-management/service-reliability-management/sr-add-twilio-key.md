---
title: Configure Twilio to send notifications in SRM
description: Connect your Service Reliability Management \(SRM\) instance and Twilio account to send notifications to teams.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Configure Twilio to send notifications in SRM

Connect your Service Reliability Management \(SRM\) instance and Twilio account to send notifications to teams.

## Before you begin

Before you begin, you must have a String Identifier \(SID\) and an authentication token for an active Twilio account.

**Note:** Performing this action requires ServiceNow expertise.

Role required: srm\_admin or admin

## About this task

You can adjust what gets sent from Twilio by editing the on-call workflow in the system.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  Select **Service Reliability Management** &gt; **Integrations** &gt; **Twilio API Key**.

3.  Select **Twilio Config**.

4.  In the new window, select **here** to edit the record.

5.  Enter the **Account SID** value.

6.  Enter a **Validity Period** value.

7.  Select **Connect** to activate the key or **Save** to save your changes without activating.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store](sr-install-sr-store-app.md)

[Assign an administrator to Service Reliability Management](sr-assign-admins.md)

[Activate teams and services in SRM](sr-activate-teams-and-services-in-srm.md)

[Customize service approval settings in SRM](sr-add-approval-services.md)

[Customize team approval settings in SRM](sr-add-approval-teams.md)

[Configure error budget actions for breached SRM SLOs](sr-configure-error-budget.md)

[Approve a change request for SRM](sr-approve-change-req.md)

[Configure fields for escalation triggers](srm-configure-trigger-fields.md)

[Install the Alert Automation application](sr-install-aa-store-app.md)

