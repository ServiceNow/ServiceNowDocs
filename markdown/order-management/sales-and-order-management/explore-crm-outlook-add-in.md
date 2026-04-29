---
title: CRM Outlook Add-in
description: The CRM Outlook Add-in helps sales teams capture email interactions into ServiceNow CRM directly from Microsoft Outlook.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Activity Management, Lead and opportunity management, Explore, Sales and Order Management]
---

# CRM Outlook Add-in

The CRM Outlook Add-in helps sales teams capture email interactions into ServiceNow CRM directly from Microsoft Outlook.

## CRM Outlook Add-in overview

The CRM Outlook Add-in application packages the ServiceNow CRM for Outlook add-in, enabling sales teams to capture and log email interactions into ServiceNow CRM without having to leave Microsoft Outlook. Sales representatives can search for CRM records, associate emails with leads, contacts, opportunities, and accounts, and create new records. For high-volume email capture, administrators can configure redirect rules to route emails automatically to their ServiceNow instance without manual association. This ability eliminates context switching between applications, reduces manual data entry, and promotes consistent CRM data for better pipeline visibility and follow-up tracking.

## CRM Outlook Add-in users

|User|Description|
|----|-----------|
|Sales representative|Searches for CRM records, associates emails to track engagement, and creates leads or contacts directly from Outlook.|
|Sales manager|Gains visibility into customer engagement and deal progression through consistently logged email interactions.|
|CRM administrator|Configures the CRM Outlook Add-in plugin, manages user roles, and sets up email redirect rules.|

## CRM Outlook Add-in workflow

The following workflow illustration shows how a sales representative captures an inbound inquiry using the CRM Outlook Add-in.

![Infographic showing how sales representatives use the CRM Outlook add-in to search CRM records, associate emails, and create new leads or contacts. For details, refer to the following description.](../image/crm-outlook-add-in.svg "Capturing email interactions with CRM Outlook Add-in")

1.  As an admin, install the CRM Outlook Add-in.
2.  Deploy the ServiceNow CRM for Outlook add-in using the manifest file.
3.  If useful, configure email client redirecting rules to enable capturing high volume of sales-related inbound emails automatically.
4.  A prospect submits an inquiry through the company website or sends an email directly to a sales representative.
5.  The sales representative receives the email in their Outlook inbox and opens the ServiceNow CRM for Outlook add-in.
6.  The representative searches for existing CRM records matching the sender's name, email, company, or other identifying information.
    -   If a matching record exists, the representative associates the email to the lead, contact, opportunity, or account.
    -   If no matching record exists, the representative creates a lead or contact record and associates the email to that record in one action.

## CRM Outlook Add-in benefits

|Benefits|Feature|Users|
|--------|-------|-----|
|Locate CRM records such as leads, opportunities, accounts, or contacts, and link emails without leaving Outlook.|[Associate an email with an existing CRM record](../task/associate-email-crm-outlook.md)|Sales representative, Sales manager|
|Capture new prospects immediately from inbound inquiries with auto-populated sender information and associate emails in a single action.|[Create a CRM record from Microsoft Outlook](../task/create-crm-entity-outlook.md)|Sales representative|
|Audit and troubleshoot email associations from the Staged Email \[sys\_email\_staging\] table.|[Track emails linked from Microsoft Outlook](../task/view-associated-emails-crm.md)|CRM administrator|
|Capture high volumes of emails automatically without manual logging, reducing missed emails and freeing agents to focus on selling.|[Setting up automatic capture of emails in CRM using redirect rules](using-redirect-rules-crm.md)|CRM administrator|

## What to explore next

To learn more about configuring and using CRM Outlook Add-in, see:

-   [Configuring Activity Management](configuring-activity-management.md)
-   [Using Activity Management](using-activity-management.md)
-   [Activity Management reference](activity-management-reference.md)

