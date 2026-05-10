---
title: Configure a TCP data input in Health Log Analytics manually
description: Set up a data input for sending raw log messages to your ServiceNow instance directly over a TCP/SSL socket.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a TCP data input in Health Log Analytics manually

Set up a data input for sending raw log messages to your ServiceNow instance directly over a TCP/SSL socket.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md). If the MID Server and external clients are on the same network, connections can be made using the private IP address.
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

**Note:** For information about streaming data from Logstash to your instance, see the [Streaming data from Logstash to your HLA instance](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0994735) \[KB0994735\] article in the Now Support knowledge base.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the TCP data input type.

    **Note:** The selected data input type complements the passive data input \(listener\). For more information, see [Supported data inputs for Health Log Analytics](../reference/hla-data-input-supported.md).

4.  On the form, fill in the fields.

    For a description of the fields, see [TCP data input configuration fields](../reference/hla-data-input-tcp-ref.md).

5.  Select **Advanced** to set additional configuration fields.

    For a description of the fields, see [TCP data input configuration fields](../reference/hla-data-input-tcp-ref.md). For information about configuring the advanced settings later, see [Configure advanced settings for Rsyslog, Splunk, or TCP data inputs in Health Log Analytics manually](hla-data-input-adv-rsyslog-splunk.md).

6.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

7.  Verify that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

8.  Select **Publish** to publish the data input to the MID Server.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts sending raw log messages to your ServiceNow instance directly over a TCP/SSL socket.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

**Related topics**  


[Configure advanced settings for Rsyslog, Splunk, or TCP data inputs in Health Log Analytics manually](hla-data-input-adv-rsyslog-splunk.md)

