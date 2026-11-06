---
title: Set up the F5 BIG-IP spoke
description: Integrate the ServiceNow instance and F5 BIG-IP using basic authentication to authenticate ServiceNow requests.Configure a connection to your F5 BIG-IP server. The F5 BIG-IP spoke connection and credential aliases use these connections to perform actions in F5 BIG-IP.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/setup-f5-bigip.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-10-14"
reading_time_minutes: 1
breadcrumb: [F5 BIG-IP Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the F5 BIG-IP spoke

Integrate the ServiceNow instance and F5 BIG-IP using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the F5 BIG-IP spoke.
-   Role required: admin.

## Configure a connection for the F5 BIG-IP spoke

Configure a connection to your F5 BIG-IP server. The F5 BIG-IP spoke connection and credential aliases use these connections to perform actions in F5 BIG-IP.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **F5\_BIG\_IP** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the F5 BIG-IP spoke, click **View Details**.

        \[Omitted image "f5-bigip-connection.png"\] Alt text: Connection for the F5 BIG-IP spoke with View Details highlighted.

    -   To manage more than one F5 BIG-IP spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "f5-bigip-connection-conf.png"\] Alt text: Initial connection configuration with Configure highlighted.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Connection Name|Name to identify the F5 BIG-IP connection record.|
    |Connection URL|URL of the host machine where the F5 BIG-IP server is installed in this format: `https://<provider-domain-name>.com`. Replace `<provider-domain-name>` with the domain name of your F5 BIG-IP server.|
    |Credential Information|
    |User Name|User name for outbound authentication.|
    |Password|Password for outbound authentication.|

    \[Omitted image "f5-bigip-conf-temp.png"\] Alt text: Configure a connection for the F5 BIG-IP spoke.

6.  Click **Save**.


### Result

The F5 BIG-IP spoke connection is configured and ready to be used.

