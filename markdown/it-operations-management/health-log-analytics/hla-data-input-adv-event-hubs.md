---
title: Configure advanced settings for Microsoft Azure Event Hubs data inputs in Health Log Analytics manually
description: Configure advanced settings for data inputs used for streaming log data from Microsoft Azure Event Hubs to your instance.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure advanced settings for Microsoft Azure Event Hubs data inputs in Health Log Analytics manually

Configure advanced settings for data inputs used for streaming log data from Microsoft Azure Event Hubs to your instance.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can set system parameters for reading log data that determine the actions that the system performs on log data arriving on the MID Server. For example, you can set the time zone to use if a log lacks a timestamp. If no advanced settings are configured, the system uses the default values.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  Open a Microsoft Azure Event Hubs data input record from the Data Inputs table.

    **Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

3.  Select **Advanced** and then select the **Advanced** tab.

4.  On the form, fill in the fields.

    For a description of the fields, see [Microsoft Azure Event Hubs data input configuration fields](../reference/hla-data-input-event-hubs-ref.md).

5.  In the Streaming Sources related list, verify that this data input is streaming log data from all relevant endpoint devices.

    For more information about streaming sources, see [Identify and resolve a log streaming issue in Health Log Analytics](hla-data-input-streaming.md).

6.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.

7.  Ensure that the data input is configured correctly by selecting **Test connection**.

    Health Log Analytics tries to connect the MID Server to the data repository.

    If the data input is configured to run on a MID Server cluster, the system tries to connect all the MID Servers contained in the cluster to the repository. The cluster passes the test if at least one of its MID Servers gets connected. This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

    -   If the connection was established, the **Test connection** button is turned off and the **Publish** button is enabled.
    -   If the connection failed, the reason for the failure displays in the **Error message** field. Resolve the issue, select **Save** if you modified the configuration, and then select **Test connection** to test the connection again.

        **Note:** You can only publish the data input configuration when the connection is created successfully.

    **Note:** You can revert to the last published configuration by selecting **Revert Changes**. This option is available only when you're modifying a configuration that has been published previously.

8.  Select **Publish** to publish the data input to the MID Server.


**Parent Topic:**[Advanced data input configuration in Health Log Analytics](../concept/hla-data-input-adv-configuration.md)

**Related topics**  


[Configure a Microsoft Azure Event Hubs data input in Health Log Analytics manually](hla-data-input-event-hubs.md)

