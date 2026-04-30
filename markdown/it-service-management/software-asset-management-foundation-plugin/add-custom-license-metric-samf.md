---
title: Add a Software Asset Management Foundation plugin custom license metric
description: You can add a custom license metric to modify the default reconciliation process.
locale: en-US
release: zurich
product: Software Asset Management Foundation plugin
classification: software-asset-management-foundation-plugin
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management Foundation plugin Administration, Software Asset Management Foundation plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Add a Software Asset Management Foundation plugin custom license metric

You can add a custom license metric to modify the default reconciliation process.

## Before you begin

Role required: sam\_admin to read the custom metric script.

## About this task

Custom license metrics can be created to define specific software calculations not included in the predefined license metrics list. Custom license metrics are useful so reconciliation can calculate rights per user or device for certain software products and bundles of lesser-known software publishers.

For example, you can create a custom metric to avoid over counting installs for products that are part of an unrecognized bundle.

Custom metrics can be disabled using the custom license metric [property](../reference/sam-properties-samf.md). This feature is enabled by default.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Custom License Metrics** and create a new record \(see table for field descriptions\).

<table id="table_fdn_2pd_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

License metric

</td><td>

Name of the custom license metric. This name is shown in the **License Metric** field of software entitlements, and in the license metric results for the software model.

</td></tr><tr><td>

Metric group

</td><td>

\[Read-only\] Custom license metric.

</td></tr><tr><td>

Allocation type

</td><td>

Allocation type of the metric license, per device or per user.-   Device
-   User


</td></tr><tr><td>

Description

</td><td>

Description of the custom license metric.

</td></tr><tr><td>

Reconciliation order - allocated

</td><td>

Reconciliation metric rank priority for allocated licenses. Lower rank value takes precedence.

</td></tr><tr><td>

Reconciliation order - unallocated

</td><td>

Reconciliation metric rank priority for unallocated licenses. Lower rank value takes precedence.

</td></tr><tr><td class="sub-head" colspan="2">

Calculation

</td></tr><tr><td>

Calculation Script

</td><td>

The calculation method for the license metric is script. Specify the reconciliation script.

</td></tr></tbody>
</table>
**Parent Topic:**[Software Asset Management Foundation plugin Administration](../concept/c_SAMAdministrationSAMF.md)

