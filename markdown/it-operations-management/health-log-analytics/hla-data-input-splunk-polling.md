---
title: Configure a Splunk Polling data input in Health Log Analytics manually
description: Set up a data input that periodically pulls log data from Splunk by using a query.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, Splunk, polling, query, data input, configuration]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a Splunk Polling data input in Health Log Analytics manually

Set up a data input that periodically pulls log data from Splunk by using a query.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md). If the MID Server and external clients are on the same network, connections can be made using the private IP address.
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Splunk Polling data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [Splunk Polling data input configuration fields](../reference/hla-data-input-splunk-polling-ref.md).

5.  Select **Advanced** to set additional configuration fields.

    On the **Transport tab** and **Advanced tab**, fill in the fields. For a description of the fields, see [Splunk Polling data input configuration fields](../reference/hla-data-input-splunk-polling-ref.md).

6.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

7.  Verify that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository. If the data input is configured to run on a MID Server cluster, the system tries to connect all the MID Servers contained in the cluster to the repository. The cluster passes the test if at least one of its MID Servers gets connected.

    **Note:** You can only publish the data input configuration when the connection is created successfully.

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.
    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

8.  Select **Publish** to publish the data input to the MID Server.


**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

