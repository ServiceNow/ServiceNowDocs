---
title: Setting up Rally OAuth 2.0 credentials for DevOps
description: Authenticate a Rally tool connection using OAuth 2.0 credentials.Register a Rally OAuth application for DevOps Change Velocity.Use the information generated during Rally account configuration to register Rally as an OAuth provider and enable the instance to request OAuth 2.0 tokens.Create a credential record for the Rally account previously created to authorize actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/setting-up-rally-oauth-2-0-credentials-for-devops.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 2
breadcrumb: [Rally, Integrate, DevOps Change Velocity, IT Service Management]
---

# Setting up Rally OAuth 2.0 credentials for DevOps

Authenticate a Rally tool connection using OAuth 2.0 credentials.

Configure your Rally account, register Rally in the application registry, and create a credential record for the Rally account.

**Parent Topic:**[Rally integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/rally-devops-integration.md)

## Register a Rally OAuth application for DevOps

Register a Rally OAuth application for DevOps Change Velocity.

### Before you begin

Role required: \(In Rally\) A user with Rally subscription

**Note:** If you don't have permission to create OAuth clients, the **Create** option will be disabled in Rally. Contact your Rally subscription or workspace administrator to have this option enabled for you.

### Procedure

1.  Log in to [CA Agile Central](https://rally1.rallydev.com/login/accounts/index.html).

2.  On the page header, select your profile and then select **My Settings**.

3.  Navigate to **Access** &gt; **OAUTH CLIENTS**.

4.  Select **Create**.

5.  In the dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Application Name|Provide a name for the application.|
    |Callback URL|Callback URL of the ServiceNow instance to which the application is to be integrated. For example, `https://<instance_url>/oauth_redirect.do`.|

6.  Select **Next**.

7.  Copy the Client ID and Client secret for later use.


## Register Rally as an OAuth Provider \(Authorization Code\)

Use the information generated during Rally account configuration to register Rally as an OAuth provider and enable the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

    The system displays the message **What kind of OAuth application?**

3.  Select **Connect to a third party OAuth Provider**.

    The system displays an empty Application Registries form.

4.  Complete the form.

<table id="table_fd2_2xr_4mb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record. For example, enter `DevOps Rally OAuth`.

</td></tr><tr><td>

Client ID

</td><td>

Client ID that you copied in the previous procedure.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret that you copied in the previous procedure.

</td></tr><tr><td>

OAuth API script

</td><td>

Select **OAuthDevOpsRallyHandler**.

</td></tr><tr><td>

Default Grant type

</td><td>

Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

Enter `https://rally1.rallydev.com/login/oauth2/auth`.

</td></tr><tr><td>

Token URL

</td><td>

Enter `https://rally1.rallydev.com/login/oauth2/token`.

</td></tr></tbody>
</table>5.  Leave the rest of the form fields as default.

6.  Right-click the form header, and select **Save**.

    The system populates **OAuth Entity Profile** with **Grant Type** as **Authorization Code**. For example, **OAuth Entity Profile** is created with the default **Name**, **DevOps Rally OAuth default\_profile**.

7.  Navigate to the **OAuth Entity Scopes** related list and add **alm** as the scope.

8.  Right-click the form header, and select **Save**.


## Create a credential record for Rally

Create a credential record for the Rally account previously created to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays the OAuth 2.0 Credentials form.

4.  Fill in these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `My Rally Account Credential`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the default OAuth Entity profile you created previously.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Save the record.

6.  Select the **Get OAuth Token** related link to generate the OAuth token.

    A successful token generation indicates that you can now authenticate connection between ServiceNow DevOps and Rally via OAuth 2.0.


