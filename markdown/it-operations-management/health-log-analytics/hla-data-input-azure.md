---
title: Configure Microsoft Azure Log Analytics data inputs
description: Configure a data input for streaming log data from Microsoft Azure Log Analytics to your ServiceNow instance. The data input points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Configuring data inputs for Health Log Analytics manually, Set up data inputs for Health Log Analytics manually, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure Microsoft Azure Log Analytics data inputs

Configure a data input for streaming log data from Microsoft Azure Log Analytics to your ServiceNow instance. The data input points the Health Log Analytics AI engine to a data source in your Microsoft Azure Log Analytics account.

## Before you begin

-   Verify that a MID Server is installed and configured with the Log Ingestion capability enabled. For more information, see [MID Server system requirements](https://www.servicenow.com/docs/access?context=r_MIDServerSystemRequirements&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    **Important:** Health Log Analytics does not support IPv6. To work with the application, configure the MID Server to IPv4.

-   Unless the MID Server and external clients are on the same network, the MID Server must have a public IP address. This is required when its IP is exposed through network address translation \(NAT\), a load balancer, or a similar device. The public IP address enables external clients, such as Filebeat agents located outside its network, to reach the MID Server. Private IP addresses are not routable over the internet. Without a public IP, external clients cannot connect to the MID Server even if they are configured with its address. In the MID Server properties, add a property named **mid.public\_ip** with the public IP address as the value. For more information, see [Create a MID Server property](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&section=t_SetMIDServerProperties&ft:locale=en-US). If the MID Server and external clients are on the same network, connections can be made using the private IP address.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Microsoft Azure Log Analytics data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [Microsoft Azure Log Analytics data input configuration fields](../reference/hla-data-input-azure-ref.md).

5.  Select **Advanced** to set additional configuration fields.

    For a description of the fields, see [Microsoft Azure Log Analytics data input configuration fields](../reference/hla-data-input-azure-ref.md). For information about configuring the advanced settings later, see [Configure advanced settings for Microsoft Azure Log Analytics data inputs](hla-data-input-adv-azure-la.md).

6.  On the **Query settings** tab, fill in the fields.

    Health Log Analytics uses the values set in these fields to generate the query for receiving log data from Microsoft Azure Log Analytics.

    For example:

    ```
    {"query": "ContainerLog | where TimeGenerated > %s | take 500", "project": ["TimeGenerated", "LogEntry", "LogEntrySource"]}
    ```

    where:

    -   `ContainerLog`: The data source name.
    -   `TimeGenerated`: The event time property name.
    -   `500`: The maximum number of rows retrieved in each query.
    -   `["TimeGenerated", "LogEntry", "LogEntrySource"]`: The event time and the comma-separated list of column names to return.
    Alternatively, you can configure a custom query in the **Log query** field. The value you set in this field overrides the values in all other fields on the **Query settings** tab except the **From** field. If the **Log query** field is empty, Health Log Analytics generates the query using the values set in the other fields on the tab.

    For a description of the **Query settings** fields, see [Microsoft Azure Log Analytics data input configuration fields](../reference/hla-data-input-azure-ref.md).

7.  On the **Transport** tab, fill in the fields.

    For a description of the fields, see [Microsoft Azure Log Analytics data input configuration fields](../reference/hla-data-input-azure-ref.md).

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

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record. The data input starts streaming log data from Microsoft Azure Log Analytics to your ServiceNow instance.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

**Related topics**  


[Configure advanced settings for Microsoft Azure Log Analytics data inputs](hla-data-input-adv-azure-la.md)

