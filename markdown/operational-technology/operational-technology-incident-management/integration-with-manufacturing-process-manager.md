---
title: Integrating with Industrial Process Manager
description: Integrate Operational Technology Incident Management with Industrial Process Manager to report incidents on equipment model entities.
locale: en-US
release: xanadu
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Explore, Operational Technology Incident Management, Operational Technology]
---

# Integrating with Industrial Process Manager

Integrate Operational Technology Incident Management with Industrial Process Manager to report incidents on equipment model entities.

Industrial Process Manager creates the ISA-95 Equipment Model data foundation that is required for the ServiceNow® Operational Technology solution. When integrated with Operational Technology Incident Management, you're enabled to view incident impact against production processes.

The ISA Equipment Model plugin \(sn\_isa\_model\) installed with Industrial Process Manager enables views for specified roles. For more information, see [ISA-95 equipment model](../../mftg-manufacturing-process-mgr/concept/isa-95-equipment-model.md).

When an OT incident is created from an OT device record, the following occurs:

-   The **OT device** field on the OT incident form is filled with the OT device value.
-   If the OT device has an associated equipment model entity, then the equipment model entity is added to **Equipment model entity** field on the OT incident form.
-   The **Site** field on the OT incident form is filled with the site of the OT device.

When an OT incident is created from an equipment model entity record, the following occurs:

-   The **Equipment model entity** field on the OT incident form is filled with the equipment model entity value.
-   The **Site** field on the OT incident form is filled with the site of the equipment model entity.

The **OT incident** related list on the equipment model entity record shows all OT incidents reported on that entity. The **Equipment model entity** field on the form can only have entities under the selected site.

**Parent Topic:**[Exploring Operational Technology Incident Management](exploring-operational-technology-incident-mgt.md)

