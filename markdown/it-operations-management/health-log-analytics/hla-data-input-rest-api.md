---
title: Configure REST API data inputs
description: Configure a REST API data input for streaming log data to your ServiceNow instance in JSON format.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure REST API data inputs

Configure a REST API data input for streaming log data to your ServiceNow instance in JSON format.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

    On the MID Web Server Context form, in the **Execute on** field, select Specific MID Server and not the cluster option. In the **MID Server** field, select the specific MID Server to which the log data is pulled.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US). If the MID Server and external clients are on the same network, connections can be made using the private IP address.

Role required: evt\_mgmt\_admin

## About this task

The extension handles log messages that are sent to the MID Server by an external log source. The MID Server processes the messages and then passes them to your instance.

To stream log messages to the MID Server, the URL must have the format `http://{MID_SERVER_IP}:{MID_WEB_SERVER_PORT}/api/mid/hla/raw`, where `/api/mid/hla/raw` is the endpoint.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the REST API data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [REST API data input configuration fields](../reference/hla-data-input-rest-api-ref.md).

    **Note:** REST API integrations support only UTF-8 encoding for incoming data.

5.  Select **Submit**.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts streaming log data in JSON format to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

