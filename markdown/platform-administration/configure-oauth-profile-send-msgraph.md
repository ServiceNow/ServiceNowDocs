---
title: Configure OAuth profile to use a client ID and secret for token generation
description: Configure an OAuth profile using a client ID and client secret to create an email account for using Microsoft Graph \(send\) in your email account type.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Send email using Microsoft Graph, Read or send emails using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure OAuth profile to use a client ID and secret for token generation

Configure an OAuth profile using a client ID and client secret to create an email account for using Microsoft Graph \(send\) in your email account type.

## Before you begin

Create an [Microsoft Azure](https://portal.azure.com) account to configure OAuth profile.

Complete the set up steps using your Microsoft Azure Developer account. See the [Microsoft Azure product documentation](https://docs.microsoft.com/en-us/azure/) for instructions on creating and configuring custom applications.

Role required: admin and Microsoft Azure portal administrator

## Procedure

1.  Log in to the Microsoft Azure registration portal with your organization credentials.

    For more information, see the Microsoft Azure [registration portal documentation](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade).

2.  Register a new custom application by filling in the application name, supported account type, and redirect URI, and select **Register**.

    **Note:** Enter the redirect URI in the following format: `https://<instance>/oauth_redirect.do`.

    An overview of the application's basic information is displayed.

3.  Copy the client ID to a text file.

    You will use this ID and the client secret value generated in the next steps to register the app as a third-party OAuth provider on your ServiceNow instance. You use the application ID as the client ID when you connect the application to your instance.

4.  Enable the **Mail.ReadWrite** permission.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **API permissions**.

    2.  Select **Add a permission**.

    3.  Select the Microsoft Graph tile.

    4.  Select **Application Permissions**.

    5.  In the **Select permissions** field, enter `Mail.Send`.

    6.  Select the **Mail.Send** check boxes.

    7.  In the **Select permissions** field, enter `Mail.ReadWrite`.

    8.  Select the **Mail.ReadWrite** check boxes.

    9.  Select **Add permissions**.

5.  Select **Grant admin consent for &lt;your organization name&gt;**.

6.  Select **Yes** to confirm.

7.  Add a client secret.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **New client secret**.

    3.  Provide a description and an expiration date and select **Add**.

8.  Copy the value \(secret value\) to a text file.

9.  Navigate to **Overview** &gt; **Endpoints** and copy the **OAuth 2.0 token endpoint \(v2\)** to a text file.


**Parent Topic:**[Sending email using Microsoft Graph](../concept/send-email-using-ms-graph.md)

