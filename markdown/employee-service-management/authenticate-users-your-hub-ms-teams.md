---
title: Create Microsoft Azure application and authenticate users to access Employee Center in Microsoft Teams
description: Create a Microsoft Azure application in the Microsoft Azure portal to enable agents to start and import the chat conversations, and assign permissions to users to view the Employee Center dashboard in the Microsoft Teams application.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Create Microsoft Azure application and authenticate users to access Employee Center in Microsoft Teams

Create a Microsoft Azure application in the Microsoft Azure portal to enable agents to start and import the chat conversations, and assign permissions to users to view the Employee Center dashboard in the Microsoft Teams application.

## Before you begin

Role required: Microsoft Azure admin

## Procedure

1.  Log in to the [Microsoft Azure portal](https://portal.azure.com/).

2.  Navigate to **Azure Services** &gt; **Microsoft Entra ID** &gt; **Manage** &gt; **App registrations**.

3.  Select **New registration**.

    The **Register an application** form appears.

    ![Register an application](../images/reg-an-app.png)

4.  Enter the name for your application, for example: `ServiceNow Auth app`, on the Register an application page.

5.  Select **Accounts in this organizational directory only \(Servicenow only - Single tenant\)**.

    For more information on why this option is selected, see [Identity and account types for single- and multi-tenant apps](https://learn.microsoft.com/en-us/security/zero-trust/develop/identity-supported-account-types#accounts-in-this-organizational-directory-only---single-tenant).

6.  Select **Register**.

    A new Microsoft Azure app is registered.

7.  Navigate to **Manage** &gt; **Authentication**.

8.  Select **Add a platform** &gt; **Web**.

9.  On the **Configure Web** form, fill in the fields.

<table id="table_cfc_hsg_pnb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Redirect URIs

</td><td>

Provide the redirect URI. The redirect URI should be in the following format:

 `https://<instance-url>/sn_now_teams_ms_login.do`

 where &lt;instance-url&gt; is the ServiceNow instance URL.

</td></tr><tr><td>

Implicit grant

</td><td>

Select **Access tokens** and **ID tokens**.

</td></tr></tbody>
</table>    ![Configure web form](../images/configure-web-meeting-extensibility02.png)

10. Select **Configure**.

11. Navigate to **Manage** &gt; **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph**.

12. Select **Delegated permissions**.

13. Select **Openid permissions** accordion, and select **email**, **offline\_access**, **openid**, and **profile** check boxes.

    ![Request API permissions](../images/request-api-permissions.png)

14. Select **Add permissions**.

15. In the **API permissions** screen, select the **Grant admin consent for \{tenant\}** link.

16. Select **Yes** on the pop-up dialog box.

17. Navigate to **Manage** &gt; **Expose an API**.

18. Select **Set against Application ID URI**, and enter the application URI in the format: `api://<instance>.<domain_name>.com/<client_id>`.

    **Note:** The client ID is the application ID from your Microsoft Azure portal.

19. Select **Save**.

20. Select **Add a scope**.

    In the **Add a scope** form, fill the following fields.

    |Field|Description|
    |-----|-----------|
    |Scope name|access\_as\_user|
    |Who can consent|Admins and users|
    |Admin consent display name|Teams can access the user’s profile.|
    |Admin consent description|Allows Teams to call the app’s web APIs as the current user.|
    |User consent display name|Teams can access the user profile and make requests on the user's behalf.|
    |User consent description|Enable Teams to call this app’s APIs with the same rights as the user.|
    |State|Enabled|

    ![Add scope](../images/add_scope02.png)

21. Select the **Add scope** button.

22. Navigate to **Authorized client applications** &gt; **Add a client application**.

23. In the **Add a client application** form, fill the fields.

<table id="add-client-application"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Client ID

</td><td>

-   Microsoft Teams mobile/desktop application:

**1fec8e78-bce4-4aaf-ab1b-5451cc387264**

-   Value for Microsoft Teams web application:

**5e3ce6c0-2b1f-4285-8d4b-75ee78787346**

</td></tr><tr><td>

Authorized scopes

</td><td>

Check the authorized scope

</td></tr></tbody>
</table>    **Note:** For using Employee Center in Microsoft 365 applications, add the following client IDs:

<table id="table_bmb_2hh_1yb"><thead><tr><th align="left">

Client ID

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

**4765445b-32c6-49b0-83e6-1d93765276ca**

</td><td>

Client ID for Microsoft 365 web application

</td></tr><tr><td>

**0ec893e0-5785-4de6-99da-4ed124e5296c**

</td><td>

Client ID for Microsoft 365 desktop application

</td></tr><tr><td>

**d3590ed6-52b3-4102-aeff-aad2292ab01c**

</td><td>

Client ID for Outlook desktop application web application

</td></tr><tr><td>

**bc59ab01-8403-45c6-8796-ac3ef710b3e3**

</td><td>

Client ID for Outlook web application

</td></tr><tr><td>

**27922004-5251-4030-b22d-91ecd9a37ea4**

</td><td>

Client ID for Outlook mobile application

</td></tr></tbody>
</table>    For more information on the client IDs, see [Configure your tab app in Microsoft Entra ID](https://learn.microsoft.com/en-us/microsoftteams/platform/tabs/how-to/authentication/tab-sso-register-aad#to-configure-authorized-client-application) in the Microsoft Teams documentation.

    ![Add client ID](../images/add-client-id.png)

24. Select the **Add application** button.

    Copy the Application \(client\) ID, and Directory \(tenant\) ID from the application overview page in the Microsoft Azure portal to update the details in the ServiceNow instance.

    ![Application ID and the tenant ID from the app overview page](../images/app-overview-azure-portal.png)


**Parent Topic:**[Setup for integrating self-configured apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_s_tnt.md)

