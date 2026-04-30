---
title: Create a KPI template
description: Create a KPI template to define KPIs against which you measure the supplier performance.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-14"
reading_time_minutes: 2
breadcrumb: [Configure Supplier Relationship and Performance Management, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create a KPI template

Create a KPI template to define KPIs against which you measure the supplier performance.

## Before you begin

Role required: sn\_kpi.admin or sn\_slm.manager or sn\_slm.admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Do one of the following:

    -   Under Quick actions, select **Create KPI template**.
    -   Select the list icon \(![List icon.](../image/cases-list-icon.png)\), navigate to **Lists** &gt; **Performance management** &gt; **KPI Templates**, and then select **New**.
3.  On the form, fill in the fields.

<table id="table_u4m_243_btb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic details

</td></tr><tr><td>

Name

</td><td>

Name of the KPI template.

</td></tr><tr><td>

Description

</td><td>

Brief description of the KPI template.

</td></tr><tr><td>

Template owner

</td><td>

The person who owns the KPI template.

</td></tr><tr><td>

Type

</td><td>

Indicates the type of the KPI template. The available options are:-   Quantitative
-   Qualitative


</td></tr><tr><td>

Active

</td><td>

This option is turned off by default. The KPI template is automatically set to active after you have added at least two thresholds for the KPI template.

</td></tr><tr><td class="sub-head" colspan="2">

KPI properties

</td></tr><tr><td>

Performance domain

</td><td>

Indicates the group that the KPI belongs to.

</td></tr><tr><td>

Recommended weight

</td><td>

Determines the importance of the KPI in the overall performance score when multiple KPIs are collected.

</td></tr><tr><td>

Direction

</td><td>

Indicates whether the KPI should be minimized or maximised to show the ideal trend of the values. The available options are:-   Maximize
-   Minimize
-   Milestone


</td></tr><tr><td>

Nature

</td><td>

Indicates whether the KPI is leading \(predicts future\), lagging \(measures past performance\), or current \(monitors ongoing activities\). The available options are:-   Leading
-   Lagging
-   Current


</td></tr><tr><td>

Precision

</td><td>

Specifies the number of decimal points to be used for data collection to ensure accuracy and consistency.This field is displayed only if you select **Quantitative** in the **Type** field.

</td></tr><tr><td>

Unit

</td><td>

Measurement used to quantify the performance indicator.This field is displayed only if you select **Quantitative** in the **Type** field.

</td></tr><tr><td class="sub-head" colspan="2">

Data collection

</td></tr><tr><td>

Collection source type

</td><td>

The user persona that provides the data. The available options are:-   User
-   Supplier Manager
-   Supplier Contact


</td></tr><tr><td>

Collected from user

</td><td>

The person who provides the data.This field is displayed only if you select **User** in the **Collection source type** field.

</td></tr><tr><td>

Instructions

</td><td>

Populated in KPI collection tasks to give more context to the user providing the KPI data.

</td></tr><tr><td>

Collection frequency

</td><td>

The frequency for collecting the KPI data. The available options are:-   Daily
-   Weekly
-   Monthly
-   Quarterly
-   Semi-annually
-   Annually


</td></tr></tbody>
</table>4.  Select **Save**.


-   **[Create KPI thresholds](create-kpi-threshold.md)**  
Create KPI thresholds that consist of predefined values that serve as benchmarks or limits for evaluating performance against specific objectives.

**Parent Topic:**[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

