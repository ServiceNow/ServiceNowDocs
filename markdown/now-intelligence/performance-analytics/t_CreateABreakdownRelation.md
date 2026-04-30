---
title: Create a breakdown relation between breakdowns
description: To set up navigation in a visualization between the elements of two breakdowns at the same level, create a breakdown relation between the breakdowns. A table must exist with fields that reference the records for both breakdowns.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Navigating breakdown elements with breakdown relations, Performance Analytics breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Create a breakdown relation between breakdowns

To set up navigation in a visualization between the elements of two breakdowns at the same level, create a breakdown relation between the breakdowns. A table must exist with fields that reference the records for both breakdowns.

## Before you begin

Review the use cases for breakdown relations in [Navigating breakdown elements with breakdown relations](../concept/breakdown-relations.md).

**Important:** Platform Analytics features, such as KPI Details and data visualizations, do not support breakdown relations.

Role required: pa\_data\_collector, pa\_power\_user, admin

**Note:** While a business analyst, typically with the pa\_power\_user role, is most likely to know what breakdown relations to create, creating them requires the knowledge and access to tables of a technical expert with pa\_data\_collector. A pa\_admin is likely to understand both. Consider having either a pa\_admin create the relation or have a collaboration between a pa\_power\_user and a pa\_data\_collector.

## About this task

You want to be able to navigate quickly between two breakdowns at the same level that are logically related. The example used in this topic involves the breakdowns Assignment Group and Assigned To for the indicator Number of open incidents. In the following animation, you switch from seeing the number of incidents assigned to the Oracle Support group and seeing the number of incidents assigned to Candace Bruckman. Both breakdowns are first level, which means that you see the total number of incidents assigned to Oracle Support and the total assigned to Candace Bruckman. If you had selected Candice as a second-level breakdown instead of through a breakdown relation, you would have seen only the Oracle Support issues that they were working on. ![Navigating from an assignment group to its members](../image/breakdown-relation-member.gif)

**Note:** Breakdown relations are one-way relationships. To create a bi-directional relationship, define multiple breakdown relations.

## Procedure

1.  Navigate to **All** &gt; **Breakdowns** &gt; **Breakdown Relations** and click **New**.

2.  Fill in the fields on the form, as follows.

    |Field|Description|Example|
    |-----|-----------|-------|
    |Breakdown|Select the breakdown that this relationship belongs to. You can access related breakdowns from this breakdown only.|For our example, where you want a selection of group members to appear when you select an Assignment Group, the **Breakdown** is Assignment Group.|
    |Related breakdown|Select the breakdown you want to associate with the first breakdown.|For our example, the related breakdown with the Assignment Group members is Assigned To.|
    |Table|Select a table with fields that reference the facts table records of the sources of both breakdowns. For many-to-many relationships, select a many-to-many table. For one-to-many relationships, select a facts table.|The Assignment Group breakdown uses Group data. The Assigned To breakdown uses User data. Assignment Groups can have many members, and a user can be a member of more than one Assignment Group, so they have a many-to-many relationship. Therefore, you select the Group Member \[sys\_user\_grmember\] table, which is a many-to-many table that joins groups and users.|
    |Breakdown field|Select the field from the specified table that identifies the breakdown element you can navigate from.|In our example, you select the **Group** field. This field in the Group Member \[sys\_user\_grmember\] table identifies the element of the Assignment Group breakdown.|
    |Related breakdown field|Select the field from the specified table that identifies the breakdown elements you can navigate to when viewing this relation.|In our example, you select the **User** field. This field in the Group Member \[sys\_user\_grmember\] table identifies the element of the Assigned To breakdown.|
    |Common field|Leave this field empty when defining a relation between breakdowns.| |
    |Conditions|Define any further conditions that a record must fulfill to appear as a related breakdown for this relationship.|In our example, you add the condition **\[User.Active\] \[is\] \[true\]** to filter our inactive group members.|


## Result

After you submit the Breakdown Relation form, the navigation options are available in the Analytics Hub for the relevant indicator. You do not need to run a [data collection job](../concept/performance-analytics-glossary.md#) first.

## What to do next

View examples of breakdown relations that are shipped by default in every instance. The example shown here is the **Members** breakdown relation. The **Member of** breakdown relation provides navigation in the reverse direction, starting with an element in Assigned To and navigating to an Assignment Group. Lastly, the **Manager** breakdown relation is similar to **Members**, but because each assignment group has only one manager, it shows a many-to-one relationship. It thus uses a facts table instead of a many-to-many table.

**Parent Topic:**[Navigating breakdown elements with breakdown relations](../concept/breakdown-relations.md)

