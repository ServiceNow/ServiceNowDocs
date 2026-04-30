---
title: Navigating breakdown elements with breakdown relations
description: Breakdown relations open a new navigation path for viewing breakdown scores, by moving from one breakdown element to another breakdown element. Breakdown relations can be between the elements of different breakdowns, or they can be within a hierarchical structure of elements in the same breakdown. Breakdown relations affect navigation on the Analytics Hub and in breakdown widgets.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Indicator breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Navigating breakdown elements with breakdown relations

Breakdown relations open a new navigation path for viewing breakdown scores, by moving from one breakdown element to another breakdown element. Breakdown relations can be between the elements of different breakdowns, or they can be within a hierarchical structure of elements in the same breakdown. Breakdown relations affect navigation on the Analytics Hub and in breakdown widgets.

**Important:** Platform Analytics features, such as KPI Details and data visualizations, do not support breakdown relations.

You can use breakdown relations to navigate between the elements of a single breakdown that are in a hierarchical relationship. For example, the Location breakdown has a hierarchy of 'parent' and 'child' elements, where a country can be the parent of cities. Breakdown relations let an Analytics Hub viewer navigate from a country down into a city, from a city to the country, or between cities in the same country.



![Navigating from Germany to child locations or to the parent EMEA region.](../image/child-locations.png)

Similarly, a breakdown widget can show the parent, child, or sibling elements of the element that was chosen for the breakdown dashboard. For more information about using breakdown relations on breakdown dashboards, see [Showing breakdown relations on dashboards](c_ShowBkdwnRltnsWdgts.md).

![A breakdown dashboard with a breakdown widget showing the child elements of the EMEA element](../image/Breakdown_relations_widget.png "Breakdown dashboard displaying children of the EMEA element")

Breakdown relations also enable navigation between the elements of different first-level breakdowns. For example, first choose an element of the Assignment Group breakdown, then look at the Members breakdown relation. In this relation, navigate to an element of the Assigned To breakdown. The selected member of Assigned To is not necessarily a member of the Assignment Group. Furthermore, the number of assignments of members of Assigned To is greater than the number of assignments of the selected Assignment Group. You see the total of all assignments, not only the assignments in the originally selected Assignment Group. You are changing which first-level breakdown you are looking at, not drilling down to a second level of breakdown and element. Again, this breakdown relation can be used both on the Analytics Hub and in a breakdown widget on a breakdown dashboard.

![Navigating from an assignment group to its members](../image/breakdown-relation-member.gif "Navigating on the Analytics Hub between elements of different breakdowns")

More details about these cases for using breakdown relations are in the topics about creating breakdown relations.

-   **[Create a breakdown relation between breakdowns](../task/t_CreateABreakdownRelation.md)**  
To set up navigation in a visualization between the elements of two breakdowns at the same level, create a breakdown relation between the breakdowns. A table must exist with fields that reference the records for both breakdowns.
-   **[Create relations between elements of one breakdown](../task/create-relation-btwn-bkdn-elements.md)**  
Use a breakdown relation to set up navigation on an Analytics Hub between a hierarchy of elements within the same breakdown. A field in the breakdown records must identify the hierarchical relationship of one record to another.

**Parent Topic:**[Indicator breakdowns](c_CreatingBreakdowns.md)

