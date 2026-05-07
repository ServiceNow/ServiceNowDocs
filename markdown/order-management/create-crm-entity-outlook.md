---
title: Create a CRM record from Microsoft Outlook
description: Create a new lead or contact record and associate an email to it directly from Microsoft Outlook, enabling you to capture new prospects without having to leave your email inbox.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow CRM for Outlook, create lead, create contact, create and associate]
breadcrumb: [Activity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Create a CRM record from Microsoft Outlook

Create a new lead or contact record and associate an email to it directly from Microsoft Outlook, enabling you to capture new prospects without having to leave your email inbox.

## Before you begin

Role required: sn\_crm\_outlook.crm\_outlook\_user

## Procedure

1.  Open an email in Microsoft Outlook.

2.  Load the Microsoft Outlook add-in by selecting **ServiceNow CRM for Outlook** from the Microsoft Outlook ribbon.

3.  If you're logged out, select **Log in** and enter your credentials.

    The add-in displays tabs for Leads, Accounts, Contacts, and More \(which includes Opportunities\).

4.  Select a record type from the **Create new** drop-down menu.

    |Record type|Description|
    |-----------|-----------|
    |**Lead**|New lead record for a potential customer who has shown interest but is not yet qualified. For a description of the field values, see [Lead form in the ServiceNow CRM for Outlook add-in](../reference/lead-fields-outlook.md).|
    |**Contact**|New contact record for an individual associated with an existing or new account. For a description of the field values, see [Contact form in the ServiceNow CRM for Outlook add-in](../reference/contact-fields-outlook.md).|

5.  Complete the required fields and any optional fields relevant to your workflow.

6.  Select **Create and associate**.


## Result

The CRM record is created and the email association is logged, enabling you to continue engagement tracking from either Microsoft Outlook or CSM/FSM Configurable Workspace.

## What to do next

You can view the associated emails if you have the staging\_emails\_admin role. For more information, see [Track emails linked from Microsoft Outlook](view-associated-emails-crm.md).

**Parent Topic:**[Using Activity Management](../concept/using-activity-management.md)

