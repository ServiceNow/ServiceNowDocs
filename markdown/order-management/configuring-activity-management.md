---
title: Configuring Activity Management
description: Install and configure the necessary plugins for enabling Activity Management features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configuring-activity-management.html
release: australia
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 3
keywords: [configure]
breadcrumb: [Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Configuring Activity Management

Install and configure the necessary plugins for enabling Activity Management features.

**Important:**

To use personal email mailbox in Activity Management, you must install the User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) on your ServiceNow instance. For setup instructions, see [Personal corporate mailbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/personal-corporate-mailbox.md).

The Omnichannel Callback for Customer Service Management \(com.sn\_omnichannel\_callback\) application must be installed with CRM Touchpoints to enable the click-to-call feature so agents can call customers from the touchpoint record.

## Configuring CRM Touchpoints

Install and configure the CRM Touchpoints application. It provides a unified system for capturing and tracking customer engagements for your sales and service teams while providing leadership with visibility into representative activity and engagement effectiveness.

1.  [Install CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-crm-touchpoints.md)

    You can install the CRM Touchpoints application \(com.sn\_crm\_touchpoint\) if you have the admin role.

2.  [Create custom touchpoint types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-custom-touchpoint-types.md)

    Create touchpoint types tailored to your sales organization's workflow to capture activities beyond the standard Discovery, Demo, and CBR types.


## Configuring CRM Outlook Add-in

Install and configure the CRM Outlook Add-in application to make the ServiceNow CRM for Outlook add-in available to your users.

1.  [Install CRM Outlook Add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-crm-outlook-add-in.md)

    You can install the CRM Outlook Add-in application \(com.sn\_crm\_outlook\) if you have the admin role.

2.  [Configure CRM access from Microsoft Outlook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/add-crm-outlook-add-in.md)

    Download and install the ServiceNow CRM for Outlook add-in to access and manage CRM records directly from your Outlook inbox, eliminating the need to switch between applications.

3.  [Configure email promotion rules for Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/promote-crm-outlook-emails.md)

    Configure email promotion rules to automatically process staged emails for manual association through the ServiceNow CRM for Outlook add-in or to trigger AI-powered auto-association with existing sales entities.


## Configuring AI sales activity association

Install and configure the AI sales activity association application to automatically link sales-related emails to existing CRM entities such as Lead, Opportunity, Account, or Contact.

**Note:** Installing AI sales activity association also installs CRM Outlook Add-in as a dependency. This is useful when a sales representative wants to manually associate an email to a CRM entity which the agentic workflow missed or ignored for reasons such as missing CRM entity or lower confidence score.

1.  [Install AI sales activity association](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-ai-sales-activity-association.md)

    You can install the AI sales activity association application \(com.sn\_act\_assoc\_agent\) if you have the admin role.

2.  [Personal corporate mailbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/personal-corporate-mailbox.md)

    Install and configure the User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) so that emails from sales representative's personal mailbox can be imported into the Staged Email \[sys\_email\_staging\] table.

3.  [Configure email promotion rules for Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/promote-crm-outlook-emails.md)

    Configure email promotion rules to automatically process staged emails for manual association through the ServiceNow CRM for Outlook add-in or to trigger AI-powered auto-association with existing sales entities.


**Related topics**  


[Using Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-activity-management.md)

[Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-activity-management.md)

[Activity Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/activity-management-reference.md)

