---
title: Configure a Vector Agent data input in Health Log Analytics manually
description: Set up a Vector Agent data input to enable Health Log Analytics to process log messages that are streaming into your ServiceNow instance via a Vector Agent.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [ServiceNow, Health Log Analytics, HLA, Vector Agent, data input, configuration]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a Vector Agent data input in Health Log Analytics manually

Set up a Vector Agent data input to enable Health Log Analytics to process log messages that are streaming into your ServiceNow instance via a Vector Agent.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    ![MID Server configuration with Log Ingestion capability enabled.](../image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=australia&pubname=australia-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US). If the MID Server and external clients are on the same network, connections can be made using the private IP address.

-   Verify that you have a `vector.yaml` file on your system, or create one.

Role required: evt\_mgmt\_admin

## About this task

If your organization uses Vector by Datadog to handle log data from multiple sources before sending it to Health Log Analytics, the log format HLA receives is distinct from other types. The Vector Agent data input enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose **Vector - Stream logs from Vector Agent**.

4.  On the **Getting Started** tab, fill in the form and then select **Next**.

    For a detailed description of the fields, see [Vector Agent data input configuration fields](../reference/hla-data-input-vector-agent-ref.md).

5.  On the **vector.yaml** tab, update the code with the relevant values as needed.

    For example, you can specify the sources or source file from which the logs will be streamed.

    **Note:** Code that you should not modify is preceded by a commented note.

    For more information, consult [the Vector documentation](https://vector.dev/docs/).

6.  Copy the updated code and paste it into the `vector.yaml` file on your system.

7.  Select **Next**.

    The **Finish** tab displays a message confirming that the data input configuration process is complete.

8.  Start streaming log data by running Vector with the configuration file.

    Run the following command:`vector --config /path/to/your/vector.yaml`, where `/path/to/your/` is the actual path to your YAML file.

9.  Use the other commands displayed on the **Finish** tab as needed.

10. Select **Save** to save the data input.


## Result

Health Log Analytics adds the data input record to the **Data Inputs** table. The data input starts streaming log data to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

