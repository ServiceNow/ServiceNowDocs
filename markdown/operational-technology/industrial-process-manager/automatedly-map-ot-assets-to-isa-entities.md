---
title: Map an individual OT device to an equipment model entity
description: Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-01-22"
reading_time_minutes: 1
breadcrumb: [Automated mapping of OT devices to the Equipment Model, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Map an individual OT device to an equipment model entity

Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.

## Before you begin

The following plugins must be installed:

-   [Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/operational-technology-manager.md)
-   [Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/industrial-process-manager-overview.md)

Role required: sn\_ot\_amazing\_write and cmdb\_ot\_viewer

## Procedure

1.  Navigate to **All** &gt; **Operational Technology \(OT\)** &gt; **All OT Devices**.

2.  In the **OT device** column, select the OT device that you want to map.

    **Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.

3.  In the Related Links section, select **Map OT device**.

    ![OT devices form related links section- platform UI](../image/map-ot-device.png)


## Result

If there is an active OT subnet that matches the IP address and site of the selected device, the device is mapped.

**Parent Topic:**[Automated mapping of OT devices to the Equipment Model](automate-mappings-between-ot-assets-and-equipment-model-entity.md)

