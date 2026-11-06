---
title: Set up Adobe Experience Platform spoke
description: Integrate your Adobe Experience Platform account with your ServiceNow instance.Configure a connection to your Adobe Experience Platform account. The Adobe Experience Platform spoke connection and credential alias uses this connection to perform actions in Adobe Experience Platform.Configure a connection to your Adobe Experience Platform account for data ingestion. The Adobe Experience Platform spoke connection and credential alias uses this connection to ingest data into Adobe Experience Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/setup-aep-spoke.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Adobe Experience Platform Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Adobe Experience Platform spoke

Integrate your Adobe Experience Platform account with your ServiceNow instance.

## Before you begin

-   Request Integration Hub subscription
-   Activate Adobe Experience Platform spoke
-   Role required: admin

## Configure a connection for the Adobe Experience Platform spoke

Configure a connection to your Adobe Experience Platform account. The Adobe Experience Platform spoke connection and credential alias uses this connection to perform actions in Adobe Experience Platform.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **AEP** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped with the Adobe Experience Platform spoke, click **View Details**.

        \[Omitted image "adobe-exp-connection.png"\] Alt text: Connection for the Adobe Experience Platform spoke

    -   To manage more than one Adobe Experience Platform connection record, create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "adobe-exp-connection-conf.png"\] Alt text: Initial connection configuration.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Connection Name|Name to identify the connection record. Defaults to `Adobe Experience Platform`.|
    |Connection URL|Base URL for the Adobe Experience Platform API. Defaults to `https://platform.adobe.io`.|
    |Sandbox|Name of the Adobe Experience Platform sandbox to use.|
    |API Key|Same value as the OAuth Client ID.|
    |Organization ID|IMS Organization ID, in the format: `<org_id>@AdobeOrg`.|
    |Credential Information|
    |Token URL|Token URL for Adobe Experience Platform. Defaults to `https://ims-na1.adobelogin.com/ims/token/v3`.|
    |OAuth Client ID|Client ID you created when registering your integration in the Adobe Developer Console.|
    |OAuth Client Secret|Client secret you created when registering your integration in the Adobe Developer Console.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    \[Omitted image "adobe-exp-conf-temp.png"\] Alt text: Configure a connection for the Adobe Experience Platform spoke.

6.  Click **Configure and Get OAuth Token**.


### Result

The Adobe Experience Platform spoke is set up and integrated with the ServiceNow instance.

**Note:** This alias uses the **Client Credentials** OAuth grant type by default. All flows, whether interactive or running in the background, use app-level permissions rather than an individual user's permissions to perform actions.

## Configure a connection for the Adobe Experience Platform data ingestion

Configure a connection to your Adobe Experience Platform account for data ingestion. The Adobe Experience Platform spoke connection and credential alias uses this connection to ingest data into Adobe Experience Platform.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **AEP\_Ingestion** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped with the Adobe Experience Platform spoke for data ingestion, click **View Details**.

        \[Omitted image "adobe-exp-ingestion-connection.png"\] Alt text: Connection for the Adobe Experience Platform ingestion spoke

    -   To manage more than one Adobe Experience Platform ingestion connection record, create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "adobe-exp-ingestion-connection-conf.png"\] Alt text: Initial connection configuration.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Connection Name|Name to identify the connection record. Defaults to `Adobe Experience Platform`.|
    |Connection URL|Base URL for the Adobe Experience Platform data ingestion API. Defaults to `https://dcs.adobedc.net`.|
    |Sandbox|Name of the Adobe Experience Platform sandbox to use.|
    |API Key|Same value as the OAuth Client ID.|
    |Organization ID|IMS Organization ID, in the format: `<org_id>@AdobeOrg`.|
    |Credential Information|
    |Token URL|Token URL for Adobe Experience Platform. Defaults to `https://ims-na1.adobelogin.com/ims/token/v3`.|
    |OAuth Client ID|Client ID you created when registering your integration in the Adobe Developer Console.|
    |OAuth Client Secret|Client secret you created when registering your integration in the Adobe Developer Console.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    \[Omitted image "adobe-exp-ingestion-conf-temp.png"\] Alt text: Configure a connection for the Adobe Experience Platform ingestion spoke.

6.  Click **Configure and Get OAuth Token**.


### Result

The Adobe Experience Platform ingestion spoke is set up and integrated with the ServiceNow instance.

**Note:** This alias uses the **Client Credentials** OAuth grant type by default. All flows, whether interactive or running in the background, use app-level permissions rather than an individual user's permissions to perform actions.

