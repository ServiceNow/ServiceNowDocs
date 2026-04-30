---
title: Sensitivity bounds properties for Insights Explorer metrics
description: The following properties can be configured to customize system behavior when detecting sensitive bounds for Insights Explorer metrics. To invoke changes to the default values, navigate to System Properties All Properties and add the indicated properties \(they are not visible by default\).
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Metric Intelligence reference, Metric Intelligence, IT Operations Management]
---

# Sensitivity bounds properties for Insights Explorer metrics

The following properties can be configured to customize system behavior when detecting sensitive bounds for Insights Explorer metrics. To invoke changes to the default values, navigate to **System Properties** &gt; **All Properties** and add the indicated properties \(they are not visible by default\).

<table id="table_l1w_r1d_lsb"><thead><tr><th>

Property Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sa\_metric.sensitive\_bounds\_calculation\_enabled

</td><td>

Enable/disable sensitive bounds calculation. Default: True

</td></tr><tr><td>

sa\_metric.sensitive\_bounds\_percentile

</td><td>

Percentile value of sensitivity bounds calculation. If the configured percentage of metric values falls within the number of standard deviations \(STDs\) indicated in the **sa\_metric.sensitive\_bounds\_sensitivity\_factor** property, sensitive bounds are detected and sensitivity calculation changes to the value specified in the **sa\_metric.sensitive\_bounds\_control\_factor** property. Default: 95%

</td></tr><tr><td>

sa\_metric.sensitive\_bounds\_control\_factor

</td><td>

The number of standard deviations \(STDs\) from the mean metric value by which metric bounds are measured after the system detects sensitive bounds.Default: 5.0

</td></tr><tr><td>

sa\_metric.sensitive\_bounds\_sensitivity\_factor

</td><td>

The number of standard deviations \(STDs\) from the mean metric value by which the system tests for sensitive bounds.Default: 2.0

</td></tr></tbody>
</table>**Parent Topic:**[Metric Intelligence reference](../../metric-intelligence/reference/metric-intelligence-reference.md)

**Related topics**  


[Metric bounds sensitivity](../concept/metric-bounds-sensitivity.md)

