---
title: Set probe parameters
description: Use probe parameters to control the behavior of a particular probe every time it is triggered.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Discovery probe management, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Set probe parameters

Use probe parameters to control the behavior of a particular probe every time it is triggered.

## Before you begin

Role required: admin

## About this task

The following parameters are available for all probe types:

<table id="table_axr_x3v_tp"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`source`

</td><td>

\[Required\] The initial host to connect to.-   Type: string \(URL\)
-   Default value: None

</td></tr></tbody>
</table>## Procedure

1.  Create or select the [probe](../reference/r_Probes.md) you want to set parameters for.

2.  From the Probe Parameters related list, click **New**.

3.  Fill in the fields, as appropriate \(see table\).

    The Probe parameter form has the following fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter the parameter name. Each [probe type](../reference/r_Probes.md) has its own list of available parameters.|
    |Value|Enter the parameter value or script as required by the parameter.|
    |Value script|\[Optional\] Enter the script you want the parameter to run if you have not already specified a script in the Value field.|
    |Probe|Displays the probe this parameter relates to.|


**Parent Topic:**[Discovery probe management](../reference/r_Probes.md)

