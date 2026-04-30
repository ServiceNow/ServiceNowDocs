---
title: Initiate conference call on incident communication task
description: Initiate a conference call and include all the required stakeholders to discuss on the resolution of the incident and the communication task.
locale: en-US
release: yokohama
product: Incident Communications Management
classification: incident-communications-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage, Incident Communications Management, IT Service Management]
---

# Initiate conference call on incident communication task

Initiate a conference call and include all the required stakeholders to discuss on the resolution of the incident and the communication task.

## Before you begin

Role required: sn\_comm\_management.comm\_plan\_manager or sn\_comm\_management.comm\_plan\_admin

Activate the Notify plugin \(com.snc.notify\), configure the Twilio account, configure the **com.snc.iam.notify\_number** property and create a default provider selector. You can also create a provider selector on the Incident Communication Task table \[incident\_alert\_task\]. The provider selector specifies the Notify group containing the Notify phone numbers or conference provider to make outgoing calls.

## Procedure

1.  Navigate to **Incident** &gt; **All**.

2.  Open an incident record.

3.  From the Incident Communication Plan related list, open the incident communication plan.

4.  From the Incident Communication Tasks related list, open the incident communication task.

5.  In the related link, click **Initiate Conference Call**.

6.  Select the conference bridge number and the participants for the conference call and click **Start Call**.


**Parent Topic:**[Managing Incident Communications](../concept/working-with-inci-comm-mgmt.md)

