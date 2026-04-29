---
title: Register an Asana OAuth application
description: Register the Asana OAuth application to access the Asana API 1.0 and to receive a Client ID and Client secret.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Asana Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Register an Asana OAuth application

Register the Asana OAuth application to access the Asana API 1.0 and to receive a Client ID and Client secret.

## Before you begin

Asana Role required: admin

-   The Asana Integration Hub spoke must be active. For more information, see [Asana Spoke](../concept/asana-spoke.md).

## Procedure

1.  Log in to your Asana account.

2.  Select the user's profile icon on the top-right corner.

3.  Select **My Settings**.

4.  Select the **Apps** tab.

5.  Select the **Manage Developers App** link at the bottom to navigate to the developer console window.

6.  Select **+ Create new app**.

7.  On the **Create new app** page, provide a name for your application.

8.  Select the **I agree to API terms and conditions** check box.

9.  Select **Create app**.

10. Provide basic information about your application.

11. Select **OAuth** in the left-pane.

12. Copy the Client ID and Client secret for later use.

13. In the **Redirect URLs** field, select **+ Add redirect URL**.

14. Enter `https://<instance>.service-now.com/oauth_redirect.do` where &lt;instance&gt; is the name of your ServiceNow instance.


