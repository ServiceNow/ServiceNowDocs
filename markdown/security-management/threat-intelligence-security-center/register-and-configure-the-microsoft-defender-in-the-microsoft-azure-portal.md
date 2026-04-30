---
title: Register and configure the Microsoft Defender in the Microsoft Azure portal
description: Register the Microsoft Defender EDR in the Microsoft Azure portal and grant the read and write access to the application.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for EDR Integration, TISC Security Tools integrations, TISC Integrations, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Register and configure the Microsoft Defender in the Microsoft Azure portal

Register the Microsoft Defender EDR in the Microsoft Azure portal and grant the read and write access to the application.

## Before you begin

Role required: Application developer, Tenant administrator.

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Enter `App registrations` in the Search box, and click **Click New registration**.

3.  Enter a name for your application and the redirect URI, and click **Register**.

    An example name is `Microsoft Defender for Endpoint`. The Redirect URI is used while providing admin consent for the application.

4.  In the **App registrations** page, select the application that you registered in Step 3.

5.  Under Manage, select **Certificates &amp; secrets**.

6.  To create a client secret, select **New client secret**.

7.  Copy the client secret and save it.

    In case you forgot the client secret, you can generate a new client secret.

8.  Navigate to **Manage** &gt; **API Permissions**.

9.  Click **Add a permission**.

10. In the Request API permissions window, click the **APIs my organization uses** tab.

11. Search for and select **WindowsDefenderATP**.

12. In the WindowsDefenderATP permissions, select **Application permissions**.

    Enabling this permission ensures that the application runs as a background service or daemon without a signed-in user.

13. Add the following application level permission and grant admin consent for the newly added API permission.

    |Permission|Permission Display Name|
    |----------|-----------------------|
    |Ti.ReadWrite.All|Read and write Indicators|


**Parent Topic:**[Microsoft Defender for EDR Integration](../concept/tisc-ms-defender-integration.md)

