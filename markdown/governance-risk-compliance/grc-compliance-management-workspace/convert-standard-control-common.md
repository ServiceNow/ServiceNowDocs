---
title: Convert standard control to common control and add reliant entities
description: Mark a control as common and associate reliant entities to it. Test the common control tied to the primary entity. The reliant entities inherit the results of the common control.
locale: en-US
release: australia
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Testing common control and implementing results on multiple reliant entities, Manage controls using the Compliance Workspace, Use, GRC Compliance workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Convert standard control to common control and add reliant entities

Mark a control as common and associate reliant entities to it. Test the common control tied to the primary entity. The reliant entities inherit the results of the common control.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_manager, sn\_compliance\_ws.corporate\_compliance\_analyst

## About this task

All existing controls are termed as standard controls. You can convert a standard control to common and reverse its function as standard if you so require. However, by default all controls whether existing or created are standard.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, click the List icon \(![List](../../grc-workspace-vrm/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **All controls**.

    You can either [create a control](create-control-ws.md) by clicking the **New** button or select one of the existing standard controls from the All controls list and convert it to a common control. Either way, the control is standard, by default, and you must convert it to common to add reliant entities.

    **Note:** Before you convert a control from standard to common, ensure that you select a value in the **Control objective** field, and save the form details. Control objective is required for a common control as there are validations to ensure that the common control does not have the same Name, Entity \(primary or reliant\), and Control objective combination as any other control.

4.  Click the More Actions ![More actions button.](../image/MoreActionsbutton.png) on the top right.

5.  Select the **Convert to common** list UI action.

    The **Convert to common** UI action appears only when the control is in the initial states such as **Draft** or **Attest**. When the control progresses beyond these states, then it can neither be converted to common nor reverted as standard control. **Convert to standard** UI action does not appear when the control is common and in the **Review** state.

    When a control is common, its **Source** field is Entity. When the control is converted back to standard, the entity source is removed if it was added when the control was converted to common. When a common control is converted to standard control, the entity type and reliant entity type associations are deleted.

6.  Click **Okay**.

    **Note:**

    -   The **Function** field changes from Standard control to Common control. Also, the Reliant entities and Reliant entity types related lists appear on the control form to help you add the reliant entities.
    -   When a standard control changes to common control, an additional **Entity based access restriction** option is added. This option is disabled by default. When **Entity based access restriction** is enabled, only users or user groups included in the access configuration for the entities associated with this control can access it.
7.  To add reliant entities, select the Reliant entities related list.

    1.  Click the **Add** button.

    2.  Select the entities in the Entities pop-up and click **Add**.

        The message confirms that the reliant entities are added successfully to the common control. The association of the entity as reliant to the common control creates a record in the Item to entity \[sn\_grc\_m2m\_item\_entity\] table.

        If you have an entity type with entities, then you can select the entity type to add the bulk of entities instead of selecting them one by one.

    3.  To pick out a primary entity and associate it as a reliant entity, click the **Add from existing control** button.

        This action enables you to:

        -   retire that existing control
        -   associate the entities of that control as reliant entities
        You can add up to 15 entities at a time by this option. When you select the entities and click **Add**, not all existing entities are added. All of the entities may be added, some of them may be added, or sometimes none of them is added. For reasons as to why the entities are skipped from being added and their controls are not retired, see the [GRC Common control inheritance \[KB1221601\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1221601) article in the Now Support Knowledge Base.

        **Note:** You must log in to Now Support to view the articles.

        When you select the **Continue to add** button in the pop-up, the existing control is retired and its associated entity is added as reliant entity. The control is treated as manually retired control.

    4.  To remove a reliant entity, select the reliant entity and click **Remove**.

8.  To add entity types, select the Reliant entity types related list.

    1.  Click the **Add** button.

    2.  Select the entity type in the Reliant entity types pop-up and click **Add**.

        The downstream action of associating entity types to a common control creates an upstream action of associating entities to the common control. All the entities that are added as part of the entity type are also listed in the Related entities related list. **Added from entity type** column lists the source of the entity type.

        The association of the entity type as reliant to the common control creates a record in the Item to entity type \[sn\_grc\_m2m\_item\_entity\_type\] table.

        **Note:** For more information on the m2m tables that store the records of entity and common control association, see [Tables installed with Policy and Compliance Management](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#table_qlq_g3m_vs).

        The advantage of using Reliant entity types is that even if you update the entity type later by adding more entities to it, after it is associated to a common control, then those added entities get automatically associated as reliant entities.

    3.  To remove a reliant entity type, select the record and click **Remove**.

9.  To add a risk to the control, select the Risks related list and click the **Add from reliant entities** button.

    Based on the reliant entities' association with risks, you can associate the common control with risks. For more information, see [Common controls in Risk Management](../../grc-workspace-risk/concept/shared-common-controls-in-risk-management.md).

10. To view the reliant entities associated to the control, click the **360º view** button from the control record.

    The primary entity and the list of all reliant entities are displayed in a distinctive visualization.


## Result

Associating reliant entities to a common control has an [impact on compliance scoring](../concept/compliance-score-common-control.md).

