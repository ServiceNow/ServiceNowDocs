---
title: Modify lens structure in Portfolio Planning
description: Add or modify entities for your lens structure so that your planning managers can start creating their portfolio plans in Portfolio Planning.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring lens in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Modify lens structure in Portfolio Planning

Add or modify entities for your lens structure so that your planning managers can start creating their portfolio plans in Portfolio Planning.

## Before you begin

Ensure that your application scope is set to **Portfolio Planning Core**.

Role required: admin

## About this task

For a lens, add entities to modify its existing structure. You can add up to six entities in a lens structure. For more information on lens and its structure, see [Configuring lens in Portfolio Planning](../concept/configuring-lens-in-portfolio-planning.md).

## Procedure

1.  Navigate to **All** &gt; **Portfolio Planning** &gt; **Lenses**.

2.  From the Lenses list, select a lens for which you want to update the lens structure.

3.  Add an entity to the lens structure.

    1.  From the Lens structure related list, select **New.**

    2.  On the form, fill in the fields.

        For field information, see [Lens structure form](../reference/lens-structure-form-portfolio-planning.md).

    3.  Select **Submit.**

4.  Repeat step 3 to complete adding all your lens entities.

    -   Add the entities in a top-down manner:

        Add the top-level entity first, followed by the second-level entity, followed by the third, and so on.

    -   Ensure that every entity, except the top-level, has a parent entity reference.

        For example, the second-level entity must refer to the top-level entity as its parent.

        ![Parent references in a lens structure](../../alignment-planner-workspace/images/lens-structure-entities-parent.png)


## What to do next

1.  Verify that the Planning item table \[sn\_align\_core\_planning\_item\] has a field that references the bottom entity of this lens.
2.  Ensure that the following form views for all the planning item types that are associated in your lens contains a field for the bottom entity of your lens structure.
    -   APW Preview
    -   APW New
    -   APW Default
3.  Update the roadmap configuration for the tables of all planning item types that you associate with this lens:

    Add the bottom entity of this lens structure and its parent to **Group by fields** and **Color by fields**. These fields are used as the default group by and color by settings for the portfolio roadmap. See [Customize the display preferences for Prioritization and Roadmap in Portfolio Planning Workspace](update-source-table-preferences-roadmap-portfolio-planning.md).

4.  Validate your lens configuration and activate it. See [Activate a lens in Portfolio Planning](activate-lens-portfolio-planning.md).

