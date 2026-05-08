---
title: Add a custom license metric
description: You can add a custom license metric to modify the default reconciliation process.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 2
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Add a custom license metric

You can add a custom license metric to modify the default reconciliation process.

## Before you begin

Role required:

-   to create or modify a custom metric script: sam\_developer
-   to read custom metric script: sam\_admin

Role required to create or modify a custom metric script: sam\_developer

## About this task

Custom license metrics can be created to define specific software calculations not included in the predefined license metrics list. Custom license metrics are useful so reconciliation can calculate rights per user or device for certain software products and bundles of lesser-known software publishers.

For example, you can create a custom metric to avoid over counting installs for products that are part of an unrecognized bundle.

You can use the Resource Value \[samp\_sw\_resource\_value\] table to enhance the custom license metric capability by doing a 1:1 calculation between the Units consumed column in the Resource Value \[samp\_sw\_resource\_value\] table and the Licenses required column in the License Metric Results \[samp\_license\_metric\_result\] table. You can create your own calculations in your custom license metric scripts and write your own logic to further customize your custom license metric. For information on adding resource values to the Resource Value \[samp\_sw\_resource\_value\] table, see [Specify resource values for your custom license metrics](specify-resource-values-custom-license-metrics.md).

Custom metrics can be disabled using the custom license metric [property](../reference/sam-properties.md). This feature is enabled by default.

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

Table Source

</td><td>

Specify if this custom license metric belongs to the Software Installations \[cmdb\_sam\_sw\_install\] table or the Resource Value \[samp\_sw\_resource\_value\] table. **Note:** If the table specified is the Resource Value table, the following fields: **Reconciliation order – allocated**, **Reconciliation order – unallocated**, and **Allocation type** are not displayed. Additionally, the Calculation Script shows a sample script related to resource value.

</td></tr><tr><td>

Metric group

</td><td>

Custom license metric.

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

Reconciliation order — allocated

</td><td>

Reconciliation metric rank priority for allocated licenses. Lower rank value takes precedence.

</td></tr><tr><td>

Reconciliation order — unallocated

</td><td>

Reconciliation metric rank priority for unallocated licenses. Lower rank value takes precedence.

</td></tr><tr><td class="sub-head" colspan="2">

Calculation

</td></tr><tr><td>

Calculation Script

</td><td>

The calculation method for the license metric is script. Specify the reconciliation script.

</td></tr></tbody>
</table>2.  Select **Submit**.


-   **[Custom license metric example script](../reference/custom-license-example-script.md)**  
The following is an example of a custom license metric script.
-   **[Specify resource values for your custom license metrics](specify-resource-values-custom-license-metrics.md)**  
If you create a custom license metric based on resource values, specify the resource value for each software product that you want to calculate licensing requirements for.

**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

