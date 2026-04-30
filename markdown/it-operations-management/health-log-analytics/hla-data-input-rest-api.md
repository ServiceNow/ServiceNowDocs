---
title: Configure data inputs \(REST API\)
description: Configure a REST API data input for streaming log data to your ServiceNow instance in JSON format. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure data inputs \(REST API\)

Configure a REST API data input for streaming log data to your ServiceNow instance in JSON format. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.

## Before you begin

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

    On the MID Web Server Context form, in the **Execute on** field, select Specific MID Server and not the cluster option. In the **MID Server** field, select the specific MID Server to which the log data is pulled.

-   If the IP address of the MID Server is exposed by network address translation \(NAT\), a load balancer or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).

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

5.  Select **Submit**.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts streaming log data in JSON format to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

-   **[REST API data input configuration fields](../reference/hla-data-input-rest-api-ref.md)**  
Description of the fields on the REST API data input configuration form.

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

