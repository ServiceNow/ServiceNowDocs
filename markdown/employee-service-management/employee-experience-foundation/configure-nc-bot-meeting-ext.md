---
title: Configure the Notify connector bot for Meeting Extensions
description: Configure the Notify connector bot for Meeting Extensions in the Microsoft Azure portal.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrate Meeting Extensions self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Configure the Notify connector bot for Meeting Extensions

Configure the Notify connector bot for Meeting Extensions in the Microsoft Azure portal.

## Before you begin

Role required: Microsoft Azure admin

## Procedure

1.  Log in to the Microsoft Azure portal at [https://portal.azure.com/](https://portal.azure.com/) as the Microsoft Azure admin.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Search for and open the new bot created for Notify Connector by name or by Application \(client\) ID.

    The app was created in the section [Create an app in Microsoft Teams to enable making calls](../../notify2/task/create-app-ms-teams.md).

4.  Expose an API.

    1.  Navigate to **Manage** &gt; **Expose an API** &gt; **Application ID URI** &gt; **Set**.

    2.  Paste the Application ID URI `api://<instance_name>.service-now.com/<client-id-in-azure>`, which was set for the Single-sign on in the section [Create and configure an app for Meeting Extensions in the Microsoft Teams Developer Portal](config-nc-use-meeting-ext-ms-teams-portal.md) and select **Save**.

    3.  Select **Add a scope**.

    4.  On the form, fill in the fields.

<table id="table_jjd_ltw_rwb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Scope name

</td><td>

`access_as_user`

</td></tr><tr><td>

Who can consent?

</td><td>

Select **Admins and users**.

</td></tr><tr><td>

Admin consent display name

</td><td>

Enter a valid name.

 For example, `Teams can access the user’s profile`.

</td></tr><tr><td>

Admin consent description

</td><td>

Enter a valid description.

 For example, `Allows Teams to call the app’s web APIs as the current user`.

</td></tr><tr><td>

User consent display name

</td><td>

Enter a valid name.

 For example, `Teams can access the user profile and make requests on the user's behalf`.

</td></tr><tr><td>

User consent description

</td><td>

Enter a valid description.

 For example, `Enable Teams to call this app’s APIs with the same rights as the user`.

</td></tr><tr><td>

State

</td><td>

Set to **Enabled**

</td></tr></tbody>
</table>    5.  Select **Add scope**.

    6.  Select **Add a client application**, enter the value `1fec8e78-bce4-4aaf-ab1b-5451cc387264` for Microsoft Teams desktop and mobile application in the **Client ID**, and then select **Authorized scopes**, and select **Add application**.

        For more information, see 'Update Azure AD app registration for SSO' section on the [Extend a Teams personal tab across Microsoft 365 app](https://learn.microsoft.com/en-us/microsoftteams/platform/m365-apps/extend-m365-teams-personal-tab?tabs=manifest-teams-toolkit) page.

    7.  Select **Add a client application**, enter the value `5e3ce6c0-2b1f-4285-8d4b-75ee78787346` for Microsoft Teams desktop and mobile application in the **Client ID**, and then select **Authorized scopes**.

        For more information, see the "Update Azure AD app registration for SSO" section on the [Extend a Teams personal tab across Microsoft 365 app](https://learn.microsoft.com/en-us/microsoftteams/platform/m365-apps/extend-m365-teams-personal-tab?tabs=manifest-teams-toolkit) page.

    8.  Select **Add application**.


**Parent Topic:**[Integrate Meeting Extensions self-configured app with Microsoft Teams](../concept/setup-meeting-extensibility-single-tenant.md)

