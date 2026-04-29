---
title: Generate a location hierarchy
description: When no locations exist, generate a complete location hierarchy for an ISA equipment model entity tree to establish location references that match the ISA hierarchy.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Generate a location hierarchy

When no locations exist, generate a complete location hierarchy for an ISA equipment model entity tree to establish location references that match the ISA hierarchy.

## Before you begin

Ensure the sn\_isa\_model.isa\_entity.validate\_and\_generate\_locations system property is enabled. For more information, see [ISA Equipment Model system properties](../reference/isa-equipment-model-system-properties.md).

Role required: cmdb\_ot\_isa\_editor

## Procedure

1.  Navigate to the Industrial Workspace.

2.  Select the Equipment model ![](../image/equip-model-manager-button.png) icon to open the Equipment Model Manager.

3.  Select the equipment model entity that needs a location hierarchy.

    If no location records exist in the selected equipment model hierarchy, the following message appears and you can continue with the auto-generation process:

    "Click Auto generate locations to create and synchronize locations with the Equipment Model Entities."

4.  To continue, select the **Auto Generate Locations** UI action.

    **Note:** You can only continue the auto-generation process if no location reference is found for a node. If a location reference is found, the following message appears and you can't continue the auto-generation process:

    "Cannot auto-generate locations because the entity has existing location references."

5.  If you have existing location references and want to continue the auto-generation process, delete the references or manually populate them for each equipment model entity.

    1.  After deleting or manually populating the location references, verify they're correctly synced in the **Location Validation Map** tab of the equipment model entity record.
    2.  Starting at the bottom level of the map, remediate the nodes with the following messages:

        -   "Invalid Location" - The entity's location parent doesn't match the equipment model entity's parent location.
        -   "Missing Location" - The entity doesn’t have a location assigned to the **Location reference** field.
        Once the bottom level has a valid location reference, the messages disappear.

    3.  Continue this process with each level until all invalid and missing locations are resolved.
    4.  Continue the auto-generation process by selecting the **Auto Generate Locations** UI action.

## Result

A Location \[cmn\_location\] record is created for the equipment model entity and its child entities. The created cmn\_location populates **Location** field for the equipment model entity.

## What to do next

You can also navigate to the **Location Validation Map** tab in the equipment model entity record to see the populated fields and view the location hierarchy node map.

**Parent Topic:**[Review and update the equipment model details](equipment-model-workspace.md)

