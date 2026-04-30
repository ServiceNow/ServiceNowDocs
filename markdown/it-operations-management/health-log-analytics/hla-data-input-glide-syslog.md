---
title: Configure data inputs \(Glide Syslog\)
description: Configure a data input for streaming log data from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\). Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.
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

# Configure data inputs \(Glide Syslog\)

Configure a data input for streaming log data from the System Log table \(Glide Syslog\) in Glide to the Health Log Analytics AI engine \(Occultus\). Data input configuration is an essential step in setting up the Health Log Analytics \(HLA\) application.

## Before you begin

**Note:** This data input doesn't run on a MID Server. Only a single Glide Syslog connector or data input can exist in the system.

-   Ensure that the Health Log Analytics application is installed and provisioned on your instance. For more information, see [Health Log Analytics \(HLA\) installation](install-health-log-analytics.md).
-   Ensure that a service instance is available.
-   Ensure that the Health Log Analytics AI Engine is up and running.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Data Inputs**.

2.  On the Data Inputs page, select **New**.

3.  Choose the Glide Syslog Retriever data input.

4.  On the form, fill in the fields.

    For a description of the fields, see [Glide Syslog data input configuration fields](../reference/hla-data-input-glide-syslog-ref.md).

5.  Select **Save**.


## Result

The data input configuration process is complete. Health Log Analytics adds the data input record to the **Data Inputs** table and attaches the configuration file to the data input record.

The data input starts streaming Glide log data from the System Log table to the Health Log Analytics AI engine, based on the configured filters. Admin users can set filters to query the System Log table. Users with the evt\_mgmt\_user role can use Event Management to monitor the logs and view the alerts that Health Log Analytics generates from them.

**Note:** If the HLA engine is down and data has stopped streaming, a notification appears at the top of the data input configuration page. When this happens, contact ServiceNow support.

## What to do next

[Make sure that the data input is streaming data.](hla-data-input-streaming.md)

-   **[Glide Syslog data input configuration fields](../reference/hla-data-input-glide-syslog-ref.md)**  
Description of the fields on the Glide Syslog data input configuration form.

**Parent Topic:**[Configuring data inputs for Health Log Analytics manually](../concept/hla-data-inputs-configuring.md)

