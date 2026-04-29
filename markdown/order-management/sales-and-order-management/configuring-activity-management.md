---
title: Configuring Activity Management
description: Install and configure the necessary plugins for enabling Activity Management features.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [configure]
breadcrumb: [Lead and opportunity management apps, Configure, Sales and Order Management]
---

# Configuring Activity Management

Install and configure the necessary plugins for enabling Activity Management features.

**Note:**

To use email capabilities in Activity Management, you must install the User Mailbox Integration plugin \(com.glide.email.user\_mailbox.integration\) on your ServiceNow instance. For setup instructions, see [Personal corporate mailbox](https://www.servicenow.com/docs/access?context=personal-corporate-mailbox&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

You must also install the Omnichannel Callback for Customer Service Management \(com.sn\_omnichannel\_callback\) application to enable the click-to-call feature, so agents can call customers from the touchpoint record.

## Configuring CRM Touchpoints

Install and configure the CRM Touchpoints application. It provides a unified system for capturing and tracking customer engagements for your sales and service teams while providing leadership with visibility into representative activity and engagement effectiveness.

1.  [Install CRM Touchpoints](../task/install-crm-touchpoints.md)

    You can install the CRM Touchpoints application \(com.sn\_crm\_touchpoint\) if you have the admin role.

2.  [Create custom touchpoint types](../task/create-custom-touchpoint-types.md)

    Create touchpoint types tailored to your sales organization's workflow to capture activities beyond the standard Discovery, Demo, and CBR types.


## Configuring CRM Outlook Add-in

Install and configure the CRM Outlook Add-in application to make the ServiceNow CRM for Outlook add-in available to your users.

1.  [Install CRM Outlook Add-in](../task/install-crm-outlook-add-in.md)

    You can install the CRM Outlook Add-in application \(com.sn\_crm\_outlook\) if you have the admin role.

2.  [Configure CRM access from Microsoft Outlook](../task/add-crm-outlook-add-in.md)

    Download and install the ServiceNow CRM for Outlook add-in to access and manage CRM records directly from your Outlook inbox, eliminating the need to switch between applications.

3.  \(Optional\) [Setting up automatic capture of emails in CRM using redirect rules](using-redirect-rules-crm.md)

    Automate the process of capturing CRM-relevant emails by configuring redirecting rules in your email client so emails can be logged in the CRM without manual associations from the ServiceNow CRM for Outlook add-in by the agent.


