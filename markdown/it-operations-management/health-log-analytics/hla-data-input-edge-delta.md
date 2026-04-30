---
title: Configure an Edge Delta data input in Health Log Analytics manually
description: Set up an Edge Delta data input to enable Health Log Analytics to process Edge Delta log messages streaming into your ServiceNow instance.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, Edge Delta, data input, configuration, setup]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure an Edge Delta data input in Health Log Analytics manually

Set up an Edge Delta data input to enable Health Log Analytics to process Edge Delta log messages streaming into your ServiceNow instance.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=zurich&pubname=zurich-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US). If the MID Server and external clients are on the same network, connections can be made using the private IP address.

Role required: evt\_mgmt\_admin

## About this task

If your organization uses Edge Delta to handle large volumes of log data from multiple sources before sending it to Health Log Analytics, the log format HLA receives is distinct from other types. The Edge Delta data input enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Edge Delta data input.

4.  On the form, fill in the fields.

    For a detailed description of the fields, see [Edge Delta data input configuration fields](../reference/hla-data-input-edge-delta-ref.md).

5.  Select **Save** to save your configuration.

6.  Select **Publish** to publish the data input.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table. The data input starts streaming log data to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

