---
title: Send notification to potentially exposed contacts in a case
description: As a case manager, send an outreach notification to potentially exposed employees to notify them of a potential exposure from an affected employee.
locale: en-US
release: yokohama
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing cases to follow up with potentially exposed contacts, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Send notification to potentially exposed contacts in a case

As a case manager, send an outreach notification to potentially exposed employees to notify them of a potential exposure from an affected employee.

## Before you begin

Ensure that your administrator has created an outreach notification that you can send to potentially exposed contacts in the case. To create an outreach notification, the ServiceNow Emergency Outreach application must be installed and active. For more information, see [Emergency Outreach](../../business-continuity/concept/emergency-outreach.md).

Role required: sn\_imt\_tracing.case\_manager

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Case Management** &gt; **Cases Assigned to Me**.

2.  Open a case to send a notification to potentially exposed contacts.

3.  In the Exposed Contacts related list, select the employees to whom you want to send a notification.

    If required, you can send a notification to a contact more than once.

4.  In the Actions on selected rows list, select **Send Exposure Notice**.

5.  In the Send Exposure Notice dialog box, select an outreach notification, and click **Send**.


## Result

An email notification is sent to the selected contacts. The **Notice sent date** column for the selected contacts in the Exposed Contacts list updates to the current date.

You can review the notifications by navigating to **Emergency Outreach** &gt; **View Outreaches** and open the outreach notification.

## What to do next

[Create a case task for each exposed contact](create-task-exposed-contact.md).

**Parent Topic:**[Managing cases to follow up with potentially exposed contacts](../concept/exposure-case-management.md)

