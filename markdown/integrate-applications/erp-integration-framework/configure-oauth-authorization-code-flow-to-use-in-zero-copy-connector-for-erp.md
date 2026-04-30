---
title: Configure OAuth authorization code flow to use in Zero Copy Connector for ERP
description: Configure OAuth authorization code flow for SAP and use OAuth to authenticate and authorize users for OData endpoints.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, oauth, odata, configure, code, provider]
breadcrumb: [Connect to SAP with OData and HTTP, Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Configure OAuth authorization code flow to use in Zero Copy Connector for ERP

Configure OAuth authorization code flow for SAP and use OAuth to authenticate and authorize users for OData endpoints.

## Before you begin

Role required: admin

**Note:** The OAuth authorization code flow can be used to call OData endpoints \(create, read, and update\). At this time, OAuth cannot be used for tables, BAPI, or RFC.

To understand OAuth, see [Set up OAuth](https://www.servicenow.com/docs/access?context=t_SettingUpOAuth&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and [OAuth inbound](https://www.servicenow.com/docs/access?context=oauth-inbound&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Consult with your SAP administrator:

-   Obtain the client ID and client secret. You need this information for the application registry form.
-   Ask if the refresh token is a one-time usable token. A scheduled job that retrieves information from SAP runs once per day. If you need to run the scheduled job more often or on demand, discuss the access token and refresh token options. For more information, see [Manage OAuth tokens](https://www.servicenow.com/docs/access?context=t_ManageTokens&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   Ask them to enable the gateway services to expose the OData endpoints you want to use.
-   Ask them to create a scope in SAP for the exposed OData endpoints and give you the name and OAuth scope. You need this to configure the scope on the application registry form.

## Procedure

1.  If you have already set up OAuth \(for example, with REST via platform features\), you can use it in Zero Copy Connector for ERP and skip to step 3.

2.  To set up OAuth, register your application by navigating to **All** &gt; **System OAuth** &gt; **Application Registry**.

    1.  Select **New**.

    2.  Select **Connect to a third party OAuth Provider**

        Use this form to set SAP as the OAuth provider and ServiceNow as the OAuth client. For detailed information about the fields on this form, see [Connect to a third-party OAuth provider](https://www.servicenow.com/docs/access?context=connect-3rd-party-oauth-provider&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    3.  Enter a **Name**.

    4.  Set ServiceNow as the OAuth client by using the information you obtained from your SAP administrator to fill in the **Client ID** and **Client Secret** fields.

    5.  In **Default Grant type**, specify how to authenticate SAP.

    6.  Unlock the **Authorization URL** and **Token URL** fields to enter the URLs.

        ![Application registry form with fields containing information.](../image/erp-oauth-usage-flow1.png)

    7.  Select the **OAuth Entity Scopes** tab.

    8.  Double-click in the **Name** and **OAuth scope** columns to enter the scope information you obtained from your SAP administrator.

        You can add multiple scopes.

        ![OAuth entity scopes tab on the application registry form.](../image/erp-oauth-usage-flow2.png)

    9.  Select **Submit**.

3.  Create a credential by navigating to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

    1.  Select **New**.

    2.  Select **OAuth 2.0 credentials**.

        For detailed information about the fields on this form, see [OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    3.  Enter a **Name**.

    4.  In **OAuth Entity Profile**, select **sap oauth profile default\_profile**.

    5.  In **Integration type**, select **Personal**.

        In most cases, it is acceptable to use system-based credentials. However, if you are trying to obtain information from SAP, such as who changed information or details about approval activities, use the personal integration type. For more information, see [Using the Personal Authentication dashboard](../../../administer/integrationhub/concept/personal-auth-dashboard.md).

        ![Oauth 2.0 credentials form with fields containing information.](../image/erp-oauth-usage-flow3.png)

    6.  Select **Submit**.

4.  Add a connection to the **Zero Copy Connector for ERP HTTP** alias by navigating to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

    1.  In **Name**, search for and select **Zero Copy Connector for ERP HTTP**.

    2.  On the **Connections** tab, select **New**.

        For detailed information about the fields on this form, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

    3.  Enter a **Name**.

    4.  In **Credential**, specify the OAuth credential you created in step 3.

    5.  Enter the **Connection URL**.

    6.  Select **Submit**.


**Parent Topic:**[Connect Zero Copy Connector for ERP to SAP using OData and HTTP](../concept/erp-canvas-use-odata-and-http-connection.md)

