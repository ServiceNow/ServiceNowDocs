---
title: Work item dependencies in EAP
description: Learn about work item dependencies and how they're shown on the Planning board for a team in Enterprise Agile Planning.
locale: en-US
release: xanadu
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Perform PI planning, Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Work item dependencies in EAP

Learn about work item dependencies and how they're shown on the Planning board for a team in Enterprise Agile Planning.

## Dependencies overview

While planning, it’s essential to know how your work items are connected with each other. Knowing dependencies between work items enables identification of challenges, coordination for resolution, and an overall improvement in collaboration between teams. Unless you know the dependency for each item, you could be at risk of not scheduling the right work for the right iteration. To get started with dependencies in EAP, see [Create and manage dependencies between work items in EAP](../task/create-dependencies-between-work-items-in-eap.md).

## Dependency line colors

On the Planning board in EAP, enable the **Dependencies** toggle to view dependencies lines across teams. The color of the dependency line indicates how the stories are scheduled.

-   Purple: The prerequisite story is scheduled in an earlier sprint than the dependent story. This dependency doesn't require any changes.
-   Yellow: The prerequisite story is scheduled in the same sprint as the dependent story. In this case, rescheduling the stories might or might not be necessary.
-   Red: The prerequisite story is scheduled in a later sprint than the dependent story. In this case, rescheduling stories is necessary.

**Note:** These colors are applicable to the Planning board of ARTs and Agile Teams because they typically involve a planning calendar.

-   Dependencies on the Planning board of a Solution Train or Portfolio appear in purple and don’t indicate any scheduling conflicts.
-   Dependencies on the Planning board of an Agile Team appear in Yellow because they're scheduled for the same Sprint.

![Dependency line colors in ART Planning board.](../images/eap-dependencies.png "Dependency lines for an ART")

## Dependencies related lists for work items

Dependencies added to a work item are displayed in its Full details page. The dependent and prerequisite items are listed in the related lists of this work item. You can also add new dependencies from these related lists.

The name of these related lists varies between Epic, Capability, Feature, and Story. Based on the type of item that you're viewing, the lists could be named as Dependent items, Depends on, Prerequisite stories, and Dependent stories.

The following screenshot shows the dependencies related lists for a Story.

![Related lists for dependencies for a story in EAP.](../images/eap-dependencies-related-lists.png)

-   **[Create and manage dependencies between work items in EAP](../task/create-dependencies-between-work-items-in-eap.md)**  
Draw work item dependencies in real-time across teams and iterations and visually analyze them while you collaborate using the Planning board in Enterprise Agile Planning.

**Parent Topic:**[Perform PI planning in EAP](pi-planning-eap.md)

**Related topics**  


[Create and manage dependencies between work items in EAP](../task/create-dependencies-between-work-items-in-eap.md)

