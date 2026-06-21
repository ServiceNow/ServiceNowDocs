---
title: Map an individual OT device to an equipment model entity
description: Perform on-demand mapping of an OT device to the ISA equipment model entity for the sites that you have access to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/operational-technology/industrial-process-manager/automatedly-map-ot-assets-to-isa-entities.html
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

-   [Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/operational-technology-manager/operational-technology-manager.md)
-   [Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/industrial-process-manager/industrial-process-manager-overview.md)

Role required: sn\_ot\_amazing\_write and cmdb\_ot\_viewer

## Procedure

1.  Navigate to **All** &gt; **Operational Technology \(OT\)** &gt; **All OT Devices**.

2.  In the **OT device** column, select the OT device that you want to map.

    **Note:** Subnet mapping also supports Discovery created configuration items \(CIs\) for ISA equipment models.

3.  In the Related Links section, select **Map OT device**.

    \[Omitted image "map-ot-device.png"\] Alt text: OT devices form related links section- platform UI


## Result

If there is an active OT subnet that matches the IP address and site of the selected device, the device is mapped.

**Parent Topic:**[Automated mapping of OT devices to the Equipment Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/operational-technology/industrial-process-manager/automate-mappings-between-ot-assets-and-equipment-model-entity.md)

