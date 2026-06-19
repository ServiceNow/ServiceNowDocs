---
title: Reading email using Microsoft Graph
description: Use Microsoft Graph endpoints to read emails from Microsoft Exchange Online.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/read-email-using-ms-graph.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Reading email using Microsoft Graph

Use Microsoft Graph endpoints to read emails from Microsoft Exchange Online.

## Using Microsoft Graph with ServiceNow

In addition to the standard IMAP, SMTP, and POP3, the ServiceNow AI Platform supports Microsoft Graph as an email type.

Email account administrators, which are users who have the email\_account\_admin role, can configure ServiceNow AI Platform to read emails from an Microsoft Exchange Online tenant using Graph Endpoints by authenticating with a client ID and client secret or with certificates.

**Note:** Antispam and malware scanning are managed by Microsoft Graph account and not ServiceNow.

In the **Email Account** form, select, **Microsoft Graph \(Receive\)** in the **Type** field.

-   **[Activate Email - Support for Email Processing by Microsoft Graph API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/ms-graph-plugin.md)**  
You can activate the Email - Support for Email Processing by Microsoft Graph API plugin \(glide.email.graph\) for Notifications if you have the admin role.
-   **[Configure an OAuth profile to use a client ID and secret for token generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/microsoft-graph.md)**  
Configure an OAuth profile using a client ID and client secret to create an email account for using Microsoft Graph \(receive\) in your email account type.
-   **[Configure an OAuth profile to use certificates for authentication with Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configure-oauth-profile-using-certificates.md)**  
Configure an OAuth application profile to authenticate using certificates.
-   **[Create an email account for Microsoft Graph \(receive\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/create-email-account-ms-graph.md)**  
Create an email account for reading emails from Microsoft Exchange Online using Microsoft Graph Endpoints.

**Parent Topic:**[Advanced email setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/c_AlternateEmailConfigurations.md)

