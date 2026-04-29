---
title: Read or send emails using Microsoft Graph
description: Use Microsoft Graph endpoints to read or send emails from Microsoft Exchange Online.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Read or send emails using Microsoft Graph

Use Microsoft Graph endpoints to read or send emails from Microsoft Exchange Online.

## Using Microsoft Graph with ServiceNow

In addition to the standard IMAP, SMTP, and POP3, the ServiceNow AI Platform supports Microsoft Graph as an email type.

Email account administrators, which are users who have the email\_account\_admin role, can configure

-   ServiceNow AI Platform to read emails from an Microsoft Exchange Online tenant using Graph Endpoints by authenticating with a client ID and client secret or with certificates.
-   ServiceNow AI Platform to send emails from an Microsoft Exchange Online tenant using Graph Endpoints by authenticating with a client ID and client secret.

**Note:** Antispam and malware scanning are managed by the customer and not ServiceNow.

To receive and email, go to the **Email Account** form, select, **Microsoft Graph \(Receive\)** in the **Type** field.

To send and email, go to the **Email Account** form, select, **Microsoft Graph \(Send\)** in the **Type** field.

-   **[Activate Email - Support for Email Processing by Microsoft Graph API](../task/ms-graph-plugin.md)**  
You can activate the Email - Support for Email Processing by Microsoft Graph API plugin \(com.glide.email.graph\) for Notifications if you have the admin role.
-   **[Reading email using Microsoft Graph](read-email-using-ms-graph.md)**  
Use Microsoft Graph API to retrieve emails from Microsoft Exchange Online and save them to sys\_email table.
-   **[Sending email using Microsoft Graph](send-email-using-ms-graph.md)**  
Use Microsoft Graph endpoints to deliver emails through Microsoft Exchange Online using the SMTP Sender.

**Parent Topic:**[Advanced email setup](../../reference-pages/concept/c_AlternateEmailConfigurations.md)

