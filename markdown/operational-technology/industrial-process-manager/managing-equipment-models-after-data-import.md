---
title: Managing equipment models
description: The Equipment Model Manager enables you to review and manage ISA-95 equipment model data. You use it to review imported equipment model data or to manually create an equipment model.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Industrial Process Manager, Operational Technology]
---

# Managing equipment models

The Equipment Model Manager enables you to review and manage ISA-95 equipment model data. You use it to review imported equipment model data or to manually create an equipment model.

An equipment model maps the operational elements of a particular facility. For example, an industrial facility in Atlanta that stores materials, and uses them to produce cars. Using the Equipment Model Manager, you can view selected equipment model entities for specific industrial sites, and perform the following tasks:

-   View a graphical representation of an equipment model hierarchy and its relationship to other entities.
-   View or map upstream or downstream production processes.
-   Review child entities.
-   Review or associate additional OT devices with the selected equipment model entity

**Note:** Users with an assigned cmdb\_ot\_isa\_admin role can view equipment model entities for any site. However, users with assigned cmdb\_ot\_isa\_editor or cmdb\_ot\_isa\_viewer roles can only access those sites that an administrator has granted access to for specific users. To learn more about granting site access, see [Assign or remove equipment model site access for non-administrators](create-user-criteria-for-equipment-model-entity-site-users.md).

-   **[Review and update the equipment model details](equipment-model-workspace.md)**  
Review and update the details for an equipment model that you imported into the ServiceNow AI Platform so that you can make sure that the information is correct. You can also manually create a new equipment model entity and then add details to it.
-   **[Automated mapping of OT devices to the Equipment Model](../../mftg-manufacturing/task/automate-mappings-between-ot-assets-and-equipment-model-entity.md)**  
Automate mapping of OT devices to the production process.​

**Parent Topic:**[Using Industrial Process Manager with the Operational Technology Manager](../concept/using-manufacturing-process-manager.md)

