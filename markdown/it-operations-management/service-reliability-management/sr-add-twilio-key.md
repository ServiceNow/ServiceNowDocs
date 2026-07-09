---
title: Configure Twilio to send notifications in SRM
description: Connect your Service Reliability Management \(SRM\) instance and Twilio account to send notifications to teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-reliability-management/sr-add-twilio-key.html
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


**Parent Topic:**[Configuring Service Reliability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-reliability-management/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store]()

[Assign an administrator to Service Reliability Management]()

[Activate teams and services in SRM]()

[Customize service approval settings]()

[Customize team approval settings]()

[Configure error budget actions for breached SRM SLOs]()

[Approve a change request for SRM]()

[Configure fields for escalation triggers]()

[Install the Alert Automation application]()

