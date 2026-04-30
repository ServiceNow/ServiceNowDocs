---
title: Configure advanced settings for MID Server data inputs
description: Configure advanced settings for data inputs that are used for collecting and streaming MID Server log messages.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Advanced data input configuration, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Configure advanced settings for MID Server data inputs

Configure advanced settings for data inputs that are used for collecting and streaming MID Server log messages.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

You can set system parameters for reading log data that determine the actions that the system performs on log data arriving on the MID Server. For example, you can set the time zone to use if a log lacks a timestamp. If no advanced settings are configured, the system uses the default values.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  Open a MID Server data input record from the Data Inputs table.

    The data input configuration displays.

    **Note:** The number of log sources that the data input has created is shown in the **Sources count** field. For more information about data input sources, see [Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md).

    **Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

3.  Select **Advanced**.

4.  On the form, fill in the fields.

    For a description of the fields, see [MID Server data input configuration fields](../reference/hla-data-input-mid-server-ref.md).

5.  In the Streaming Sources related list, verify that this data input is streaming log data from all relevant endpoint devices.

    For more information about streaming sources, see [Identify and resolve log streaming issues](hla-data-input-streaming.md).

6.  Select **Update**.


## Result

Health Log Analytics updates the system parameters.

**Parent Topic:**[Advanced data input configuration](../concept/hla-data-input-adv-configuration.md)

**Related topics**  


[Configure data inputs \(MID Server\)](hla-data-input-mid-server.md)

