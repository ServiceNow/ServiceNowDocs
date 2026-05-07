---
title: Maintain import properties
description: Use Import Properties when you create your own credential records, scheduled imports, or data sources. Currently, the properties are configured for the records used when importing.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Mappedin, Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Maintain import properties

Use Import Properties when you create your own credential records, scheduled imports, or data sources. Currently, the properties are configured for the records used when importing.

## Before you begin

Role required: sn\_wsd\_mappedin.admin

## Procedure

1.  Navigate to **All** &gt; **Space Mapping** &gt; **Mappedin Administration** &gt; **Import properties**.

    **Note:** Only make edits if you are configuring your own credential records, scheduled imports, or data sources.

2.  Make edits to properties.

3.  Click **Save**.

    Other properties are found under the System Property \[sys\_properties\] table.

4.  Enter `sys_properties.list` in the navigation filter and open the following properties

<table id="choicetable_sct_wbg_h4b"><thead><tr><th align="left" id="d262870e99">

System property

</th><th align="left" id="d262870e102">

Description

</th></tr></thead><tbody><tr><td id="d262870e108">

**sn\_wsd\_core.external\_id\_generator.field​**

</td><td>

Defines the external ID.

</td></tr><tr><td id="d262870e117">

**sn\_wsd\_core.external\_id\_generator.max\_buildings**

</td><td>

The maximum number of buildings to generate IDs for with a single selection.50 is the default.

</td></tr><tr><td id="d262870e129">

**sn\_wsd\_core.external\_id\_generator.max\_spaces**

</td><td>

The maximum number of spaces to generate IDs for at a given time.The default is 5000.

</td></tr><tr><td id="d262870e141">

**sn\_wsd\_core.external\_id\_generator.stagger​**

</td><td>

The amount of time \(in seconds\) to stagger processing external ID generations.The default is 300 seconds.

</td></tr></tbody>
</table>
**Parent Topic:**[Configure Mappedin](../concept/mappedin-integration-topics.md)

