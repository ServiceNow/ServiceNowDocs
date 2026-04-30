---
title: Operational changes in item generation of common controls
description: Operational changes are made in item generation mainly because item generation either creates a control or activates an existing standard control. When it comes to associating a control to an entity, then associating a reliant entity to a common control takes precedence over creating a control for that entity.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use the item generation process, Common GRC features, Governance, Risk, and Compliance]
---

# Operational changes in item generation of common controls

Operational changes are made in item generation mainly because item generation either creates a control or activates an existing standard control. When it comes to associating a control to an entity, then associating a reliant entity to a common control takes precedence over creating a control for that entity.

## Creation of controls

If the existing controls in your system can be used for testing entities, then you can take advantage of the existing data and avoid creating controls. Having many controls can lead to control explosion. If that is not feasible, then you can associate a primary entity with a common control, test the common control, and implement the test results on the reliant entities of the common control. If both these options don’t work, then you can create a control.

To create a common control, select **Common** in the **Function** field of the Control form. Select the **Convert to common** list UI action. A common control is created upon validation. It’s mandatory that you select a control objective before you convert a standard control to common control.

## Association of reliant entities to common control

1.  Use the Reliant entities related list in the Control form to add individual entities to the common control. You can also remove the reliant entities using the **Remove** button.
2.  Use Reliant entity types related list in the Control form to add entity types to the common control. You can also remove the reliant entity types using the **Remove** button.
3.  Use the **Inherit common controls** UI action in the Controls related list of the Risk form to select common controls grouped by control objectives.

**Note:** For more information on reliant entity associations for a common control, see [Create a control using the Compliance Workspace](../../grc-workspace-compliance/task/create-control-ws.md) and [Convert standard control to common control and add reliant entities](../../grc-workspace-compliance/task/convert-standard-control-common.md).

## Item generation – Assumptions

-   There’s no auto-generation of common controls.
-   When the existence of common controls or associations of reliant entities to common control or standard controls are checked, the control’s name, entity, and control objective must match.
-   Order of precedence between standard and common controls:
    -   If reliant association and standard control do not exist, then based on the action type, a standard control is created. Action types, for example can be Add content to entity type, Add document to entity type, Activate content, Activate document.
    -   If reliant association and standard control do not exist, then based on the action type a reliant association to common control is created. Action type can be Add entity type to common control.
    -   If the user's intent is not clear from the action type and a standard control does not already exist, then in conflicting entity type, the preference is to associate the reliant entity to the common control over creation of a standard control. Action type, for example can be Add entity to entity type.

## Item generation changes

<table id="table_w4r_n4y_2wb"><thead><tr><th>

Item generation action type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add entity type to common control

</td><td>

If the entity is not associated with the common item, then the application associates the entity with the common item by creating an m2m association between the two.

</td></tr><tr><td>

Remove entity type from common control

</td><td>

If the entity is associated with the common item, and the Entity types field has other entity types or **Individually\_added** is true in the m2m record, then the application removes the Entity type ID from the Entity types column or deletes the entity to common item m2m record.

</td></tr><tr><td>

Add entity to item

</td><td>

If Risk Management is installed, based on the risk statement associated to the control objective, the risk to common control m2m records are added in the Control to Entity m2m table after considering the reliant entities.

</td></tr><tr><td>

Remove entity from item

</td><td>

-   If Risk Management is installed, based on the risk statement associated to the control objective, risk to common control m2m records are deleted in consideration of the reliant entities.
-   If Privacy Management is installed, then the Processing Activity to common control m2m association based on its reliant entity and also the Processing Activity to control objective m2m association are removed.

</td></tr><tr><td>

Activate entity to item

</td><td>

If Risk Management is installed, based on the risk statement associated to the control objective, risk to common control m2m records are added in the Control to Entity m2m table in consideration of its reliant entities.

</td></tr><tr><td>

Deactivate entity to item

</td><td>

-   If Risk Management is installed, based on the risk statement associated to the control objective, then the risk to common control m2m records are deleted after considering the control's reliant entities.
-   If Privacy Management is installed and the Processing Activity corresponds to a reliant entity, then the Processing Activity to common control m2m association and also the Processing Activity to control objective m2m association are removed.

</td></tr><tr><td>

Activate item

</td><td>

A common item is added:1.  When no standard control exists with the same name, content \(control and control objective\), and entity combination.
2.  If the entity is not reliant on any other common item with the same name, content, and entity.
3.  When the entity is active.

 A standard item is added:

1.  Risk Management and Policy and Compliance Management plugins are installed
2.  Based on the risk statement and control objective association, risks are associated to controls.

</td></tr><tr><td>

Deactivate item

</td><td>

-   Common item: Deactivates all Control to Entity m2m records.
-   Standard item: Deletes risks to control associations based on the Risk statement and Control objective associations.

</td></tr></tbody>
</table>**Parent Topic:**[Using the item generation process to generate controls and risks](../concept/item-generation-process.md)

