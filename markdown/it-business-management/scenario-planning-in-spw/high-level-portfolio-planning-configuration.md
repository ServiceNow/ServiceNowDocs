---
title: High-level planning configuration in Strategic Planning
description: If your planning managers need high-level planning enabled for items other than the default ones, you need to update the configuration for lens entities and portfolio plans.
locale: en-US
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# High-level planning configuration in Strategic Planning

If your planning managers need high-level planning enabled for items other than the default ones, you need to update the configuration for lens entities and portfolio plans.

By default, Strategic Programs, Programs \(pm\_program\), and Initiatives are the items that are enabled for high-level planning. Also by default, the Product Enhancement entity with the Digital Product lens is enabled for high-level planning. To enable other planning item types, complete the following configuration tasks.

**Note:** High-level planning is enabled for Strategic Planning v2.1.0 and higher.

## For items that extend the Planning Item table

For example, you added Custom planning item 1 \[sn\_align\_core\_custom\_planning\_item\_1\] to your lens structure and you want to use it for high-level portfolio plans. In the Lens structure related list for your lens, set the **Planning enabled** field to **true** for the Custom planning item 1 entity. For detailed information, see [Enable high-level planning for a lens entity](enable-high-level-planning-for-lens-entity.md).

## For items that do not extend the Planning Item table

Consider the example of enabling high-level planning for the Strategic Priority \[sn\_gf\_strategy\] planning item type.

1.  Create a global rank column in the Strategic Priority \[sn\_gf\_strategy\] table. See [Create global rank column for high-level planning](create-global-rank-field-to-enable-high-level-planning.md).
2.  Create rank configuration for the new global rank column. See [Create rank configuration for high-level planning](create-rank-configuration-enable-high-level-planning.md).
3.  Create portfolio plan configuration for the Strategic Priority \[sn\_gf\_strategy\] table. See [Create portfolio plan configuration for high-level planning](create-portfolio-plan-configuration-for-high-level-planning.md).
4.  Enable high-level planning for the Strategic Priority \[sn\_gf\_strategy\] entity in the lens structure record. See [Enable high-level planning for a lens entity](enable-high-level-planning-for-lens-entity.md).
5.  Run diagnostics and fix script to populate global rank for all existing Strategic Priority records. See [Populate global rank for high-level planning items](populate-global-rank-for-high-level-planning-items.md).
6.  Create a business rule for the Strategic Priority \[sn\_gf\_strategy\] table to enable setting a global rank for any future records created. See [Create a business rule for high-level planning](create-a-business-rule-for-high-level-planning.md).

**Tip:** While choosing a table as your high-level planning entity, ensure that it has fields such as start date and end date, owner or assigned to, name or short description, so that this can be used as a planning item. For example, you cannot use the Organization or Product tables as your high-level planning entities. On the other hand, the Strategic Priority tables meets the requirements of a planning item and can be configured for high-level planning.

Once all these tasks are complete, your planning manager can create a high-level portfolio plan for the desired entity - for this example, portfolio plans can be created to prioritize and roadmap the strategic priorities of the company, and to view how the work across the company is aligned to these strategic priorities.

