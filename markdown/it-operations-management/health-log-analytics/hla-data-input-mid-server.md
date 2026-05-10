---
title: Configure a MID Server data input in Health Log Analytics manually
description: Set up a data input for collecting and streaming MID Server log messages to your ServiceNow instance.
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

# Configure a MID Server data input in Health Log Analytics manually

Set up a data input for collecting and streaming MID Server log messages to your ServiceNow instance.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md). If the MID Server and external clients are on the same network, connections can be made using the private IP address.
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

Role required: evt\_mgmt\_admin

## About this task

This procedure describes how to create a MID Server data input from the Data Inputs page. To configure the MID Server data input automatically, click the related link on the MID Server form.

**Important:**

-   When you create a MID Server data input, all logs are automatically mapped to the predefined mid\_server\_log source type. This source type includes preconfigured mapping settings to maximize the value of monitoring your MID Server logs. To review the mapping script, navigate directly from the data input configuration form to the mapping form by selecting **Go to Mapping** under Related Links. Review the source type by navigating to Source Type Structures and select the mid\_server\_log source type.
-   For optimal performance, debug MID Server log messages are not processed by default. If you want to send debug messages to Health Log Analytics for processing, add the following to your MID Server properties: mid.hla.mid\_data\_input.ignore\_debug\_level\_logs = false.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the MID Server data input.

4.  On the form, provide a description of the data input and the name of the MID Server from which the logs are streamed.

    For a description of the fields, see [MID Server data input configuration fields](../reference/hla-data-input-mid-server-ref.md).

5.  Select **Advanced** to set additional configuration fields.

    On the form, fill in the fields. For a description of the fields, see [MID Server data input configuration fields](../reference/hla-data-input-mid-server-ref.md). For information about configuring the advanced settings later, see [Configure advanced settings for MID Server data inputs in Health Log Analytics manually](hla-data-input-adv-mid-server.md).

6.  Select **Submit**.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts collecting and streaming MID Server log messages to your ServiceNow instance.

For a description of how this data input can help you detect and resolve emerging issues in your organization's ServiceNow instance, see [Use Case: Proactive monitoring of your ServiceNow instance in Health Log Analytics](../../health-log-analytics-operator/concept/hla-use-case-syslogs.md).

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

