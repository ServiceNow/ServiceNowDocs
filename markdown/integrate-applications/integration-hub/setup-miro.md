---
title: Set up the Miro spoke
description: Integrate the ServiceNow instance and Miro by creating a custom OAuth application in Miro to authenticate ServiceNow requests.Create a Miro Enterprise OAuth 2.0 application to enable access to the Miro API.Enable SCIM \(System for Cross-domain Identity Management\) on your Miro Enterprise account so that you can generate an API access token for authenticating your Miro API requests.Create a connection between your Miro Enterprise applications and your ServiceNow instance.Create a connection between the Miro Enterprise SCIM and your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Miro Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Miro spoke

Integrate the ServiceNow instance and Miro by creating a custom OAuth application in Miro to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Miro spoke.
-   Role required:
    -   ServiceNow admin
    -   Miro Company Admin

## Create a Miro Enterprise OAuth 2.0 application

Create a Miro Enterprise OAuth 2.0 application to enable access to the Miro API.

### Before you begin

Role required: Miro company admin.

### Procedure

1.  From a web browser, open the [Miro Platform](https://developers.miro.com/docs).

2.  If you have not created any teams within your organization or you want to build and test the OAuth 2.0 application using fake data, [get a developer team](https://miro.com/app/dashboard/?createDevTeam=1).

3.  On the page header of the Miro Platform, click **Your Apps**.

    The sign up page opens.

4.  Sign in using your Company Admin credentials.

    Your default organization profile opens.

5.  At the top of the left navigation pane, click the organization profile icon to select the organization that you want to build the OAuth 2.0 application for.

    The profile for the selected organization opens.

6.  On the left navigation pane, click **Profile settings**.

7.  Select the **API, SDK &amp; Embed** tab of your profile settings.

8.  In the Your apps section, select the **I agree to the Terms and Conditions** check box and then click **Create new app**.

    The Create new app dialog box opens.

9.  On the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |App name|Name of the OAuth 2.0 application.|
    |Description|Brief description of the OAuth 2.0 application.|

10. Select the team that you want to build the OAuth 2.0 application for.

11. Click **Create app**.

    The settings for your newly created app open.

12. In the Your app &lt;*app-name*&gt; section, copy the values in the **Client id** and **Client secret** fields.

    Save them in a secure location for later use.

13. In the Redirect URLs section, enter the URL of the OAuth provider that users are redirected to after authentication and then click **Add**.

    Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

14. In the OAuth scopes section, enable the **organizations:read** OAuth scope.

    OAuth scopes specify the level of access that the application has to your protected resources. The organizations:read OAuth scope enables your application to read information about your organizations and organization members.


### What to do next

Keep your organization profile open so that you can enable SCIM \(System for Cross-domain Identity Management\) on your Miro Enterprise account.

## Enable SCIM on your Miro Enterprise account

Enable SCIM \(System for Cross-domain Identity Management\) on your Miro Enterprise account so that you can generate an API access token for authenticating your Miro API requests.

### Before you begin

Role required: Miro Company Admin

### Procedure

1.  On the left navigation pane of your Miro organization profile, click **Security**.

2.  On the Security page, select the option to **Enable SSO/SAML**.

3.  After SSO/SAML is enabled, select the option to enable **SCIM Provisioning**.

    Miro automatically generates and displays your API access token in the **Api Token** field.

4.  Select the **Send email notifications to users provisioned by SCIM** check box to allow Miro to send email notifications to all users that have been provisioned using SCIM.

5.  Copy the API access token in the **Api Token** field.

    Save it in a secure location for later use.


## Create a Miro Enterprise connection

Create a connection between your Miro Enterprise applications and your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    The Workflow Studio launches in a new tab.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Click **View Details** for your Miro Enterprise connection.

5.  From your Miro Enterprise connection details, click **Add Connection**.

    The Create Connection dialog box opens.

6.  On the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the Miro Enterprise connection. This field populates automatically.|
    |Credential Information|
    |OAuth Client ID|Client ID that is assigned to your Miro Enterprise OAuth 2.0 application.|
    |OAuth Client Secret|Client secret that is assigned to your Miro Enterprise OAuth 2.0 application.|
    |OAuth Redirect URL|URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the redirect URL that you specified in [Create a Miro Enterprise OAuth 2.0 application](setup-miro.md#).|

7.  Click **Create and Get OAuth Token**.

    The Miro OAuth authorization dialog box opens.

8.  On the dialog box, locate the team that you built the Miro Enterprise OAuth 2.0 application for and then click **Install**.

    The OAuth access token becomes available for authorizing your Miro Enterprise connection.


## Create a Miro Enterprise SCIM connection

Create a connection between the Miro Enterprise SCIM and your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Click **View Details** for your Miro Enterprise SCIM connection.

4.  From your Miro Enterprise SCIM connection details, click **Add Connection**.

    The Create Connection dialog box opens.

5.  On the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the Miro Enterprise SCIM connection. This field populates automatically.|
    |Credential Information|
    |API Token|API access token for authenticating Miro API requests. Enter the same API access token that you generated and copied in [Enable SCIM on your Miro Enterprise account](setup-miro.md#).|

6.  Click **Create Connection**.


