---
title: Associate an email with an existing CRM record
description: Link an email to an existing lead, account, contact, or opportunity record directly from Microsoft Outlook. Associating emails with CRM records helps maintain a complete engagement history without having to switch between applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/associate-email-crm-outlook.html
release: australia
topic_type: task
last_updated: "2026-06-08"
reading_time_minutes: 3
keywords: [ServiceNow CRM for Outlook, associate email, link email, log email]
breadcrumb: [Activity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Associate an email with an existing CRM record

Link an email to an existing lead, account, contact, or opportunity record directly from Microsoft Outlook. Associating emails with CRM records helps maintain a complete engagement history without having to switch between applications.

## Before you begin

Write permission on the underlying CRM entity table is required to view the corresponding tab in the ServiceNow CRM for Outlook Add-in and to create or associate records on that tab. For example, to associate an email with a LEAD record, you must have write permission on the Lead \[sn\_lead\_mgmt\_core\_lead\] table.

Your administrator can grant you this write permission in either of these ways: directly through table ACLs, or through the responsibility framework. The responsibility framework grants you access to specific records based on your role and your membership. For more information, see [Create a responsibility definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/t_CreateAResponsibilityDefinition.md).

Role required: sn\_crm\_outlook.crm\_outlook\_user

## About this task

Use these steps to associate any email in your inbox or sent folder. You stay in control of which emails are captured in ServiceNow CRM. Only the emails you choose to open in the ServiceNow CRM for Outlook add-in are associated.

**Note:** If an email belongs to a thread where you've already associated one message, the ServiceNow CRM for Outlook add-in shows the matched CRM record directly when you launch it. You don't need to search for the record or select **Associate** again. You can skip straight to the optional steps to add details or open the record in CRM.

## Procedure

1.  Open an email in Microsoft Outlook.

2.  Load the Microsoft Outlook add-in by selecting **ServiceNow CRM for Outlook** from the Microsoft Outlook ribbon.

3.  If a sign-in form appears, enter your credentials and select **Log in**.

4.  Select a tab for the record type you want to search.

    -   **Leads**
    -   **Account**
    -   **Contacts**
    -   **More** &gt; **Opportunities**
5.  In the **Filters** field, set filters to narrow results.

    The CRM Outlook Add-in extracts the sender's name and email domain or the first recipient's name and domain, for sent emails, and matches them against the following fields per entity:

    -   Leads and opportunities: first name, last name, and email domain
    -   Accounts and contacts: email domain only
    Records matching any of these fields appear in the corresponding tab. The first two recipient addresses are considered for matching.

    For example, to find a lead by email address, set the condition **\[Email\] \[is\] \[**&lt;email address to search for&gt;**\]**.

6.  In the **Search** field, enter the search information such as a name or email address.

7.  Locate the record you want to associate and select **Associate**.

    If the email is part of a thread you've already associated, the matched record card appears automatically. You don't need to perform this step.

    The email is linked to the CRM record. The association appears in the record's activity history in ServiceNow CRM.

8.  Enter additional information for your selected CRM entity, and select **Save**.

    For more information about the form fields for the CRM entities, refer to the corresponding topic.

    |CRM entity|Form field descriptions|
    |----------|-----------------------|
    |**Lead**|[Lead form in the ServiceNow CRM for Outlook add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/lead-fields-outlook.md)|
    |**Opportunity**|[Opportunity form in the ServiceNow CRM for Outlook add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/opportunity-fields-outlook.md)|
    |**Account**|[Account form in the ServiceNow CRM for Outlook add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/account-fields-outlook.md)|
    |**Contact**|[Contact form in the ServiceNow CRM for Outlook add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/contact-fields-outlook.md)|

9.  View the associated record in the CRM by selecting **Open**.

    You're redirected to the entity record in the CSM/FSM Configurable Workspace.


## Result

The email is associated with the CRM record, and the engagement is logged for future reference.

## What to do next

You can view the associated emails from the respective entity record's Emails tab. For more information, see [Track emails linked from Microsoft Outlook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-associated-emails-crm.md).

**Parent Topic:**[Using Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-activity-management.md)

**Related topics**  


[Configuring Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-activity-management.md)

[Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-activity-management.md)

