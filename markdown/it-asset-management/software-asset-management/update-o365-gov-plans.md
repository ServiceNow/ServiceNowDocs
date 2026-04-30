---
title: Update REST and OAuth endpoints for Microsoft Office 365 Government plans
description: Change the endpoints of the REST message and OAuth application on your ServiceNow subscription profile so that you can use your subscriptions.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrating with Microsoft 365, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Update REST and OAuth endpoints for Microsoft Office 365 Government plans

Change the endpoints of the REST message and OAuth application on your ServiceNow subscription profile so that you can use your subscriptions.

## Before you begin

Role required: sam\_admin

## About this task

The ServiceNow AI Platform® supports Microsoft Office 365 Government plans, which provide all the features and capabilities of Microsoft 365 services in a segmented government cloud community that enables organizations to meet U.S. compliance and security standards.

For more information on Microsoft Office 365 Government plans, see [Office 365 Government](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government).

**Important:** The Software Asset Management application supports tracking last activity for license compliance, subscription management, and optimization recommendations for Microsoft products such as Exchange Online, Teams, Power BI, OneDrive, and so on. For more details, see [Evaluating software usage activity for Microsoft 365 subscriptions](../concept/o365-usage-activity.md).

The detailed usage metrics for these Microsoft products \(except Power BI\) are only available through specific report APIs that aren't supported in government-regulated environments. For further details, refer to the [Microsoft national cloud deployments documentation](https://learn.microsoft.com/en-us/graph/api/reportroot-getm365appuserdetail?view=graph-rest-1.0&tabs=http).

## Procedure

1.  From your ServiceNow instance, navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.

2.  Select the Microsoft 365 integration profile that you want to update.

3.  On the Integration Profile record, select the Preview this record icon ![](../image/preview-icon.png)next to the **REST message** field.

4.  On the record preview, select **Open Record**.

    The REST Message record opens.

5.  Update the REST message endpoints on your Microsoft 365 integration profile.

    REST message endpoints enable you to retrieve usage data from your Microsoft 365 applications and services.

    1.  In the **HTTP Methods** related list, update the REST message endpoints based on your needs.

        Microsoft provides various endpoints for Microsoft Office 365 Government plans. For more information on the available endpoints, see [Office 365 U.S. Government GCC High endpoints](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-u-s-government-gcc-high-endpoints?view=o365-worldwide).

        **Important:** You must change the `.com` to `.us` in the URL of each endpoint. For example, you must change `https://graph.microsoft.com/v1.0/reports` to `https://graph.microsoft.us/v1.0/reports`.

    2.  Select **Save**.

    3.  Update the OAuth entity scope for the **GET PowerBI Usage** endpoint.

        The OAuth entity scope specifies the level of access that users have to your protected resources.

        1.  Select the **GET PowerBI Usage** endpoint.

            The HTTP Method record opens.

        2.  In the Authentication section of the HTTP Method record, select the Preview this record icon ![](../image/preview-icon.png) next to the **OAuth profile** field.
        3.  On the record preview, select **Open Record**.

            The OAuth Entity Profile record opens.

        4.  In the OAuth Entity Profile Scopes list, update the **OAuth scope** field of the **PowerBIPermissions** OAuth entity scope with the backend API URL that you’re using for Microsoft Power BI.

            **Note:** Microsoft supports various backend API URLs for Power BI. For more information on the available URLs, see [Power BI for US Government](https://learn.microsoft.com/en-us/power-bi/enterprise/service-govus-overview).

        5.  Select **Update**.

            The OAuth Entity Profile record closes and you automatically return to the REST Message record.

6.  Update the OAuth application endpoint on your Microsoft 365 integration profile.

    The OAuth application endpoint enables your ServiceNow instance to access your Microsoft 365 subscription data.

    1.  In the Authentication section of the REST Message record, select the Preview this record icon ![](../image/preview-icon.png) next to the **OAuth profile** field.

    2.  On the record preview, select **Open Record**.

        The OAuth Entity Profile record opens.

    3.  In the OAuth Entity Profile Scopes list, change the `.com` to `.us` in the URL that is listed in the **OAuth scope** field of the **Permissions** OAuth entity scope.

    4.  Select the Preview this record icon ![](../image/preview-icon.png) next to the **OAuth provider** field.

    5.  On the record preview, select **Open Record**.

        The Application Registries record opens.

    6.  Select the Edit URL icon ![](../../../reuse/icons/product-icons/lock-outline-24.svg) next to the **Token URL** field.

    7.  In the URL, change the `.com` to `.us`.

        For example, change `https://login.microsoftonline.com` to `https://login.microsoftonline.us`.

    8.  Select the Lock URL icon ![](../../../reuse/icons/product-icons/unlock-outline-24.svg).

    9.  Select **Update**.


## What to do next

Revalidate the connection and credential details of this integration. For more information, see [Create a Microsoft 365 integration profile](set-up-microsoft-office-365.md).

