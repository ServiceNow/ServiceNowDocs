---
title: Create automated KPI templates
description: Automated KPI templates can be used to create KPIs that eliminate the dependency on manual input from users. When creating a template for automated KPIs, you can configure the data source and the calculation method.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [KPI templates, Configure Supplier Relationship and Performance Management, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create automated KPI templates

Automated KPI templates can be used to create KPIs that eliminate the dependency on manual input from users. When creating a template for automated KPIs, you can configure the data source and the calculation method.

## Before you begin

Role required: sn\_kpi.admin or sn\_slm.manager or sn\_slm.admin

-   Automated KPI templates can be created for **Quantitative** KPI template type only.
-   You must have access to data tables for extracting information for automated KPI templates.
-   If the automated KPI collection fails to extract data, manual KPI data collection tasks are created and assigned to the supplier manager.

**Important:** Check your entitlements to determine whether you have access to Automated KPIs. This feature is available from the Yokohama December 2025 release onwards.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Do one of the following:

    -   Under Quick actions, select **Create KPI template**.![Selected Create KPI template option under Quick actions.](../image/create-kpi-template.png)
    -   Select the list icon \(![List icon.](../image/cases-list-icon.png)\), navigate to **Lists** &gt; **Performance management** &gt; **KPI Templates**, and then select **New**.
3.  On the form, fill in the fields.

    Select **Automated** for creating an automated KPI template.

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

Indicates the type of the KPI template. Select **Quantitative**.**Note:** Automated KPI templates can be created for **Quantitative** KPI template type only.

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

Data collection type

</td><td>

Select **Automated** for creating a automated KPI template.**Note:** Automated KPI template can be created only for **Quantitative** KPI type.

</td></tr><tr><td>

Collection table

</td><td>

Table from where KPI data is to be collected.**Note:** You must have access to the data tables for extracting data for automated KPIs.

</td></tr><tr><td>

Entity table column

</td><td>

Column of the collection table which refers to the supplier or contract name.

</td></tr><tr><td>

KPI data table column

</td><td>

Column of the collection table which contains the KPI data to be extracted.

</td></tr><tr><td>

Automated data aggregation method

</td><td>

The aggregation method used to calculate the data extracted from the tables mentioned according to the condition:-   Count
-   Sum
-   Average
-   Min
-   Max
-   Latest


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

Criteria

</td><td>

Build a filter criteria by adding conditions that contain a field, operator, and value\(s\).

</td></tr><tr><td>

Instructions

</td><td>

Populated in KPI collection tasks to give more context to the user providing the KPI data.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

An automated KPI template is created. This KPI is activated only when the following conditions are met:

-   At least two active thresholds are added
-   One of those thresholds is marked as target

**Parent Topic:**[KPI templates](../concept/kpi-templates.md)

**Related topics**  


[Create KPI thresholds](create-kpi-threshold.md)

[Create KPI units](../concept/create-kpi-units.md)

[Create KPI performance domains](../concept/create-kpi-domain.md)

