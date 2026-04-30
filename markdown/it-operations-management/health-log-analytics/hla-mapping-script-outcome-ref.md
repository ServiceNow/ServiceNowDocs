---
title: JavaScript function test outcome fields
description: Description of the JavaScript function test outcome fields.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Health Log Analytics reference, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# JavaScript function test outcome fields

Description of the JavaScript function test outcome fields.

The following fields are read-only:

<table id="table_mjz_l5v_kxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Duration \(ms\)

</td><td>

The processing time of all samples, in milliseconds.

</td></tr><tr><td>

Source types

</td><td>

The number of source types predicted or created for this data input.

</td></tr><tr><td>

Sources

</td><td>

The number of sources predicted or created for this data input.

</td></tr><tr><td>

Errors

</td><td>

The number of JavaScript errors that occurred in all the samples.

</td></tr><tr><td>

Unmapped

</td><td>

The number of log lines that could not be mapped. These log lines are mapped to default tags.

</td></tr><tr><td>

Samples

</td><td>

The number of log samples on which the test is run.The default value is 1,000.

**Note:** You can increase the number of log samples up to a maximum of 5,000 samples in the system property data\_input\_mapping.max\_examples. For more information, see [Configure global Health Log Analytics system properties](../task/hla-system-properties-configure.md).

</td></tr></tbody>
</table>In the related lists, view the predicted or created source types and sources.

<table id="table_ihw_sw5_fvb"><thead><tr><th>

List/Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Outcome Key Value Mapping**

</td><td>

The results of running the JavaScript function on the log samples.

</td></tr><tr><td>

**Source Types \(from samples\)**

</td><td>

The predicted or created source types.**Note:** You can open source types that have already been created by selecting the appropriate link.

</td></tr><tr><td>

**Sources \(from samples\)**

</td><td>

The predicted or created sources.**Note:** You can open sources that have already been created by selecting the appropriate link.

</td></tr><tr><td>

**Test Outcome**

</td><td>

The log samples used for testing your JavaScript function, ordered by sources and source types.The **Test Outcome** list displays the number of log samples for each source-source type combination, and is updated when the log samples are refreshed and you start testing your script.

The list links to samples in the **Mapping Samples** table, which shows the outcome of the JavaScript function for each sample.

This feature is supported in the Health Log Analytics application, Version 26.0.17 - February 2023 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr><tr><td>

**Source Type Structures**

</td><td>

The source type structures for this data input.Reviewing the source type structures can help you gain a better understanding of the data flow.

The **Last event time** column on this tab shows the last date and time the AI engine processed a log for the source type structure. The system refreshes this information every 5 minutes. Knowing when the last log was processed for this source type structure makes it easier to verify that log data is streaming.

</td></tr></tbody>
</table>**Parent Topic:**[Health Log Analytics reference](../concept/hla-reference.md)

