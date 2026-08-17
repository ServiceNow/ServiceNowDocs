---
title: CRM Outlook Add-in
description: The CRM Outlook Add-in helps sales teams capture email interactions into ServiceNow CRM directly from Microsoft Outlook.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/explore-crm-outlook-add-in.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Activity Management, Sales automation, Explore, Sales Customer Relationship Management]
---

# CRM Outlook Add-in

The CRM Outlook Add-in helps sales teams capture email interactions into ServiceNow CRM directly from Microsoft Outlook.

## CRM Outlook Add-in overview

The CRM Outlook Add-in application packages the ServiceNow CRM for Outlook add-in, enabling sales teams to capture and log email interactions into ServiceNow CRM without having to leave Microsoft Outlook. Sales representatives can search for CRM records, associate emails with leads, contacts, opportunities, and accounts, and create new records. For high-volume email capture, administrators can configure redirect rules to route emails automatically to their ServiceNow instance without manual association. This ability eliminates context switching between applications, reduces manual data entry, and promotes consistent CRM data for better pipeline visibility and follow-up tracking.

## CRM Outlook Add-in users

<table id="table_sam_users"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales representative

</td><td>

Searches for CRM records, associates emails to track engagement, and creates leads or contacts directly from Outlook.

</td></tr><tr><td>

Sales manager

</td><td>

Gains visibility into customer engagement and deal progression through consistently logged email interactions.

</td></tr><tr><td>

CRM administrator

</td><td>

Configures the CRM Outlook Add-in and AI sales activity association plugins, manages user roles, and sets up email promotion rules.

</td></tr></tbody>
</table>## CRM Outlook Add-in workflow

The following workflow illustration shows how a sales representative captures an inbound inquiry using the CRM Outlook Add-in.

\[Omitted image "crm-outlook-add-in.svg"\] Alt text: Infographic showing how sales representatives use the CRM Outlook add-in to search CRM records, associate emails, and create new leads or contacts. For details, refer to the following description.

1.  As an admin, install the CRM Outlook Add-in application.
2.  Deploy the ServiceNow CRM for Outlook add-in using the manifest file.
3.  Install the User Mailbox Integration plugin.
4.  Configure email promotion so that emails associated with CRM records through the ServiceNow CRM for Outlook add‑in are promoted from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table, making them visible to agents in the workspace.
5.  A prospect submits an inquiry through the company website or sends an email directly to a sales representative.
6.  The sales representative receives the email in their Outlook inbox and opens the ServiceNow CRM for Outlook add-in.
7.  The representative searches for existing CRM records matching the sender's name, email, company, or other identifying information.
    -   If a matching record exists, the representative associates the email to the lead, contact, opportunity, or account.
    -   If no matching record exists, the representative creates a lead or contact record and associates the email to that record in one action.
8.  Sales teams can view the associated email on the CSM/FSM Configurable Workspace.

## CRM Outlook Add-in benefits

|Benefits|Feature|Users|
|--------|-------|-----|
|Locate CRM records such as leads, opportunities, accounts, or contacts, and link emails without leaving Outlook.|[Associate an email with an existing CRM record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/associate-email-crm-outlook.md)|Sales representative, Sales manager|
|Capture new prospects immediately from inbound inquiries with auto-populated sender information and associate emails in a single action.|[Create a CRM record from Microsoft Outlook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-crm-entity-outlook.md)|Sales representative|
|Promote emails from the Staged Email \[sys\_email\_staging\] table to the Email \[sys\_email\] table, making them visible to agents in the workspace.|[Configure email promotion rules for Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/promote-crm-outlook-emails.md)|CRM administrator|
|View associated emails from the CRM entity records.|[Track emails linked from Microsoft Outlook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/view-associated-emails-crm.md)|Sales representative|

## What to explore next

To learn more about configuring and using CRM Outlook Add-in, see:

-   [Configuring Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-activity-management.md)
-   [Using Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-activity-management.md)
-   [Activity Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/activity-management-reference.md)

