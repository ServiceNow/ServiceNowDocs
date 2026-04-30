---
title: Register a Microsoft Entra ID application
description: Register an application through the Microsoft Entra ID portal.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Register a Microsoft Entra ID application

Register an application through the Microsoft Entra ID portal.

## Before you begin

Microsoft Entra ID Role required: Refer to the [Minimal user permissions](../concept/integrate-with-microsoft.md) table.

## Procedure

1.  From a web browser, open the [App registrations page](https://portal.azure.com/?Microsoft_AAD_RegisteredApps=true#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) of the Microsoft Entra ID portal.

2.  Log in using your global administrator credentials.

3.  On the App registrations page, select **New registration**.

4.  In the Name section of the Register an application form, enter a name for the application.

5.  In the Supported account types section, select **Accounts in any organizational directory \(Any Microsoft Entra ID - Multitenant\)**.

6.  Select **Register**.

    The application is registered and you’re automatically redirected to the Overview page for the new application.

7.  On the Overview page, copy the values in the **Application \(client\) ID** and **Directory \(tenant\) ID** fields.

    Save them in a secure location for later use.

8.  Generate a Client secret for your application.

    1.  From the side navigation menu, navigate to **Manage** &gt; **Certificates &amp; secrets**.

        The Certificates &amp; secrets page opens.

    2.  In the Client secrets section, generate a client secret for the application by selecting **New client secret**.

    3.  In the dialog box, fill in the fields.

<table id="table_mks_npw_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the client secret.

</td></tr><tr><td>

Expires

</td><td>

Time period after which you want the client secret to expire. The options are:-   In 1 year
-   In 2 years
-   Never


</td></tr></tbody>
</table>    4.  Select **Add**.

        The dialog box closes and you return to the Certificates &amp; secrets page.

    5.  In the Client secrets section, copy the value in the **VALUE** field for the newly generated client secret.

        Save this in a secure location for later use.

9.  Specify the level of access that the application has to your protected resources.

    1.  From the side navigation menu, navigate to **Manage** &gt; **API permissions**.

    2.  On the API permissions page, select **Add a permission**.

    3.  In the Request API permissions dialog box, select the **Microsoft APIs** tab.

    4.  From the list of available Microsoft APIs, select **Microsoft Graph**.

    5.  When prompted to select the types of permissions that the application requires, select **Application permissions**.

    6.  Under Select permissions, select the check boxes for the following permissions:

        -   Reports.Read.All
        -   User.Read.All
        -   Organization.Read.All
    7.  Select **Add permissions**.

        The dialog box closes and you return to the API permissions page.

10. Grant admin consent for your application.


## What to do next

After you successfully register and set up your application, remain in the Microsoft Azure portal if you must enable your application to access Power BI service content and APIs.

