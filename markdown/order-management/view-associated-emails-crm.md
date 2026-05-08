---
title: Track emails linked from Microsoft Outlook
description: View emails that have been linked to CRM records using the Microsoft Outlook directly from the CSM/FSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Activity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Track emails linked from Microsoft Outlook

View emails that have been linked to CRM records using the Microsoft Outlook directly from the CSM/FSM Configurable Workspace.

## Before you begin

Email promotion must be configured before you can view the associated emails on the Emails tab of the Lead, Opportunity, Accounts, or Contacts record. For more information, see [Make emails associated through the CRM Outlook Add-in visible to agents](promote-crm-outlook-emails.md).

The User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) must be installed on your ServiceNow instance to enable agents to send emails from the touchpoint record. For setup instructions, see Personal corporate mailbox.

Role required: sn\_crm\_outlook.crm\_outlook\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

3.  Navigate to CRM entity with which you associated the email.

    To view emails associated with a Lead, you'd navigate to **Leads** &gt; **All** and select a LEAD record.

4.  Open the CRM entity record that you want to work with.

5.  Navigate to the **Emails** tab.

6.  View email by selecting a timestamp link from the Created column.


**Parent Topic:**[Using Activity Management](../concept/using-activity-management.md)

