---
title: Configure a connection for the Jamf spoke
description: Configure a connection to your Jamf instance. The Jamf spoke connection and credential aliases use these connections to perform actions in Jamf.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/jamf-conctn-config.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 1
breadcrumb: [Set up the Jamf spoke, Jamf Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure a connection for the Jamf spoke

Configure a connection to your Jamf instance. The Jamf spoke connection and credential aliases use these connections to perform actions in Jamf.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Jamf** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Jamf spoke, click **View Details**.

        \[Omitted image "jamf-connection.png"\] Alt text: Connection for the Jamf spoke with View Details highlighted.

    -   To manage more than one Jamf spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "jamf-connection-conf.png"\] Alt text: Initial connection configuration with Configure highlighted.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Connection Name|Name to identify the Jamf connection record.|
    |Connection URL|Base URL to connect to your Jamf instance in this format: `https://<Instance-name>.jamfcloud.com/`.|
    |Credential Information|
    |Credential Name|Name to identify the credential record.|
    |User Name|User name of the Jamf account.|
    |Password|Password of the Jamf account.|
    |Connection URL|Base URL to connect to your Jamf instance in this format: `https://<Instance-name>.jamfcloud.com/`.|

    \[Omitted image "jamf-conf-temp.png"\] Alt text: Configure a connection for the Jamf spoke.

6.  Click **Save**.


## Result

The Jamf spoke connection is configured and ready to be used.

