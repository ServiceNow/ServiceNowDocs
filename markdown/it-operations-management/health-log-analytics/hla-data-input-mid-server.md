---
title: Configure data inputs \(MID Server\)
description: Configure a data input for collecting and streaming MID Server log messages to your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure data inputs \(MID Server\)

Configure a data input for collecting and streaming MID Server log messages to your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.

## Before you begin

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the MID Server IP address is exposed by network address translation \(NAT\), a load balancer, or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).
-   For shipping your logs encrypted using SSL TLS, see the [Streaming Data With Rsyslog &amp; Filebeat Using SSL \[KB0866319\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0866319) article in the Now Support Knowledge Base.

Role required: evt\_mgmt\_admin

## About this task

This procedure describes how to create a MID Server data input from the Data Inputs page.

Alternatively, you can create a data input for a specific MID Server from the MID Server form: Navigate to the MID Servers page, select a MID Server, and then select the **Create MID Server Data Input using HLA** related link. Define the data input configuration to complete the process.

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

    On the form, fill in the fields. For a description of the fields, see [MID Server data input configuration fields](../reference/hla-data-input-mid-server-ref.md). For information about configuring the advanced settings later, see [Configure advanced settings for MID Server data inputs](hla-data-input-adv-mid-server.md).

6.  Select **Submit**.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts collecting and streaming MID Server log messages to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

-   **[MID Server data input configuration fields](../reference/hla-data-input-mid-server-ref.md)**  
Description of the fields on the MID Server data input configuration form.

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

