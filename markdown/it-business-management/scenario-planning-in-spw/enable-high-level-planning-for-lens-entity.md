---
title: Enable high-level planning for a lens entity
description: To enable high-level planning on for an entity in Strategic Planning Workspace, update the lens entity configuration.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [High-level planning configuration in Strategic Planning, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Enable high-level planning for a lens entity

To enable high-level planning on for an entity in Strategic Planning Workspace, update the lens entity configuration.

## Before you begin

[Create portfolio plan configuration for high-level planning](create-portfolio-plan-configuration-for-high-level-planning.md).

Role required: admin

## About this task

For the table that you want to enable high-level planning, set the **Planning enabled** field to **Yes** in the Lens form. Completing this task would enable your planning managers to create portfolio plans using this table as a planning item, in Strategic Planning Workspace.

For this task, consider the example of Strategic Investments as the lens and the Strategic Priority \[sn\_gf\_strategy\] table as the high-level planning entity.

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Lenses**.

2.  Select and open the lens that you want to use for high-level planning.

    For example, select **Strategic Investments**.

3.  In the Lens structures related list of the Lens form, set the **Planning enabled** field of your high-level entity to **true**.

    For example, set the Planning enabled field of Strategic Priority entity to **true**.

    If your high-level entity is not a part of your lens structure, you can add it. See [Add or modify lens structure in Strategic Planning](define-lens-structure-in-alignment-planner-workspace.md).

    ![Planning enabled field for a lens entity in the Lens structures related list of a Lens form.](../images/planning-enabled-field.png)

4.  Save the Lens form.


## Result

Your planning managers can now create portfolio plans on the Strategic Investment lens and use Strategic Priority as their planning item.

**Important:** Once a portfolio plan is creating based on this entity, you can neither disable high-level planning for it nor delete the entity record from the lens structure.

## What to do next

[Populate global rank for high-level planning items](populate-global-rank-for-high-level-planning-items.md).

