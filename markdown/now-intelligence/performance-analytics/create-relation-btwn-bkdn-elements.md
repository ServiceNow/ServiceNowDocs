---
title: Create relations between elements of one breakdown
description: Use a breakdown relation to set up navigation on an Analytics Hub between a hierarchy of elements within the same breakdown. A field in the breakdown records must identify the hierarchical relationship of one record to another.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Navigating breakdown elements with breakdown relations, Indicator breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create relations between elements of one breakdown

Use a breakdown relation to set up navigation on an Analytics Hub between a hierarchy of elements within the same breakdown. A field in the breakdown records must identify the hierarchical relationship of one record to another.

## Before you begin

Review the use cases for breakdown relations in [Navigating breakdown elements with breakdown relations](../concept/breakdown-relations.md).

**Important:** Platform Analytics features, such as KPI Details and data visualizations, do not support breakdown relations.

Role required: pa\_data\_collector, pa\_power\_user, admin

**Note:** While a business analyst, typically with the pa\_power\_user role, is most likely to know what breakdown relations to create, creating them requires the knowledge and access to tables of a technical expert with pa\_data\_collector. A pa\_admin is likely to understand both. Consider having either a pa\_admin create the relation or have a collaboration between a pa\_power\_user and a pa\_data\_collector.

## About this task

You can create breakdown relations to navigate the following hierarchical relationships between elements of a breakdown:

-   Child relations, to navigate from a parent element to its children
-   Parent relations, to navigate from a child element to its parents
-   Sibling, or peer relations, to navigate between elements that share the same parent element

In a breakdown with a hierarchical relationship between elements, one field in the element record identifies the position of the element in the hierarchy. Typically this field is Parent, and identifies the parent element. Elements that are the parent of one element can themselves have a parent element, and you can navigate this multi-level hierarchy in the Analytics Hub.

The example used in this topic is the Location breakdown for the Number of open incidents indicator. A child relation and a parent relation are needed to navigate the several levels of hierarchy, such as from region to country to city and back.

![Navigating from Germany to child locations or to the parent EMEA region.](../image/child-locations.png)

**Note:** Breakdown relations are one-way relationships. Define multiple breakdown relations to create a bi-directional relationship.

## Procedure

1.  Navigate to **All** &gt; **Breakdowns** &gt; **Breakdown Relations** and click **New**.

2.  In the **Breakdown** and **Related breakdown** fields, select the breakdown whose elements you want to navigate between.

    These fields have the same value when you are creating a relation between elements of the same breakdown. For our example, select the **Location** breakdown in both fields.

3.  In the **Table** field, select the same table as the breakdown source facts table.

    In our example, select **Location \[cmn\_location\]**.

4.  Fill in the rest of the form, depending on whether you are creating a child, a parent, or a sibling/peer relation.

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


## Result

After you submit the Breakdown Relation form, the navigation options are available in the Analytics Hub for the relevant indicator. You do not need to run a data collection job first.

## What to do next

View examples of breakdown relations that are shipped by default in every instance. For the Location breakdown, the **Child Location** and **Parent Location** breakdown relations are included. The **Sibling Group** breakdown relation is an example of a sibling or peer relation.

**Parent Topic:**[Navigating breakdown elements with breakdown relations](../concept/breakdown-relations.md)

