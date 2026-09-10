---
title: Create a connection record for the Asana spoke
description: Create a connection record with all the details needed to integrate your ServiceNow instance to the Asana instance. When your ServiceNow instance requests a connection, the OAuth app you had set up authenticates the request based on the details in the connection record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/create-a-connection-record.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-08-13"
reading_time_minutes: 1
breadcrumb: [Set up the Asana spoke, Asana Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create a connection record for the Asana spoke

Create a connection record with all the details needed to integrate your ServiceNow instance to the Asana instance. When your ServiceNow instance requests a connection, the OAuth app you had set up authenticates the request based on the details in the connection record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Asana** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Asana spoke, click **View Details**.

        \[Omitted image "asana-conf-temp.png"\] Alt text:

    -   To manage more than one Asana spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "asna-configure.png"\] Alt text:

5.  On the form, fill in these fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection established with the Asana instance. The first connection's default name is automatically assigned to match the name specified in the Connections and Credentials form on the Connection &amp; Credential Aliases page. To provide your custom name, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL your ServiceNow instance uses to connect to the Asana instance.|
    |OAuth Client ID|The client ID that you had generated while you set up the OAuth application.|
    |OAuth Client Secret|The client secret that you had generated while you set up the OAuth application.|
    |OAuth Redirect URL|The redirect URL that the OAuth application uses to redirect to your ServiceNow instance. The URL must be in the format `https://<your instance name>.service-now.com/oauth_redirect.do`.|

    \[Omitted image "asana-configure-template.png"\] Alt text:

6.  Click **Configure and Get OAuth Token**.

    The OAuth application authenticates the connection request and provides a temporary token to access the Asana instance.


