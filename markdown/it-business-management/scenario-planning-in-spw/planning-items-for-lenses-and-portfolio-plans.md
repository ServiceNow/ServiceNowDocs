---
title: Planning item configuration for lenses and portfolio plans
description: Learn about the types of default and custom planning items that planning managers can work with in Strategic Planning Workspace.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Planning item configuration for lenses and portfolio plans

Learn about the types of default and custom planning items that planning managers can work with in Strategic Planning Workspace.

For every portfolio plan that you build using a lens, only those item types that are added to that lens are available for planning. For example, a lens XYZ has epics and projects added to it. Then, in any portfolio plan that you build using the XYZ lens, you can plan for work in the form of epics and projects only.

## Default planning items

By default, you can use Projects, Demands, and Epics as planning items for your lens and build plans using them.

## Pre-defined custom planning items

If you want to use a different item type, you can use up to five pre-defined custom planning item tables that are available in your ServiceNow instance.

1.  Select one of the custom planning item type tables available. See [Components installed with Strategic Planning Workspace](../reference/components-installed-with-alignment-planner-workspace.md).
2.  Modify the label of the table that you want to use.

    For example, you want to plan for incidents, change the label of Custom planning item 1 to **Incident**.

3.  Add this table to the **sn\_align\_core.planning\_item\_types\_allow\_list** property. See [Enable custom item types in Strategic Planning](../task/enable-custom-item-types-strategic-planning-workspace.md).

## New custom planning items

If you've used up all these five pre-defined custom planning item tables and want a different item type to use for your portfolio plans, you can define new item types. See [Define a new planning item type in Strategic Planning](../task/create-planning-organization-and-planning-item-type.md).

