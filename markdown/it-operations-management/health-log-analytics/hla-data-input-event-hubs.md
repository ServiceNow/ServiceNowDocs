---
title: Configure data inputs \(Microsoft Azure Event Hubs\)
description: Configure a data input for streaming events from Microsoft Azure Event Hubs to your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.
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

# Configure data inputs \(Microsoft Azure Event Hubs\)

Configure a data input for streaming events from Microsoft Azure Event Hubs to your ServiceNow instance. Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.

## Before you begin

-   Ensure that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   If the IP address of the MID Server is exposed by network address translation \(NAT\), a load balancer or a similar device, it must have a public IP address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Microsoft Azure Event Hubs data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [Microsoft Azure Event Hubs data input configuration fields](../reference/hla-data-input-event-hubs-ref.md).

5.  Select **Advanced** to set additional configuration fields.

    For a description of the fields, see [Microsoft Azure Event Hubs data input configuration fields](../reference/hla-data-input-event-hubs-ref.md). For information about configuring the advanced settings later, see [Configure advanced settings for Microsoft Azure Event Hubs data inputs](hla-data-input-adv-event-hubs.md).

6.  On the **Query settings** tab, fill in the fields.

    For a description of the fields, see [Microsoft Azure Event Hubs data input configuration fields](../reference/hla-data-input-event-hubs-ref.md).

7.  On the **Transport** tab, fill in the fields.

    For a description of the fields, see [Microsoft Azure Event Hubs data input configuration fields](../reference/hla-data-input-event-hubs-ref.md).

8.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

9.  Ensure that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    If the data input is configured to run on a MID Server cluster, the system tries to connect all the MID Servers contained in the cluster to the repository. The cluster passes the test if at least one of its MID Servers gets connected. This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

10. Select **Publish** to publish the data input to the MID Server.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts streaming log data from Microsoft Azure Event Hubs to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

-   **[Microsoft Azure Event Hubs data input configuration fields](../reference/hla-data-input-event-hubs-ref.md)**  
Description of the fields on the Microsoft Azure Event Hubs data input configuration form.

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

**Related topics**  


[Configure advanced settings for Microsoft Azure Event Hubs data inputs](hla-data-input-adv-event-hubs.md)

