---
title: Managing equipment models
description: The Equipment Model Manager in the Industrial Workspace enables you to review and manage ISA-95 equipment model data. You use it to review imported equipment model data or to manually create an equipment model.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Industrial Process Manager, Operational Technology]
---

# Managing equipment models

The Equipment Model Manager in the Industrial Workspace enables you to review and manage ISA-95 equipment model data. You use it to review imported equipment model data or to manually create an equipment model.

## Equipment Model Manager in the Industrial Workspace

An equipment model maps the operational elements of a particular facility. For example, an industrial facility in Atlanta that stores materials, and uses them to produce cars. With the Equipment Model Manager, you can view selected equipment model entities and any related records for specific industrial sites. The Equipment Model Manager contains the following functionalities to help you manage the equipment model entities in your OT environment:

-   Viewing a graphical representation of an equipment model hierarchy and its relationship to other equipment model entities.
-   Viewing or mapping upstream or downstream production processes.
-   Reviewing child equipment model entities.
-   Reviewing or associating additional OT devices with the selected equipment model entity.
-   Adding child equipment model entities to your favorites and updating your view to show only your favorites.
-   Keeping record context available when viewing or creating multiple records by opening the records in a single row of tabs.

**Note:** Users with an assigned cmdb\_ot\_isa\_admin role can view equipment model entities for any site. However, users with assigned cmdb\_ot\_isa\_editor or cmdb\_ot\_isa\_viewer roles can only access those sites that an administrator has granted access to for specific users. To learn more about granting site access, see [Assign or remove equipment model site access for non-administrators](create-user-criteria-for-equipment-model-entity-site-users.md).

-   **[Review and update the equipment model details](equipment-model-workspace.md)**  
Review and update the details for an equipment model that you imported into the ServiceNow AI Platform so that you can make sure that the information is correct. You can also manually create a new equipment model entity and then add details to it.
-   **[Automated mapping of OT devices to the Equipment Model](../../mftg-manufacturing/task/automate-mappings-between-ot-assets-and-equipment-model-entity.md)**  
Automate mapping of OT devices to the production process.​

**Parent Topic:**[Using Industrial Process Manager with the Operational Technology Manager](../concept/using-manufacturing-process-manager.md)

