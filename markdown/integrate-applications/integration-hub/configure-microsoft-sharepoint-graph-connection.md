---
title: Configure Microsoft SharePoint Graph connection
description: Configure a Microsoft SharePoint Graph connection and a connection record that enable your ServiceNow instance to integrate with the Microsoft SharePoint using the Microsoft Graph.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/configure-microsoft-sharepoint-graph-connection.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
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

        \[Omitted image "MS-sharepoint-spoke-app-reg-button.png"\] Alt text: App registration button.

    3.  Select **All applications** or **Owned applications**.

        \[Omitted image "ms-sharepoint-spoke-graph-select-app.png"\] Alt text: OAuth application selection options.

    4.  In the search field, enter the name of the OAuth application you had created.

        To learn how to configure an OAuth application, see [Configure OAuth application in Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/configure-oauth-application-in-microsoft-azure.md).

    5.  In the search results, select the name of the OAuth application you had configured.

    6.  On the left panel, under the Manage heading, select API permissions.

        \[Omitted image "MS-sharepoint-spoke-graph-api-permissions-link.png"\] Alt text: API permissions link.

    7.  Under the Configured permissions heading, select **+ Add a permission**.

    8.  In the Request API permissions window, select **Microsoft Graph**.

        \[Omitted image "MS-sharepoint-spoke-graph-ms-graph-button.png"\] Alt text: Microsoft Graph button.

    9.  Select **Delegated permissions**.

    10. Under the Select permissions heading, enter `site` in the search field.

    11. Expand the Sites list.

        \[Omitted image "MS-sharepoint-spoke-graph-click-sites.png"\] Alt text: Sites list.

    12. Select `Sites.FullControl.all`, `Sites.Read.All` and `Sites.ReadWrite.All`.

        \[Omitted image "ms-sharepoint-online-spoke-graph-site-permissions.png"\] Alt text: Microsoft SharePoint Online spoke Graph Site permissions.

    13. Under the Select permissions heading, enter `User.read` in the search field.

        \[Omitted image "MS-SharePoint-Online-spoke-graph-user-permission.png"\] Alt text: Microsoft SharePoint Online spoke Graph User permissions.

    14. Select **Add permissions**.

        The permission is added.

        \[Omitted image "MS-sharepoint-spoke-graph-permissions-added.png"\] Alt text: Permissions added.

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

        \[Omitted image "ms-sharept-graph-alias-tile.png"\] Alt text: View Details button on Microsoft SharePoint Graph alias.

    7.  Click **Configure**.

        \[Omitted image "MS-sharepoint-spoke-graph-configure-button.png"\] Alt text: Configure button.

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

Name of the OAuth application that you created. To learn how to create an OAuth app, see [Configure OAuth application in Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that was generated when you created the OAuth app. To learn where to find the client ID, see [Configure OAuth application in Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that was generated when you created the OAuth app. To learn where to find the client ID, see [Configure OAuth application in Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/configure-oauth-application-in-microsoft-azure.md).

</td></tr><tr><td>

OAuth Authorization URL

</td><td>

The URL must be in the format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/authorize?response_mode=query`.**Tip:** To find the tenant ID, do the steps.

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).
2.  Under the Manage Azure Active Directory heading, select **View**.

The tenant ID is available under the Basic information heading.

\[Omitted image "MS-sharepoint-spoke-graph-tenant-ID.png"\] Alt text: Tenant ID.

</td></tr><tr><td>

OAuth Token URL

</td><td>

The URL must be in the format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`.**Tip:** To find the tenant ID, do the steps.

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).
2.  Under the Manage Azure Active Directory heading, select **View**.

The tenant ID is available under the Basic information heading.

\[Omitted image "MS-sharepoint-spoke-graph-tenant-ID.png"\] Alt text: Tenant ID.

</td></tr><tr><td>

Token Revocation URL

</td><td>

The URL must be in the format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`.**Tip:** To find the tenant ID, do the steps.

1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).
2.  Under the Manage Azure Active Directory heading, select **View**.

The tenant ID is available under the Basic information heading.

\[Omitted image "MS-sharepoint-spoke-graph-tenant-ID.png"\] Alt text: Tenant ID.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

The URL must be in the format: `https://<instance-name>.service-now.com/oauth_redirect.do`.

</td></tr></tbody>
</table>        \[Omitted image "ms-sharept-graph-conn-form.png"\] Alt text: Microsoft SharePoint Graph connection form.

    9.  Select **Configure and Get OAuth Token**.

3.  Click **Configure and Get OAuth Token**.

    The connection record is created.

    \[Omitted image "MS-sharepoint-spoke-graph-connection-created.png"\] Alt text: Connection created.

4.  To use the Microsoft Graph action, create a record in the Tenant table \(sn\_sp\_spoke\_tenant\) on your ServiceNow instance.

    **Note:** After you configure and get OAuth token, an application registry record is created with the details you have provided. In this application record, do not select any **OAuth API Script**.


