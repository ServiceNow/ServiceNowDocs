---
title: Configure a connection for the Smartsheet spoke
description: Configure a connection to your Smartsheet account. The Smartsheet spoke connection and credential aliases use these connections to perform actions in Smartsheet.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/smartsheet-conctn-config.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-15"
reading_time_minutes: 1
breadcrumb: [Set up the Smartsheet spoke, Smartsheet Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure a connection for the Smartsheet spoke

Configure a connection to your Smartsheet account. The Smartsheet spoke connection and credential aliases use these connections to perform actions in Smartsheet.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Smartsheet** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Smartsheet spoke, click **View Details**.

        \[Omitted image "smartsheet-connection.png"\] Alt text: Connection for the Smartsheet spoke with View Details highlighted.

    -   To manage more than one Smartsheet spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "smartsheet-connection-conf.png"\] Alt text: Initial connection configuration with Configure highlighted.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Name|Name to identify the Smartsheet connection record.|
    |Connection URL|Connection URL. Default value: `https://api.smartsheet.com/`.|
    |Credential Information|
    |API Key|API key generated in your Smartsheet account.|

    \[Omitted image "smartsheet-conf-temp.png"\] Alt text: Configure a connection for the Smartsheet spoke.

6.  Click **Save**.


## Result

The Smartsheet spoke connection is configured and ready to be used.

