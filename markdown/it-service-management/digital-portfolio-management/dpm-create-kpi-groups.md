---
title: Create KPI groups and mappings in Digital Portfolio Management
description: Create key performance indicator \(KPI\) groups and mappings in Digital Portfolio Management \(DPM\) to monitor the overall health and progress of all your services and offerings.
locale: en-US
release: zurich
product: Digital Portfolio Management
classification: digital-portfolio-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure KPI groups, Configure, Digital Portfolio Management, IT Service Management]
---

# Create KPI groups and mappings in Digital Portfolio Management

Create key performance indicator \(KPI\) groups and mappings in Digital Portfolio Management \(DPM\) to monitor the overall health and progress of all your services and offerings.

## Before you begin

-   Plugins required: sn\_dpm, com.sn\_team\_perf, and com.snc.service\_portfolio
-   Role required: sn\_dpm.dpm\_admin

## About this task

Create KPI groups and associate each group's type with its corresponding record. Here are the record types:

-   Service portfolios
-   Taxonomy nodes
-   Services
-   Offerings
-   Service instances
-   Business applications
-   Enterprise portfolios
-   Enterprise taxonomy nodes

In addition to creating your own KPI groups, you can use and configure the KPI groups that come with the base DPM application. For details, see [KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi.md).

This procedure includes the following tasks:

1.  Create a KPI group.
2.  Add indicators to a KPI group.
3.  Create a KPI group mapping.

## Procedure

1.  Create a KPI group.

    1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **KPI Groups**.
    2.  Select **New**.
    3.  On the form, fill in the fields.

<table id="table_ir3_cs5_2sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the KPI group.

</td></tr><tr><td>

Description

</td><td>

The description of the KPI group.

</td></tr><tr><td>

Type

</td><td>

The type that you want to create:-   Service portfolios
-   Taxonomy nodes
-   Services
-   Offerings
-   Service instances
**Note:** The type must correlate to the record. For example, you can only associate a service portfolio type to a portfolio record. You can only associate an offering type to an offering record.

</td></tr><tr><td>

Order

</td><td>

Determines the page layout of the KPI groups in the Digital Portfolio Management workspace.

</td></tr><tr><td>

Show on preview

</td><td>

If selected, the KPI group displays in the Details section of the Enterprise Portfolio homepage in the DPM workspace. All selected KPI groups will display on the page, not just one.

</td></tr></tbody>
</table>    4.  Select **Submit**

        **Tip:** You can also create a KPI group by copying an existing KPI group. For more information, see [Copy a KPI group to create a new KPI group in Digital Portfolio Management](dpm-copy-kpi-group.md).

2.  Add indicators to a KPI group.

    1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **KPI Groups**.
    2.  Select the KPI group that you want to add indicators to.
    3.  On the **KPIs** tab, select **New**.
    4.  On the form, fill in the fields.

<table id="table_xmm_2q5_2sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KPI Group

</td><td>

KPI group to add indicators.

</td></tr><tr><td>

KPI

</td><td>

KPI indicator that you want to measure.

</td></tr><tr><td>

Label

</td><td>

Name of the KPI indicator. You can edit the label.

</td></tr><tr><td>

Parent KPI

</td><td>

Parent KPI, if this KPI is a supporting KPI.

</td></tr><tr><td>

Display Aggregate

</td><td>

KPI display aggregate: Average or Sum.

**Note:** This field applies when the latest score property \[sn\_dpm.kpi\_groups.show\_latest\_score\] is false. For information, see [Configure the Digital Portfolio Management experience](dpm-configure-experience.md).

</td></tr><tr><td>

Order

</td><td>

Page layout of the KPI groups in the Digital Portfolio Management workspace.

</td></tr><tr><td>

Description

</td><td>

The description of the indicator. For more information on KPI results, see [KB1123710](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637474).

</td></tr><tr><td>

Chart type

</td><td>

The chart type for the KPI group. The options are:

-   **Single score**
-   **Time series: Line**
-   **Time series: Column**
-   **Time series: Area**
-   **Time series: Spline**
-   **Time series: Step line**
-   **Group By**
**Note:** The **Group By** option enables you to select the results breakdown. For example, incidents by priority.

</td></tr></tbody>
</table>    5.  Select **Submit**.
3.  Create a KPI group mapping.

    1.  Navigate to **All** &gt; **Digital Portfolio Management** &gt; **KPI Group Mappings**.

        **Note:** You can also map a KPI group by navigating to **All** &gt; **Digital Portfolio Management** &gt; **KPI Groups**. Select a KPI group to view, and then select the **KPI Group Mappings** tab.

    2.  Select **New**.
    3.  On the form, fill in the fields.

<table id="table_n3z_2v5_2sb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KPI Group

</td><td>

KPI group name to add the mapping.

</td></tr><tr><td>

Mapping

</td><td>

Mapping type associated with the KPI group. Depending on which KPI Group you select, one of the following displays as the Mapping field.

 -   Service portfolio
-   Taxonomy node
-   Service
-   Offering
-   Service instance
-   Business application
-   Enterprise portfolio
-   Enterprise taxonomy node


</td></tr></tbody>
</table>    4.  Select **Submit**.

**Parent Topic:**[Configure KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi-groups.md)

**Related topics**  


[Configure KPI groups in Digital Portfolio Management](../concept/dpm-configure-kpi-groups.md)

[Configure KPIs in Digital Portfolio Management with service availability example](dpm-configure-kpi-availability.md)

