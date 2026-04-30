---
title: Date conditions
description: A maintenance user can configure Date range for the lifecycle phases.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Date conditions

A maintenance user can configure Date range for the lifecycle phases.

## Date conditions

<table id="table_nml_hll_l2b"><thead><tr><th>

Date conditions

</th><th>

Timeline in TPM screen

</th></tr></thead><tbody><tr><td>

Current date, Current date –10 years, Current date + 3 years.

</td><td>

Default dates.Timelines of product models that fulfill the default date conditions are shown.

</td></tr><tr><td>

All phases that start before the current date –10 years and continues to the present time.

</td><td>

Product models with such date conditions are shown and the timeline expands itself automatically from the default \(–10 years to +3 years\) to accommodate the past years.

</td></tr><tr><td>

Phases that start before the current date –10 years and continue beyond the current date and may still be in progress

</td><td>

Product models with such phases are shown until current date + 3 years.

</td></tr><tr><td>

Lifecycle phases that start and end before the current date –10 years

</td><td>

Product models with such phases are NOT shown.

</td></tr></tbody>
</table><table id="table_ent_csl_l2b"><thead><tr><th>

Lifecycle phase of record

</th><th>

Conditions for plotting the dates on TPM timeline

</th></tr></thead><tbody><tr><td>

One internal and one publisher

</td><td>

All dates are plotted on the timeline.

</td></tr><tr><td>

Multiple publishers

</td><td>

Only one publisher date is plotted.The publisher that is selected for plotting depends on the **sequence** property in the source column. All sources have a sequence number attached to them. The source with the least sequence number is selected. If the source with the least sequence number does not have any lifecycle records, then the source with the next least sequence number is selected.

</td></tr><tr><td>

One internal and multiple publishers

</td><td>

The internal date is plotted, but only one publisher date is plotted. The publisher record that is selected for plotting depends on the **sequence** property.

</td></tr><tr><td>

Overlapping dates of two phases

</td><td>

Only one line is shown.

</td></tr><tr><td>

Gaps in dates

</td><td>

A continuous line with no gap in the timeline.

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Product lifecycle data on the timeline](../concept/lifecycle-data-timeline.md)

