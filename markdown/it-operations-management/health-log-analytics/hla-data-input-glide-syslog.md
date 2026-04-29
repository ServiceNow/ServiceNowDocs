---
title: Configure a ServiceNow System Logs Retriever data input in Health Log Analytics manually
description: Set up a data input for streaming log data from the ServiceNow System Log table to the HLA engine \(aka Occultus\).
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, data input, configuration]
breadcrumb: [Manual data input configuration, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Configure a ServiceNow System Logs Retriever data input in Health Log Analytics manually

Set up a data input for streaming log data from the ServiceNow System Log table to the HLA engine \(aka Occultus\).

## Before you begin

**Note:** Only a single ServiceNow System Logs Retriever data input can exist in the system. This data input doesn't run on a MID Server.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the ServiceNow System Logs Retriever data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [ServiceNow System Logs Retriever data input configuration fields](../reference/hla-data-input-glide-syslog-ref.md).

5.  Select **Save**.

    Health Log Analytics adds the data input record to the Data Inputs table.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record.

The data input starts streaming ServiceNow log data from the System Log table to the Health Log Analytics AI engine, based on the configured filters. Admin users can set filters to query the System Log table. Operators can monitor the logs and view the alerts that Health Log Analytics generates from them.

For a description of how this data input can help you detect and resolve emerging issues in your organization's ServiceNow instance, see [Use Case: Proactive monitoring of your ServiceNow instance in Health Log Analytics](../../health-log-analytics-operator/concept/hla-use-case-syslogs.md).

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

