---
title: Configure Adobe Acrobat Sign for external content indexing
description: Create and authorize an OAuth 2.0 application in Adobe Acrobat Sign to allow the Adobe Acrobat Sign external content connector to access your Adobe Acrobat Sign source system.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-01-27"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Adobe Acrobat Sign external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure Adobe Acrobat Sign for external content indexing

Create and authorize an OAuth 2.0 application in Adobe Acrobat Sign to allow the Adobe Acrobat Sign external content connector to access your Adobe Acrobat Sign source system.

## Before you begin

You need to be an administrator in the Adobe Acrobat Sign.

Role required: none

## About this task

The Adobe Acrobat Sign external content connector retrieves documents from agreements in your Adobe Acrobat Sign source system using the Adobe Acrobat Sign REST API.

To allow the connector to access your Adobe Acrobat Sign content via the REST API, you must configure and authorize an API application with OAuth 2.0 in Adobe Acrobat Sign. Your connector admin can use settings copied from this application to configure the Adobe Acrobat Sign external connector for proper connection to your source system.

## Procedure

1.  In Adobe Acrobat Sign, create a new API application for the Adobe Acrobat Sign external content connector.

    1.  Navigate to your Adobe Acrobat Sign instance and log in with administrator credentials.

    2.  In the application menu, select **API**.

        If the **API** menu item isn't visible, select **Account** instead.

    3.  In the account menu, navigate to **Adobe Sign API** &gt; **API Applications**.

    4.  Select the Create icon ![](../image/adobe-acrobat-sign-api-apps-plus-icon.png).

    5.  On the Create form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name for your API application. As an example, you might enter **ServiceNow external content connector**.|
        |Display Name|Display name for your API application. As an example, you might enter **ServiceNow external content connector**.|
        |Domain|Domain for your API application. Select **CUSTOMER**.|

    6.  Select **Save**.

    Adobe Acrobat Sign creates your new API application.

2.  Copy the application ID and secret for your new API application.

    1.  On the API Applications page, copy the application ID for your new API application and store it in a secure location.

        **Important:** Your external content connector admin needs this application ID when configuring the Adobe Acrobat Sign external content connector.

    2.  Select the API Applications entry for your new API application.

        The action menu for your new API application appears.

    3.  In the action menu, select **View/Edit**.

    4.  Copy the application secret for your new API application and store it in a secure location.

        **Important:** Your external content connector admin needs this application secret when configuring the Adobe Acrobat Sign external content connector.

3.  Configure OAuth 2.0 settings for your new API application.

    1.  On the API Applications page, select the entry for your new API application.

        The action menu for your new API application appears.

    2.  In the action menu, select **Configure OAuth for Application**.

    3.  On the Configure OAuth form, fill in the fields.

<table id="table_jrv_zd3_zhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Redirect URI

</td><td>

Enter `https://<instance-name>.service-now.com/oauth_redirect.do`, replacing `<instance-name>` with your ServiceNow AI Platform instance name.

</td></tr><tr><td>

Enabled Scopes

</td><td>

For each of the following scopes, select the **Enabled?** option and set the **Modifier** to **account**:-   user\_read
-   agreement\_read


</td></tr></tbody>
</table>
## What to do next

Provide the following items to your connector admin:

-   The base URL for your Adobe Acrobat Sign instance. This URL is typically `https://<host>.<data-center>.adobesign.com/`, where `<host>` is `secure` or your organization name and `<data-center>` is the shard ID for your Adobe Acrobat Sign data center. For a list of Adobe Acrobat Sign data centers, see [https://helpx.adobe.com/sign/using/adobesign-data-centers.html](https://helpx.adobe.com/sign/using/adobesign-data-centers.html).
-   The API application ID that you copied in step [2.a](configure-adobe-acrobat-sign-external-content-indexing.md#copy-app-id-step).
-   The API application secret that you copied in step [2.d](configure-adobe-acrobat-sign-external-content-indexing.md#copy-app-secret-step).

Your connector admin needs these items to configure an Adobe Acrobat Sign external content connector to retrieve documents and security principals from your Adobe Acrobat Sign source system.

For details on creating and configuring a Adobe Acrobat Sign external content connector, see [Create an Adobe Acrobat Sign external content connector](create-ext-cont-connector-adobe-acrobat-sign.md).

**Parent Topic:**[Adobe Acrobat Sign external content connector](../concept/adobe-acrobat-sign-external-content-connector.md)

