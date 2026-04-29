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

For an organization that handles multiple products, operational lines, and practices, having a single control for an entity and a control objective combination is ineffective. Multiple levels of control objectives, controlled and managed centrally helps to get the granular control information.

The benefits of creating multiple controls for the same entity and control objective combinations are:

-   You can create high-level control objectives and more granular controls.
-   The control owner, compliance manager, and compliance user can manage the compliance library more efficiently.

You can create multiple controls for the same combination of entity and control objective by enabling the **Inherit from control objective** option in the [Control form](../task/t_CreateAControl.md#mutliple-control-entity-co). Controls can be created either through item generation process or, by default, inherited from the control objective. Such controls have a unique name as they are unique to the entity–control objective combination. By default, only one control can be inherited from the control objective. However, if you want to create multiple controls for the same combination of entity and control objective you have to do it manually and the name of the control must be unique.

When you select the **Inherit from control objective** option in the Control form, the control automatically inherits the name and description of the control objective. However, when the option is not selected, then you must enter the name of the control manually.

**Note:** Suppose multiple products or systems in your organization fulfill the same control objective through a shared mechanism. For example, two Single Sign On products that both satisfy the same requirement . Consider converting the control to a common control instead of creating multiple controls manually. A common control can be associated with multiple reliant entities without requiring a separate control for each.

For more information, see [Convert standard control to common control and add reliant entities](../../grc-workspace-compliance/task/convert-standard-control-common.md).

