---
title: Configure Microsoft SharePoint Graph connection
description: Configure a Microsoft SharePoint Graph connection and a connection record that enable your ServiceNow instance to integrate with the Microsoft SharePoint using the Microsoft Graph.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-02-01"
reading_time_minutes: 4
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure Microsoft SharePoint Graph connection

Configure a Microsoft SharePoint Graph connection and a connection record that enable your ServiceNow instance to integrate with the Microsoft SharePoint using the Microsoft Graph.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft SharePoint Online spoke.
-   Access to Microsoft Azure portal.
-   Create an OAuth application on Microsoft Azure portal.
-   Role required: admin.

## Procedure

1.  Configure a SharePoint Graph connection by adding permissions.

    1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).

    2.  Select **App registrations**.

        ![App registration button.](../image/MS-sharepoint-spoke-app-reg-button.png)

    3.  Select **All applications** or **Owned applications**.

        ![OAuth application selection options.](../image/ms-sharepoint-spoke-graph-select-app.png)

    4.  In the search field, enter the name of the OAuth application you had created.

        To learn how to configure an OAuth application, see [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

    5.  In the search results, select the name of the OAuth application you had configured.

    6.  On the left panel, under the Manage heading, select API permissions.

        ![API permissions link.](../image/MS-sharepoint-spoke-graph-api-permissions-link.png)

    7.  Under the Configured permissions heading, select **+ Add a permission**.

    8.  In the Request API permissions window, select **Microsoft Graph**.

        ![Microsoft Graph button.](../image/MS-sharepoint-spoke-graph-ms-graph-button.png)

    9.  Select **Delegated permissions**.

    10. Under the Select permissions heading, enter `site` in the search field.

    11. Expand the Sites list.

        ![Sites list.](../image/MS-sharepoint-spoke-graph-click-sites.png)

    12. Select `Sites.FullControl.all`, `Sites.Read.All` and `Sites.ReadWrite.All`.

        ![Microsoft SharePoint Online spoke Graph Site permissions.](../image/ms-sharepoint-online-spoke-graph-site-permissions.png)

    13. Under the Select permissions heading, enter `User.read` in the search field.

        ![Microsoft SharePoint Online spoke Graph User permissions.](../image/MS-SharePoint-Online-spoke-graph-user-permission.png)

    14. Select **Add permissions**.

        The permission is added.

        ![Permissions added.](../image/MS-sharepoint-spoke-graph-permissions-added.png)

    15. To grant admin consent, under the Configured permissions heading, select **Grant admin consent**.

    16. Select **Yes**.

        Admin consent is mandatory if the value under the Admin consent required column for the Sites.Read.All permission is Yes.

2.  Configure the Microsoft SharePoint Graph connection record.

    1.  Log in to your ServiceNow instance.

        **Note:** The URL of the instance and that of the instance you had provided as the redirect URL must be the same.

    2.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    3.  Select the **Integrations** tab.

    4.  In the Search all connections field, enter `Microsoft SharePoint`.

        **Note:** The **Outbound** tab is selected by default. Confirm that the **Outbound** tab is already selected.

    5.  In the Search all connections field, enter `Microsoft SharePoint`.

    6.  In the MicrosoftSharePointGraph tile, click **View Details**.

        ![View Details button on Microsoft SharePoint Graph alias.](../image/ms-sharept-graph-alias-tile.png)

    7.  Click **Configure**.

        ![Configure button.](../image/MS-sharepoint-spoke-graph-configure-button.png)

    8.  On the form, fill these details.

<table id="table_ihs_m4s_g2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

The name of the connection record. The default and read-only name of the first connection record is MicrosoftSharePointGraph. To provide a custom name, you must create a connection record by clicking **Add connection**.

</td></tr><tr><td>

Connection URL

</td><td>

The URL to connect to the Microsoft Graph APIs. The URL is [https://graph.microsoft.com/v1.0](https://graph.microsoft.com/v1.0).

</td></tr><tr><td>

OAuth Entity Name

</td><td>

Name of the OAuth application that you created. To learn how to create an OAuth app, see [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that was generated when you created the OAuth app. To learn where to find the client ID, see [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that was generated when you created the OAuth app. To learn where to find the client ID, see [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

OAuth Authorization URL

</td><td>

The URL must be in the format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/authorize?response_mode=query`.**Tip:** To find the tenant ID, do the steps.

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).
2.  Under the Manage Azure Active Directory heading, select **View**.

The tenant ID is available under the Basic information heading.

![Tenant ID.](../image/MS-sharepoint-spoke-graph-tenant-ID.png)

</td></tr><tr><td>

OAuth Token URL

</td><td>

The URL must be in the format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`.**Tip:** To find the tenant ID, do the steps.

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).
2.  Under the Manage Azure Active Directory heading, select **View**.

The tenant ID is available under the Basic information heading.

![Tenant ID.](../image/MS-sharepoint-spoke-graph-tenant-ID.png)

</td></tr><tr><td>

Token Revocation URL

</td><td>

The URL must be in the format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`.**Tip:** To find the tenant ID, do the steps.

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).
2.  Under the Manage Azure Active Directory heading, select **View**.

The tenant ID is available under the Basic information heading.

![Tenant ID.](../image/MS-sharepoint-spoke-graph-tenant-ID.png)

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The URL must be in the format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>        ![Microsoft SharePoint Graph connection form.](../image/ms-sharept-graph-conn-form.png)

    9.  Select **Configure and Get OAuth Token**.

3.  Click **Configure and Get OAuth Token**.

    The connection record is created.

    ![Connection created.](../image/MS-sharepoint-spoke-graph-connection-created.png)

4.  To use the Microsoft Graph action, create a record in the Tenant table \(sn\_sp\_spoke\_tenant\) on your ServiceNow instance.

    **Note:** After you configure and get OAuth token, an application registry record is created with the details you have provided. In this application record, do not select any **OAuth API Script**.


