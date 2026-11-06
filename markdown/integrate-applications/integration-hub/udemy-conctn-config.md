---
title: Configure a connection for the Udemy spoke
description: Configure a connection to your Udemy account. The Udemy spoke connection and credential aliases use these connections to perform actions in Udemy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/udemy-conctn-config.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Set up the Udemy spoke, Udemy Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure a connection for the Udemy spoke

Configure a connection to your Udemy account. The Udemy spoke connection and credential aliases use these connections to perform actions in Udemy.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Udemy** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Udemy spoke, click **View Details**.

        \[Omitted image "udemy-connection.png"\] Alt text: Connection for the Udemy spoke with View Details highlighted.

    -   To manage more than one Udemy spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "udemy-connection-conf.png"\] Alt text: Initial connection configuration with Configure highlighted.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Connection Name|Name to identify the Udemy connection record. Default value: `Udemy Connection`.|
    |Connection URL|URL of your Udemy domain in this format: `https://<provider-domain-name>.com`. Replace `<provider-domain-name>` with the domain name of your Udemy account.|
    |Domain Name|Domain name of your Udemy account.|
    |Domain ID|Domain ID of your Udemy account.|
    |API Version|Version of the Udemy API. Default value: `api-2.0`.|
    |Credential Information|
    |API Key|API key generated in your Udemy account.|
    |Credential Name|Name to identify the Udemy credential record. Default value: `Udemy Credentials`.|

    \[Omitted image "udemy-conf-temp.png"\] Alt text: Configure a connection for the Udemy spoke.

6.  Click **Save**.


## Result

The Udemy spoke connection is configured and ready to be used.

