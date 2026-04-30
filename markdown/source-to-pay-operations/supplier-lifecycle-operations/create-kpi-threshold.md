---
title: Create KPI thresholds
description: Create KPI thresholds that consist of predefined values that serve as benchmarks or limits for evaluating performance against specific objectives.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create KPI thresholds

Create KPI thresholds that consist of predefined values that serve as benchmarks or limits for evaluating performance against specific objectives.

Create KPI thresholds. 

## Before you begin

Role required: sn\_slm.manager or sn\_slm.admin

## About this task

Ensure that you add at least two active thresholds to activate a KPI template. You can add a maximum of five thresholds to a KPI template.

**Note:** Thresholds help determine what score the supplier receives in the **KPI management** tab and in the scorecard. For more information, see [Manage supplier KPIs from the supplier record page of the Source-to-Pay Workspace](kpi-mgmt-tab-supplier.md).

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\), and navigate to **Lists** &gt; **Performance management** &gt; **KPI Templates**.

3.  In the Name column, select the link to the KPI template.

4.  Select the **Thresholds** tab and select **New**.![Selected option to create a new KPI threshold.](../image/create-kpi-thresholds.png)

5.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the KPI threshold.

</td></tr><tr><td>

Label

</td><td>

Label for the KPI threshold. **Note:** The Label field is displayed only for the Qualitative KPI templates.

</td></tr><tr><td>

Description

</td><td>

Brief description of the KPI threshold.

</td></tr><tr><td>

Active

</td><td>

Option indicating that the threshold is active for use.

</td></tr><tr><td>

Low Value

</td><td>

Represents the low value in the KPI threshold value range.-   This field is displayed only for Quantitative KPI templates.
-   This value is **included** in the threshold range.
-   If left empty, the **Low Value** defaults to negative infinity.


</td></tr><tr><td>

High Value

</td><td>

Represents the high value in the KPI threshold value range.-   This field is displayed only for Quantitative KPI templates.
-   This value is **excluded** from the threshold range.
-   If left empty, the **High Value** defaults to positive infinity.


</td></tr><tr><td>

Normalized value

</td><td>

Indicates a value that has been calculated from its original figure to fit a specific scale for easy comparison with other values. For example, a scale of 1–5.

</td></tr><tr><td>

Color

</td><td>

The color you select for each threshold is inherited by the Status column \(showing highlighted value\) in the KPI management tab on the Supplier page. For more information, see [Manage supplier KPIs from the supplier record page of the Source-to-Pay Workspace](kpi-mgmt-tab-supplier.md).

</td></tr></tbody>
</table>6.  Select **Save**.

    **Note:** A KPI is activated only when at least two active thresholds are added to it and one of those thresholds is marked as **Target threshold**.


**Parent Topic:**[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

**Related topics**  


[Create manual KPI templates](create-kpi-template-slo.md)

