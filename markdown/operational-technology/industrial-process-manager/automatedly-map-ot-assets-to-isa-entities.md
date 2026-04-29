---
title: Map an individual OT device to an equipment model entity
description: Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automatically map all OT devices, Automated Mapping Across Zone-based IP Network Groups, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Map an individual OT device to an equipment model entity

Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

Role required: sn\_ot\_amazing\_write and cmdb\_ot\_viewer

## Procedure

1.  Navigate to the Industrial Workspace.

2.  Open the Industrial Workspace list view.

3.  Under the **Operational Technology \(OT\)** list module, select one of the available lists.

4.  Select the OT device that you want to map.

5.  In the OT device record, select the **More actions** ![](../../mftg-manufacturing-ot-knowledge/image/more-actions.png) icon.

6.  Select the **Map OT device** UI action.


## Result

If there is an active OT subnet that matches the IP address and site of the selected device, the device is mapped.

**Parent Topic:**[Automatically map all OT devices to an equipment model entity](automatedly-map-all-ot-assets.md)

