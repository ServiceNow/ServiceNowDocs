---
title: Create a CRM record from Microsoft Outlook
description: Create a new lead or contact record and associate an email with it directly from Microsoft Outlook, enabling you to capture new prospects without having to leave your email inbox.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/create-crm-entity-outlook.html
release: australia
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 2
keywords: [ServiceNow CRM for Outlook, create lead, create contact, create and associate]
breadcrumb: [Activity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Create a CRM record from Microsoft Outlook

Create a new lead or contact record and associate an email with it directly from Microsoft Outlook, enabling you to capture new prospects without having to leave your email inbox.

## Before you begin

Write permission on the underlying CRM entity table is required to view the corresponding tab in the ServiceNow CRM for Outlook Add-in and to create or associate records on that tab. For example, to associate an email with a LEAD record, you must have write permission on the Lead \[sn\_lead\_mgmt\_core\_lead\] table.

Your admin can grant you this write permission in either of these ways: directly through table ACLs, or through the responsibility framework. The responsibility framework grants you access to specific records based on your role and your membership. For more information, see [Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_CreateAResponsibilityDefinition.md).

Role required: sn\_crm\_outlook.crm\_outlook\_user

## Procedure

1.  Open an email in Microsoft Outlook.

2.  Load the Microsoft Outlook add-in by selecting **ServiceNow CRM for Outlook** from the Microsoft Outlook ribbon.

3.  If a sign-in form appears, enter your credentials and select **Log in**.

4.  Select a record type from the **Create new** drop-down menu.

    |Record type|Description|
    |-----------|-----------|
    |**Lead**|New lead record for a potential customer who has shown interest but is not yet qualified. For a description of the field values, see [Lead form in the ServiceNow CRM for Outlook add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/lead-fields-outlook.md).|
    |**Contact**|New contact record for an individual associated with an existing or new account. For a description of the field values, see [Contact form in the ServiceNow CRM for Outlook add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/contact-fields-outlook.md).|

    When you create a Lead or Contact from a sent email, the form populates with the first recipient's first name, last name, and domain. For received emails, the form is populated with the sender’s details.

5.  Complete the required fields and any optional fields relevant to your workflow.

6.  Select **Create and associate**.


## Result

The CRM record is created and the email association is logged, enabling you to continue engagement tracking from either Microsoft Outlook or CSM/FSM Configurable Workspace.

## What to do next

You can view the associated emails from the respective entity record's Emails tab. For more information, see [Track emails linked from Microsoft Outlook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-associated-emails-crm.md).

**Parent Topic:**[Using Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-activity-management.md)

**Related topics**  


[Configuring Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-activity-management.md)

[Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-activity-management.md)

