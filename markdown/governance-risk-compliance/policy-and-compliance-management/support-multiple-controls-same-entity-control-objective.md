---
title: Multiple controls for compliance management
description: You can create multiple controls for a unique combination of an entity and a control objective to get granular control information.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage controls, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Multiple controls for compliance management

You can create multiple controls for a unique combination of an entity and a control objective to get granular control information.

Controls can be created through the item generation process or inherited directly from the control objective. By default, only one control can be inherited from a control objective.

For organizations that manage multiple products, operational lines, or practices, a single control per entity–control objective combination may not provide sufficient granularity.

Creating multiple controls for the same entity and control objective combination lets you:

-   Define high-level control objectives with more detailed and specific controls.
-   Give control owners, compliance managers, and compliance users more precise visibility into the compliance library.

To create multiple controls for the same entity and control objective combination, disable the Inherit from control objective option in the Control form.

For more information, see [Control form](../task/t_CreateAControl.md#mutliple-control-entity-co).

When Inherit from control objective is enabled, the control automatically inherits the name and description from the control objective.

> **Note:** Beyond the first inherited control, additional controls for the same combination must be created manually.

**Note:** Suppose multiple products or systems in your organization fulfill the same control objective through a shared mechanism. For example, two Single Sign On products that both satisfy the same requirement . Consider converting the control to a common control instead of creating multiple controls manually. A common control can be associated with multiple reliant entities without requiring a separate control for each.

For more information, see [Convert standard control to common control and add reliant entities](../../grc-workspace-compliance/task/convert-standard-control-common.md).

