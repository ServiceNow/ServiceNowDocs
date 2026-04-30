---
title: Review the properties extracted from a source type in Health Log Analytics
description: View the properties that were extracted from all the source types in a source type structure in a single table to identify any setup issues.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
keywords: [ServiceNow, Health Log Analytics, HLA, source type structure, source types, properties, setup problems, classification, Source Type Properties Stats]
breadcrumb: [Additional data input setup tasks, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Review the properties extracted from a source type in Health Log Analytics

View the properties that were extracted from all the source types in a source type structure in a single table to identify any setup issues.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The Source Type Properties Stats table provides a comprehensive overview of the properties that were extracted from the source types. By reviewing the statistical distribution of their values, you can assess the classification of these properties and adjust your settings if needed.

The procedure in this section explains how to access the Source Type Properties Stats table via the Source Type Structure. From a source type record, you can navigate to the Source Type Structure by selecting the **Go to Source Type Structure** related link.

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Source Type Structures**.

2.  Open a source type structure record.

3.  Open the **Properties Statistics** related links tab.

    ![The Source Type Properties Stats table.](../image/hla-properties-stats-table.png)

    The **Source Type Properties Stats** table shows the properties of all the source types that are part of this source type structure.

<table id="table_jkf_cxr_zbc"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source Type Property

</td><td>

The property extracted from the source type.

</td></tr><tr><td>

Classification

</td><td>

The classification of the property. The available types are: METER, GAUGE, ARC, and INVALID.

**Note:** A property classified as INVALID \(the default classification\) isn't tracked for anomaly detection or shown in the Meaningful Properties analysis.

</td></tr><tr><td>

Source Type

</td><td>

The source type from which the property was extracted.

</td></tr><tr><td>

Log Source

</td><td>

The list of Log Sources in which this property appeared.

</td></tr><tr><td>

Domain

</td><td>

The domain to which the log source belongs.

</td></tr><tr><td>

Total Unique Value Count

</td><td>

Only for properties classified as METER: The total number of distinct values contained in it.This field is inactive when the property is classified as ARC or GAUGE.

**Note:** The Total Unique Value Count is updated once a day. Records older than 24 hours are deleted automatically.

</td></tr><tr><td>

Sample Values

</td><td>

Only for properties classified as METER: Sample unique values tracked by the system. Default is 30 samples.This field is inactive when the property is classified as ARC or GAUGE.

</td></tr></tbody>
</table>4.  Review the properties and identify possible classification issues.

5.  View statistics for individual source type properties classified as ARC\_ONLY or GAUGE.

    1.  Open a source type property classified as ARC\_ONLY or GAUGE from the **Properties Statistics** related links tab.

    2.  On the **Source Type Property** form, select **Source Type Properties Stats**.

    The following information displays in a pop-up:

    -   For an ARC property: The percentage distribution of terms, based on the processed logs. For example, the percentage of Bad Request vs. Success.
    -   For a GAUGE property: The average, minimum, and standard deviation from the expected numerical value.
6.  Change classification settings on the **Key/Value Mapping** tab.

    For more information, see [Refine the source type structure](hla-source-type-structure-refine.md).


**Parent Topic:**[Additional data input setup tasks](../concept/hla-data-input-setup-extra.md)

