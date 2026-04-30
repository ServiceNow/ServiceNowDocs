---
title: System properties used by the OT subnet mapping feature
description: An Amazing Admin can view and configure the system properties that support the OT subnet mapping feature.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automated mapping of OT devices to the Equipment Model, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# System properties used by the OT subnet mapping feature

An Amazing Admin can view and configure the system properties that support the OT subnet mapping feature.

Users with the Amazing Admin role can access OT subnet mapping property settings by navigating to **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **OT Subnet Mapping Properties**.

<table id="table_orj_4bw_mtb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_otsm.map\_all\_ot\_assets.all\_discovery\_sources**

</td><td>

Control mapping of OT devices for all discovery sources. Map OT devices for all discovery sources. If checked, this will override the specific discovery sources below. Default is Yes \(true\).Default value: **true**

</td></tr><tr><td>

**sn\_otsm.map\_all\_ot\_assets.discovery\_sources**

</td><td>

Map OT devices for specified discovery sources \(comma separated format\). Only applicable if "Map OT devices for all discovery sources" above is unchecked.

</td></tr><tr><td>

**sn\_otsm.subnet\_mapping.auto\_assign\_ot\_control\_modules**

</td><td>

Automatically assigns all OT control modules to equipment model entities based on the Owns::Owned by relationship. Default is Yes \(true\).

</td></tr><tr><td>

**sn\_otsm.subnet\_mapping.location\_auto\_update**

</td><td>

Override location of an OT device with subnet's location. If checked, the location of the subnet takes precedence over OT device's location when it's mapped with the subnet. Default is Yes.

</td></tr></tbody>
</table>**Parent Topic:**[Automated mapping of OT devices to the Equipment Model](../task/automate-mappings-between-ot-assets-and-equipment-model-entity.md)

