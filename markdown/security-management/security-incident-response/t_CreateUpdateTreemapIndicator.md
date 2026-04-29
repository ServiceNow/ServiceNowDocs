---
title: Create or update a treemap indicator
description: You can modify the predefined indicators for a treemap category or create new indicators. For each indicator, you can configure its data source and specify how lists of security incidents are opened from treemaps that are viewed with the indicator.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security incident treemaps, Security Incident Response Overview dashboard, Visual representation of Security Incident Response reporting, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create or update a treemap indicator

You can modify the predefined indicators for a treemap category or create new indicators. For each indicator, you can configure its data source and specify how lists of security incidents are opened from treemaps that are viewed with the indicator.

## Before you begin

Role required: sn\_si.admin

The treemaps use performance analytics as the data source. The Performance Analytics module requires a separate plugin.

## Procedure

1.  Open the treemap definition that you want to configure indicators for.

    |Treemap definition|Action|
    |------------------|------|
    |**Service impact treemap**|Navigate to **Security Incident** &gt; **Administration** &gt; **Service Impact Definition**.|
    |**Real-time treemap**|Navigate to **Security Incident** &gt; **Administration** &gt; **Real-time Definition**.|

2.  In the **Treemap Categories** related list, select the category that you want to configure indicators for.

3.  In the **Treemap Indicators** related list, select an indicator to modify or click **New** to create a new indicator.

4.  Fill in the fields.

<table id="table_s52_yvn_r4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name that is displayed for the indicator in the **Indicators** list on the service impact dashboard.

</td></tr><tr><td>

Short description

</td><td>

A description that is displayed for the indicator in the **Indicators** list above the treemap.

</td></tr><tr><td>

Result limit

</td><td>

The maximum number of results allowed. The upper limit is 100.

</td></tr><tr><td>

Result Precision

</td><td>

The number of digits to display after the decimal point.This field is displayed for the real-time treemap definition only.

</td></tr><tr><td>

Active

</td><td>

Check box to activate this indicator.

</td></tr><tr><td>

Category

</td><td>

The category name entered on the previous screen.

</td></tr><tr><td>

Direction

</td><td>

Indicates whether the tile on the treemap is minimized or maximized.This field is displayed for the real-time treemap definition only.

</td></tr><tr><td>

Unit

</td><td>

The unit of measure to be used for the metric.This field is displayed for the real-time definition only.

</td></tr><tr><td>

Automatic Refresh Interval

</td><td>

How frequently to refresh the treemap.

</td></tr><tr><td>

Order

</td><td>

The order the indicator appears in the **Indicators** list above the treemap.

</td></tr></tbody>
</table>5.  Click the **Data Source Configuration** tab and configure one of the following data source options for the indicator.

<table id="choicetable_x2q_twj_bt"><thead><tr><th align="left" id="d189231e291">

Option

</th><th align="left" id="d189231e294">

Action

</th></tr></thead><tbody><tr><td id="d189231e300">

**Performance analytics**

</td><td>

Select **Performance Analytics** from the **Data source** field, then make the following entries:-   **Indicator:** The indicator used to group the PA data.
-   **Default breakdown:** The default breakdown used to break the selected PA indicator into multiple parts.


</td></tr><tr><td id="d189231e328">

**Custom script**

</td><td>

Select **Custom Script** from the **Data Source** field. Then use the HTML editor to customize the script as needed. The result of running the script must be an array in order for the information to display in the treemap.

</td></tr><tr><td id="d189231e343">

**Query conditions**

</td><td>

Select **Query Condition** from the **Data Source** field, and then make the following entries:-   **Query table:** The base table to be queried.
-   **Aggregate type:** The type of aggregate \(SUM, COUNT, AVG, MIN, MAX\) to be used.
-   **Aggregate field:** The field to be used by the query.
-   **Group by:** The field to sort the queried data.
 **Note:** To enhance the query, click **Add Filter Condition** and **Add "OR" Clause**.

</td></tr></tbody>
</table>6.  Click the **Click Through** tab, and specify how lists of security incidents are opened from the treemap.

    1.  In the **Click through URL navigation type** field, select whether you want the list of security incidents to open in a new window, in the same window, or in a dialog box.

    2.  In the **Click through URL script** field, modify the sample script if needed.

7.  Click **Submit** or **Update**.


**Parent Topic:**[Security incident treemaps](../concept/c_ConfigureTreemaps.md)

