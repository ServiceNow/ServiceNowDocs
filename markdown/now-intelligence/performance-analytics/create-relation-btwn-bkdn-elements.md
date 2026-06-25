---
title: Create relations between elements of a breakdown
description: Use a breakdown relation to set up navigation between a hierarchy of elements within the same breakdown. A field in the breakdown records must identify the hierarchical relationship of one record to another.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/create-relation-btwn-bkdn-elements.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Navigating breakdown elements with breakdown relations, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create relations between elements of a breakdown

Use a breakdown relation to set up navigation between a hierarchy of elements within the same breakdown. A field in the breakdown records must identify the hierarchical relationship of one record to another.

## Before you begin

Review the use cases for breakdown relations in [Navigating breakdown elements with breakdown relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/breakdown-relations.md).

**Important:** To show breakdown relations on Platform Analytics, you have to create a dashboard with an indicator scorecard and a filter. KPI Details does not support breakdown relations.

Role required: pa\_data\_collector, pa\_power\_user, admin

**Note:** While a business analyst, typically with the pa\_power\_user role, is most likely to know what breakdown relations to create, creating them requires the knowledge and access to tables of a technical expert with pa\_data\_collector. A pa\_admin is likely to understand both. Consider having either a pa\_admin create the relation or have a collaboration between a pa\_power\_user and a pa\_data\_collector.

## About this task

You can create breakdown relations to navigate the following hierarchical relationships between elements of a breakdown:

-   Child relations, to navigate from a parent element to its children
-   Parent relations, to navigate from a child element to its parents
-   Sibling, or peer relations, to navigate between elements that share the same parent element

In a breakdown with a hierarchical relationship between elements, one field in the element record identifies the position of the element in the hierarchy. Typically this field is Parent, and identifies the parent element. Elements that are the parent of one element can themselves have a parent element.

**Note:** Breakdown relations are one-way relationships. Define multiple breakdown relations to create a bi-directional relationship.

## Procedure

1.  Navigate to **All** &gt; **Breakdowns** &gt; **Breakdown Relations** and click **New**.

2.  In the **Breakdown** and **Related breakdown** fields, select the breakdown whose elements you want to navigate between.

    These fields have the same value when you're creating a hierarchical relation between elements of the same breakdown.

3.  In the **Table** field, select the same table as the breakdown source facts table.

4.  Fill in the rest of the form, depending on whether you're creating a child, a parent, or a sibling/peer relation.

<table id="table_bkdwn-relations"><thead><tr><th>

Field

</th><th>

Child relation

</th><th>

Parent relation

</th><th>

Sibling/peer relation

</th></tr></thead><tbody><tr><td>

Breakdown field

</td><td>

Select the field that identifies the parent element.For the Location breakdown, select **Parent**.

</td><td>

Select the unique identifier field for elements of this breakdown.For the Location breakdown, as for most breakdowns, select **Sys ID**

</td><td>

Select the unique identifier field for elements of this breakdown.For the Location breakdown, as for most breakdowns, select **Sys ID**

</td></tr><tr><td>

Related breakdown field

</td><td>

Select the unique identifier field for elements of this breakdown.For the Location breakdown, as for most breakdowns, select **Sys ID**

</td><td>

Select the field that identifies the parent element.For the Location breakdown, select **Parent**.

</td><td>

Select the unique identifier field for elements of this breakdown.For the Location breakdown, as for most breakdowns, select **Sys ID**

</td></tr><tr><td>

Common field

</td><td>

Leave empty.

</td><td>

Leave empty.

</td><td>

Select the field that identifies the parent element.For the Location breakdown, select **Parent**.

</td></tr></tbody>
</table>5.  Under **Conditions**, define any further conditions that a record must fulfill to appear as a related breakdown for this relationship.


## Parent group of Assignment Groups

These instructions create a parent group relation for the Assignment Group breakdown and displays the relation in a dashboard. To display the breakdown relation in a dashboard, you need two dashboard elements:

-   A filter
-   An indicator scorecard

The filter is the starting point. It acts as a source, and the breakdown configured for the indicator scorecard acts as a target. The breakdown relation record defines how these two elements are connected.

1.  Navigate to **All** &gt; **Breakdowns** &gt; **Breakdown Relations** and tap **New**.
2.  Name the relation Parent Group.
3.  For both Breakdown and Related Breakdown, select Assignment Group.
4.  For the Table, select Group \[sys\_user\_group\].
5.  Select SysID for the breakdown field.
6.  Select Parent for the related breakdown field.
7.  Do not select a common field.
8.  Define \[Active\]\[Is\]\[True\] as the condition.
9.  Tap **Update**.

You now have a hierarchical breakdown relation. To display it, you need a dashboard with an indicator scorecard.

1.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**
2.  Tap **Create dashboard**.
3.  Create a Next Experience dashboard in the In-line editor and name it Hierarchical relation.
4.  Tap **Add new element**
5.  Select **Data visualization** and create a visualization.
6.  Configure the visualization as follows:

    |Field|Value|
    |-----|-----|
    |Visualization type|Indicator scorecard|
    |Scorecard type|List|
    |Data &gt; Indicator &gt; Source definition|Manually selected|

7.  Tap **Indicator &gt; Add**.
8.  Select the Number of open incidents indicator.
9.  Tap **Breakdown &gt; Add**
10. Select Assignment Group.
11. Turn on **Follow breakdown relation**.
12. Select the Parent Group relation.
13. Save.

Lastly, you need a filter on the same breakdown.

1.  Tap **Add new element**.
2.  Select Filter &gt; New Filter.
3.  Label the filter Assignment Group.
4.  Tap **Add source** and select the Group \[sys\_user\_group\] table.
5.  Tap **Apply**
6.  Under Data to filter, tap **Add**.
7.  Select indicators with the breakdown Assignment Group.
8.  Tap **Apply**.

Save the dashboard and start selecting values in the filter. When you select a child value, like Database Atlanta, you roll the result up into the parent value, like Database.

## What to do next

View examples of breakdown relations that are shipped by default in every instance.

**Parent Topic:**[Navigating breakdown elements with breakdown relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/breakdown-relations.md)

**Related topics**  


[Create an Indicator Scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-indicator-scorecard.md)

[Create or add a filter on an inline dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/select-workspace-filter-type.md)

