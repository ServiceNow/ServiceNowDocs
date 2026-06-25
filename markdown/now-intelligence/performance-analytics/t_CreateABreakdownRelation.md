---
title: Create a breakdown-to-breakdown relation
description: To set up navigation in a visualization between the elements of two breakdowns at the same level, create a breakdown relation between the breakdowns. A table must exist with fields that reference the records for both breakdowns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/t\_CreateABreakdownRelation.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Navigating breakdown elements with breakdown relations, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a breakdown-to-breakdown relation

To set up navigation in a visualization between the elements of two breakdowns at the same level, create a breakdown relation between the breakdowns. A table must exist with fields that reference the records for both breakdowns.

## Before you begin

Review the use cases for breakdown relations in [Navigating breakdown elements with breakdown relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/breakdown-relations.md).

**Important:** Platform Analytics features, such as KPI Details and data visualizations, do not support breakdown relations.

Role required: pa\_data\_collector, pa\_power\_user, admin

**Note:** While a business analyst, typically with the pa\_power\_user role, is most likely to know what breakdown relations to create, creating them requires the knowledge and access to tables of a technical expert with pa\_data\_collector. A pa\_admin is likely to understand both. Consider having either a pa\_admin create the relation or have a collaboration between a pa\_power\_user and a pa\_data\_collector.

## About this task

You want to be able to navigate quickly between two breakdowns at the same level that are logically related.

**Note:** Breakdown relations are one-way relationships. To create a bi-directional relationship, define multiple breakdown relations.

## Procedure

1.  Navigate to **All** &gt; **Breakdowns** &gt; **Breakdown Relations** and tap **New**.

2.  Fill in the fields on the form, as follows.

    |Field|Description|Example|
    |-----|-----------|-------|
    |Breakdown|Select the breakdown that this relationship belongs to. You can access related breakdowns from this breakdown only.|If you want a selection of group members to appear when you select an Assignment Group, the **Breakdown** is Assignment Group.|
    |Related breakdown|Select the breakdown you want to associate with the first breakdown.|If you want a selection of group members to appear when you select an Assignment Group, the related breakdown with the Assignment Group members is Assigned To.|
    |Table|Select a table with fields that reference the facts table records of the sources of both breakdowns. For many-to-many relationships, select a many-to-many table. For one-to-many relationships, select a facts table.|The Assignment Group breakdown uses Group data. The Assigned To breakdown uses User data. Assignment Groups can have many members, and a user can be a member of more than one Assignment Group, so they have a many-to-many relationship. Therefore, you select the Group Member \[sys\_user\_grmember\] table, which is a many-to-many table that joins groups and users.|
    |Breakdown field|Select the field from the specified table that identifies the breakdown element you can navigate from.|To relate Assignment Group and Assigned To, select the **Group** field. This field in the Group Member \[sys\_user\_grmember\] table identifies the element of the Assignment Group breakdown.|
    |Related breakdown field|Select the field from the specified table that identifies the breakdown elements you can navigate to when viewing this relation.|To relate Assignment Group and Assigned To, select the **User** field. This field in the Group Member \[sys\_user\_grmember\] table identifies the element of the Assigned To breakdown.|
    |Common field|Leave this field empty when defining a relation between breakdowns.| |
    |Conditions|Define any further conditions that a record must fulfill to appear as a related breakdown for this relationship.|Add the condition **\[User.Active\] \[is\] \[true\]** to filter out inactive group members.|


## Result

After you submit the Breakdown Relation form, put a filter element and an indicator scorecard element on a Next Experience dashboard. The filter is the starting point. It acts as a source, and the breakdown configured for the indicator scorecard acts as a target. The breakdown relation record defines how these two elements are connected. The filter should use the breakdown source table from the primary breakdown as its filter source. It should filter all indicators with that breakdown. The indicator scorecard should use the related breakdown. For example, consider the following:

-   A breakdown relations record named Members, where the Breakdown is Assignment Group and the related breakdown is Assigned To. The table is Group Member \[sys\_user\_grmember\], which has fields on both breakdown sources. The Breakdown Field is Group and the Related Breakdown Field is User.
-   A filter on the Group \[sys\_user\_group\] table that filters indicators with the Assignment Group breakdown.
-   An indicator scorecard that shows the Number of open incidents indicator. The breakdown is Assigned To, and the scorecard follows the Members breakdown relation.

When an Assignment Group is selected in the filter, the members of that assignment group are displayed in the indicator scorecard.

\[Omitted image "bkdown2bkdown-relation.png"\] Alt text: Dashboard using an assignment group filter to show the members of an assignment group in an indicator scorecard with the Assigned To breakdown.

## What to do next

View examples of breakdown relations that are shipped by default in every instance. The example shown here is the **Members** breakdown relation. The **Member of** breakdown relation provides navigation in the reverse direction, starting with an element in Assigned To and navigating to an Assignment Group. Lastly, the **Manager** breakdown relation is similar to **Members**, but because each assignment group has only one manager, it shows a many-to-one relationship. It thus uses a facts table instead of a many-to-many table.

**Parent Topic:**[Navigating breakdown elements with breakdown relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/breakdown-relations.md)

**Related topics**  


[Create an Indicator Scorecard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-dv-indicator-scorecard.md)

[Create or add a filter on an inline dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/select-workspace-filter-type.md)

