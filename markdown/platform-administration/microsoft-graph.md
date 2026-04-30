---
title: Configure an OAuth profile to use a client ID and secret for token generation
description: Configure an OAuth profile using a client ID and client secret to create an email account for using Microsoft Graph \(receive\) in your email account type.Use the information generated during Microsoft Azure account configuration to register an application as an OAuth provider.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Reading email using Microsoft Graph, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure an OAuth profile to use a client ID and secret for token generation

Configure an OAuth profile using a client ID and client secret to create an email account for using Microsoft Graph \(receive\) in your email account type.

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

    5.  In the **Select permissions** field, enter `Mail.ReadWrite`.

    6.  Select the **Mail.ReadWrite** check box.

    7.  Select **Add permissions**.

5.  Select **Grant admin consent for &lt;your organization name&gt;**.

6.  Select **Yes** to confirm.

7.  Add a client secret.

    1.  In Microsoft Azure, navigate to **Manage** &gt; **Certificates &amp; secrets**.

    2.  Select **New client secret**.

    3.  Provide a description and an expiration date and select **Add**.

8.  Copy the value \(secret value\) to a text file.

9.  Navigate to **Overview** &gt; **Endpoints** and copy the **OAuth 2.0 token endpoint \(v2\)** to a text file.


**Parent Topic:**[Reading email using Microsoft Graph](../concept/read-email-using-ms-graph.md)

**Related topics**  


[Activate Email - Support for Email Processing by Microsoft Graph API](ms-graph-plugin.md)

[Configure an OAuth profile to use certificates for authentication with Microsoft Azure](configure-oauth-profile-using-certificates.md)

[Create an email account for Microsoft Graph \(receive\)](create-email-account-ms-graph.md)

## Register an application as an OAuth provider

Use the information generated during Microsoft Azure account configuration to register an application as an OAuth provider.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  On the **What kind of OAuth application** screen, select **Connect to a third-party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_alw_kq3_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record.

</td></tr><tr><td>

Client ID

</td><td>

Application ID of the application you created in Microsoft Azure.

</td></tr><tr><td>

Client Secret

</td><td>

The client secret you generated when you created the application in Microsoft Azure.**Note:** When using certificates, the **Client Secret** is a dummy value.

</td></tr><tr><td>

OAuth API Script

</td><td>

OAuth API script name. For more information see, [OAuth API Script](oauth-api-script.md). **Note:** This is required only while using certificates.

</td></tr><tr><td>

Default Grant type

</td><td>

Client Credentials.

</td></tr><tr><td>

Token URL

</td><td>

Token URL copied after configuring the Microsoft Azure account.

</td></tr><tr><td>

Redirect URL

</td><td>

`https://<instance>./oauth_redirect.do` **Note:** This URL should be the same as the URL in Microsoft Azure.

</td></tr></tbody>
</table>5.  Right-click the form header and select **Save**.

    An OAuth Entity Profile record is created.

6.  In the OAuth Entity Scopes related list, add scopes to match the permissions you defined when you configured the application.

7.  Select **Insert a new row**.

8.  Enter `Default` as the name and `.default` as OAuth scope.

9.  Right-click the form header and select **Save**.

10. In the OAuth Entity Profiles embedded list, select the profile created by default.

11. In the OAuth Entity Scopes embedded list, add a new row and select the **Default** scope.

12. Select **Update**.


### What to do next

[Create an email account for Microsoft Graph \(receive\)](create-email-account-ms-graph.md) using the OAuth profile.

