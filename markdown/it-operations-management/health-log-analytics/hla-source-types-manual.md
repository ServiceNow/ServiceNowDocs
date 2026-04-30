---
title: Add source types manually
description: Create a source type manually before you configure a data input if you want to stream log data to a specific source type rather than to the source type automatically extracted by Health Log Analytics during the mapping process.
locale: en-US
release: xanadu
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up data inputs for Health Log Analytics manually, Health Log Analytics data input setup, Configuring Health Log Analytics, Health Log Analytics, ITOM Health, IT Operations Management]
---

# Add source types manually

Create a source type manually before you configure a data input if you want to stream log data to a specific source type rather than to the source type automatically extracted by Health Log Analytics during the mapping process.

## Before you begin

This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Source Types**.

2.  On the Source Types page, select **New**.

3.  On the form, fill in the fields.

<table id="table_cwx_llc_lpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the source type.The name must be between 3-50 characters long. Acceptable characters are letters, numeric values, dashes, and underscores.

</td></tr><tr><td>

Examples

</td><td>

One or more raw input samples for this source type. Enter each sample on a new line.**Note:** This field must contain data.

</td></tr></tbody>
</table>    The fields in the following table are read-only.

<table id="table_xnp_zpc_lpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created manually

</td><td>

Option for indicating that this source type was created manually. Default: true.

</td></tr><tr><td>

Auto-extraction enabled

</td><td>

Auto-extraction for this source type is disabled by default.

</td></tr><tr><td>

Learning mode

</td><td>

Option for indicating that Learning mode for the source type is ongoing. The AI engine must learn the format of log messages in each new log stream. In Learning mode, it learns the format of messages for this source type and extracts properties based on that knowledge.

</td></tr></tbody>
</table>4.  Right-click the form header and select **Save**.

5.  Select **Load examples** to load the raw input samples for this source type that you provided in the **Examples** field.

    When loading the log samples is completed successfully, the **Examples** field and the **Load examples** buttons no longer appear on the form.

6.  Check how the AI engine has parsed the raw input samples by selecting the **Go to Source Type Structure** related link and modify the extracted properties if necessary.

7.  Click **Submit**.


## What to do next

Configure a data input and then map it to the new source type. For more information, see [Set up data inputs for Health Log Analytics manually](hla-data-input-setup-manual.md) and [Map raw log data](hla-data-input-mapping.md).

**Parent Topic:**[Set up data inputs for Health Log Analytics manually](hla-data-input-setup-manual.md)

**Related topics**  


[Refine the source type structure](hla-source-type-structure-refine.md)

