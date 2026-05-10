---
title: Configure a Cribl data input in Health Log Analytics manually
description: Configure a dedicated Cribl data input to enable Health Log Analytics to process Cribl log messages streaming into your ServiceNow instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Cribl, data input, configuration, ServiceNow, Health Log Analytics, HLA]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a Cribl data input in Health Log Analytics manually

Configure a dedicated Cribl data input to enable Health Log Analytics to process Cribl log messages streaming into your ServiceNow instance.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerSystemRequirements.md).

    ![MID Server configuration with Log Ingestion capability enabled.](../../health-log-analytics-admin/image/hla-mid-log-ingestion.png)

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerProperties.md). If the MID Server and external clients are on the same network, connections can be made using the private IP address.

Role required: evt\_mgmt\_admin

## About this task

If your organization uses Cribl for filtering and routing large volumes of log data from various sources, the log format Health Log Analytics receives is distinct from other types. The Cribl data input enables HLA to detect and separate transport headers from inner log messages in this format, forwarding only the inner message to the source type structure for processing.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Cribl data input.

4.  On the **Getting Started** tab, fill in the form fields and then select **Next**.

    For a description of the fields, see [Cribl data input configuration fields](../../health-log-analytics-admin/reference/hla-data-input-cribl-ref.md).

5.  On the **Config** tab, fill in the form fields and then select **Next**.

    For a description of the fields, see [Cribl data input configuration fields](../../health-log-analytics-admin/reference/hla-data-input-cribl-ref.md).

6.  On the **Process** tab, select the required route and then select **Next**.

    For more information, see [Cribl data input configuration fields](../../health-log-analytics-admin/reference/hla-data-input-cribl-ref.md).

    **Note:** For troubleshooting issues related to this step, see the [Cribl - Setting up Cribl data input \| Troubleshooting setup &amp; data ingestion issues \[KB0558611\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1787528) article in the Now Support Knowledge Base.

    The **Finish** tab opens.

7.  On the Cribl instance, verify that the configuration of the data input is correct.

    You can use the Cribl commands displayed on the **Finish** tab as needed.

8.  When the configuration is correct, return to the data input configuration **Finish** tab and select **Publish** to publish the data input.


## Result

The data input configuration process is complete. The data input starts streaming log data to your ServiceNow instance.

For resolving issues related to the ingestion of log data from Cribl, see the [Cribl - Setting up Cribl data input \| Troubleshooting setup &amp; data ingestion issues \[KB0558611\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1787528) article in the Now Support Knowledge Base.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](../../health-log-analytics-admin/task/hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../../health-log-analytics-admin/concept/hla-data-inputs-configuring.md)

