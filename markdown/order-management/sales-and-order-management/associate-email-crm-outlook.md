---
title: Associate an email with an existing CRM record
description: Link an email to an existing lead, account, contact, or opportunity record directly from Microsoft Outlook. Associating emails with CRM records helps maintain a complete engagement history without having to switch between applications.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ServiceNow CRM for Outlook, associate email, link email, log email]
breadcrumb: [Activity Management, Lead and opportunity apps, Use, Sales and Order Management]
---

# Associate an email with an existing CRM record

Link an email to an existing lead, account, contact, or opportunity record directly from Microsoft Outlook. Associating emails with CRM records helps maintain a complete engagement history without having to switch between applications.

## Before you begin

Role required: sn\_crm\_outlook.crm\_outlook\_user

## Procedure

1.  Open an email in Microsoft Outlook.

2.  Load the Microsoft Outlook add-in by selecting **ServiceNow CRM for Outlook** from the Microsoft Outlook ribbon.

3.  If you're logged out, select **Log in** and enter your credentials.

4.  Select a tab for the record type you want to search.

    -   Leads
    -   Account
    -   Contacts
    -   More &gt; Opportunities
5.  In the **Filters** field, set filters to narrow results.

    For example, to find a lead by email address, you would set the condition **\[Email\] \[is\] \[**&lt;email address to search for&gt;**\]**.

6.  In the **Search** field, enter the search information such as a name or email address.

7.  Locate the record you want to associate and select **Associate**.

    The email is linked to the CRM record. The association appears in the record's activity history in ServiceNow CRM.

8.  Enter additional information for your selected CRM entity, and select **Save**.

    For more information about the form fields for the CRM entities, refer to the corresponding topic.

    |CRM entity|Form field descriptions|
    |----------|-----------------------|
    |**Lead**|[Lead form in the ServiceNow CRM for Outlook add-in](../reference/lead-fields-outlook.md)|
    |**Opportunity**|[Opportunity form in the ServiceNow CRM for Outlook add-in](../reference/opportunity-fields-outlook.md)|
    |**Account**|[Account form in the ServiceNow CRM for Outlook add-in](../reference/account-fields-outlook.md)|
    |**Contact**|[Contact form in the ServiceNow CRM for Outlook add-in](../reference/contact-fields-outlook.md)|

9.  View the associated record in the CRM by selecting **Open**.

    You're redirected to the entity record in the CSM/FSM Configurable Workspace.


## Result

The email is associated with the CRM record, and the engagement is logged for future reference.

## What to do next

You can view the associated emails if you have the staging\_emails\_admin role. For more information, see [Track emails linked from Microsoft Outlook](view-associated-emails-crm.md).

**Parent Topic:**[Using Activity Management](../concept/using-activity-management.md)

