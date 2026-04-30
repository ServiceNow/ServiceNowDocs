---
title: Create KPIs without using KPI template
description: You can add new KPIs for a supplier without using the existing KPI templates. Adding new KPIs directly generates the corresponding KPI templates.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Supplier Relationship and Performance Management, Configure, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create KPIs without using KPI template

You can add new KPIs for a supplier without using the existing KPI templates. Adding new KPIs directly generates the corresponding KPI templates.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\) and navigate to **Lists** &gt; **Performance management** &gt; **KPIs**.

3.  Select **New**.![Selected option to create a new KPI.](../image/create-kpi-without-template.png)

4.  On the Create New KPI form, fill in the fields.

<table id="table_u4m_243"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Basic details

</td></tr><tr><td>

Name

</td><td>

Name of the KPI.

</td></tr><tr><td>

Supplier

</td><td>

Name of the supplier.

</td></tr><tr><td>

Description

</td><td>

Brief description of the KPI template.

</td></tr><tr><td>

Type

</td><td>

Indicates the type of the KPI. The available options are:-   Quantitative
-   Qualitative
**Note:**

-   Manual KPIs can be created of both Qualitative and Quantitative types.
-   Automated KPIs can be created only of Quantitative type.


</td></tr><tr><td>

Active

</td><td>

This option is turned off by default. The KPI is automatically set to active after you have added at least two thresholds for the KPI and one of those thresholds is marked as target.

</td></tr><tr><td class="sub-head" colspan="2">

KPI properties

</td></tr><tr><td>

Performance domain

</td><td>

Indicates the group that the KPI belongs to.

</td></tr><tr><td>

Weight

</td><td>

Determines the importance of the KPI in the overall performance score when multiple KPIs are collected.

</td></tr><tr><td>

Direction

</td><td>

Indicates whether the KPI should be minimized or maximized to show the ideal trend of the values. The available options are:-   Maximize
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

Data collection type

</td><td>

Select **Manual** for creating a manual KPI template.

 Select **Automated** for creating a automated KPI template.

</td></tr><tr><td>

Collection source \(for **Manual** data collection type\)

</td><td>

The user persona that provides the data. The available options are:-   User
-   Supplier Manager
-   Supplier Contact


</td></tr><tr><td>

Collected from \(for **Manual** data collection type\)

</td><td>

The person who provides the data.This field is displayed only if you select **User** in the **Collection source** field.

</td></tr><tr><td>

Collection table \(for **Automated** data collection type\)

</td><td>

Table from where KPI data is to be collected.**Note:** You must have access to the data tables for extracting data for automated KPIs.

</td></tr><tr><td>

Entity table column \(for **Automated** data collection type\)

</td><td>

Column of the collection table which refers to the supplier or contract name.

</td></tr><tr><td>

KPI data table column \(for **Automated** data collection type\)

</td><td>

Column of the collection table which contains the KPI data to be extracted.

</td></tr><tr><td>

Automated data aggregation method \(for **Automated** data collection type\)

</td><td>

The method used to calculate the aggregated KPI value when the given KPI consists of automated KPIs:-   Count
-   Sum
-   Average
-   Min
-   Max
-   Latest


</td></tr><tr><td>

Criteria \(for **Automated** data collection type\)

</td><td>

Build a filter criteria by adding conditions that contain a field, operator, and value\(s\).

</td></tr><tr><td>

Collection frequency

</td><td>

The frequency for collecting the KPI data. The available options are:-   Daily
-   Weekly
-   Monthly
-   Quarterly
-   Semi-annually
-   Annually


</td></tr><tr><td>

Contract data aggregation method

</td><td>

The method used to calculate the aggregated KPI value when the given KPI consists of contract-level sub-KPIs:-   Average
-   Sum
-   Minimum
-   Maximum


</td></tr><tr><td>

Instructions

</td><td>

Populated in KPI collection tasks to give more context to the user providing the KPI data.

</td></tr><tr><td>

Next run date

</td><td>

The next scheduled run date in yyyy-mm-dd format.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

A KPI is created for the selected supplier. Also, a corresponding KPI template is created.

This KPI is activated only when the following conditions are met:

-   At least two active thresholds are added
-   One of those thresholds is marked as target

**Note:** For Automated KPIs:

-   You must have access to the data tables for extracting data for automated KPIs.
-   If the automated KPI collection fails to extract data, manual KPI data collection tasks are created and assigned to the supplier manager.

**Parent Topic:**[Configure Supplier Relationship and Performance Management](../concept/configuring-supplier-performance-mgmt.md)

**Related topics**  


[Create KPIs by adding suppliers to a KPI template](add-supplier-kpi-template.md)

[Create KPI units](../concept/create-kpi-units.md)

