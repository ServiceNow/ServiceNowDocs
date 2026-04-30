---
title: Set up the Plivo spoke
description: Integrate the ServiceNow instance and Plivo account by using the basic authentication to authenticate ServiceNow requests.Add and configure a Plivo connection to authenticate ServiceNow requests in Plivo spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Plivo Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Plivo spoke

Integrate the ServiceNow instance and Plivo account by using the basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Plivo spoke.
-   Role required: admin.

## Configure a connection for the Plivo spoke

Add and configure a Plivo connection to authenticate ServiceNow requests in Plivo spoke.

### Before you begin

-   Values of **AUTH ID** and **AUTH TOKEN**. You can find these vales in the dashboard of your Plivo account. For more information, see [Authentication](https://www.plivo.com/docs/account/api/request#authentication) in the [Plivo documentation](https://www.plivo.com/docs/).
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Plivo** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Plivo spoke, click **View Details**.

        ![Connection for Plivo spoke.](../image/plivo-connection.png)

    -   To manage more than one Plivo spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![First-time connection configuration of the Plivo spoke.](../image/plivo-conf-connection.png)

5.  On the **Configure Connection** form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record.|
    |Connection URL|Base URL to connect to Plivo. Enter `https://api.plivo.com`.|
    |Auth ID|Auth ID of your Plivo account.|
    |API Version|API version of your Plivo account. Enter `v1`.|
    |User name|Auth ID of your Plivo account.|
    |Password|Auth token of your Plivo account.|

    ![Configure a connection for the Plivo spoke.](../image/plivo-configured-connection.png)

6.  Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.

