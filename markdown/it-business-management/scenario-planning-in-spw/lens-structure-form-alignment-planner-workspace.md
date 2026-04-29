---
title: Lens structure form
description: Learn about the fields of the Lens structure form. Use this form to define a structure for your lens in Strategic Planning.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Form field information for Strategic Planning, Reference, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Lens structure form

Learn about the fields of the Lens structure form. Use this form to define a structure for your lens in Strategic Planning.

<table id="table_hvj_25t_fvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

</td><td>

Source table for your lens entity. An entity represents a planning level in the perspective of your lens.

 Select the entity that is relevant for your planning persona from the perspective of this lens. For example, Department, Product Model, or Business Objective.

</td></tr><tr><td>

Entity filter

</td><td>

Conditions to filter data from your entity source. The filtered data is shown on the workspace for your planning persona to select and plan for.

</td></tr><tr><td>

Top entity

</td><td>

Indicates if this entity is the top-level entity of your lens structure.

</td></tr><tr><td>

Parent entity

</td><td>

Entity that is one level above this entity in your current lens structure.This field is available only if the **Top entity** field isn’t selected.

</td></tr><tr><td>

Reference to parent entity

</td><td>

Column in the current entity table that references the parent entity table.For example:

-   Entity is **Strategic Program \[sn\_align\_core\_program\]**
-   Parent entity is **Department \[cmn\_department\]**

Then the field of the Strategic Program \[sn\_align\_core\_program\] table that references the Department \[cmn\_Department\] table would be **Department**.

 This field is available only if the **Top entity** field isn’t selected.

</td></tr></tbody>
</table>**Parent Topic:**[Form field information for Strategic Planning](form-field-information-for-strategic-planning.md)

**Related topics**  


[Add or modify lens structure in Strategic Planning](../task/define-lens-structure-in-alignment-planner-workspace.md)

