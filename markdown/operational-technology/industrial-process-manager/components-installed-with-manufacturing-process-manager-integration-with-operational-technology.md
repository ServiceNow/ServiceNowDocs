---
title: Automated mapping components installed when Industrial Process Manager and Operational Technology Manager are both installed
description: Several types of automated mapping components will be installed with activation of the Industrial Process Manager when Operational Technology Manager is also active, including tables, system properties, and scheduled flows.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# Automated mapping components installed when Industrial Process Manager and Operational Technology Manager are both installed

Several types of automated mapping components will be installed with activation of the Industrial Process Manager when Operational Technology Manager is also active, including tables, system properties, and scheduled flows.

These automated mapping components are installed with or available when Industrial Process Manager is installed with Operational Technology Manager.

<table id="table_gw2_tnw_mtb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT Subnet to Equipment Model Entity Mapping\[ot\_subnet\_mapping\]

</td><td>

Stores the mappings of OT subnet to equipment model entities.

</td></tr></tbody>
</table><table id="table_fkb_jdw_mtb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_otsm.map\_all\_ot\_assets.all\_discovery\_sources

</td><td>

Control mapping of OT devices for all discovery sources. Default value: **true**

</td></tr><tr><td>

sn\_otsm.map\_all\_ot\_assets.discovery\_sources

</td><td>

Map OT devices for specified discovery sources \(comma separated format\).

</td></tr><tr><td>

sn\_otsm.subnet\_mapping.auto\_assign\_ot\_control\_modules

</td><td>

Automatically assigns all OT control modules to equipment model entities based on the Owns::Owned by relationship. Default is Yes \(true\).

</td></tr><tr><td>

sn\_otsm.subnet\_mapping.location\_auto\_update

</td><td>

Override location of an OT device with subnet's location. If checked, the location of the subnet takes precedence over OT device's location when it's mapped with the subnet. Default is Yes.

</td></tr></tbody>
</table>|Application|Flow|
|-----------|----|
|Industrial Process Manager integration with Operational Technology Manager|OT device mapping flow|

**Parent Topic:**[Industrial Process Manager reference](../../mftg-manufacturing-process-mgr/reference/manufacturing-process-mgr-reference.md)

