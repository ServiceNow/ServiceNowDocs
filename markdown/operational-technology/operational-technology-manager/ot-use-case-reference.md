---
title: Operational Technology and CSDM elements
description: Terms related to managing business applications with elements of CSDM.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Implementing the CSDM framework for Operational Technology, Configure, Operational Technology Manager, Operational Technology]
---

# Operational Technology and CSDM elements

Terms related to managing business applications with elements of CSDM.

<table id="table_jyf_xnv_xbc"><thead><tr><th>

Term

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Equipment model

</td><td>

The service records that describe how an industrial operation is organized to produce an output or product.

</td></tr><tr><td>

Production process

</td><td>

The relationships between equipment model entities and the various stages of the workflow from the raw material to finished goods.

</td></tr><tr><td>

Site

</td><td>

A parent equipment model entity record that has no parent. This is a special equipment model entity record because it is used to assign read or write level access to the OT devices assigned to the site.

</td></tr><tr><td>

OT device \(site assignment\)

</td><td>

The site assignment is needed for role-based security \(RBAC\) of OT devices. This is implemented as a choice list reference field on the OT Device Details \(cmdb\_ot\_entity\) table portion of the OT device record because an OT device can belong to only one site.

</td></tr><tr><td>

OT device \(automates::automated\)

</td><td>

The automates::automated by relationship describes how the OT device is related to the production process, which could include more than one equipment model entity.

</td></tr><tr><td>

Windows

</td><td>

In both OT and IT networks, the Windows server is represented in the cmdb\_ci\_win\_server server. Additionally, the Windows server in the OT network has a reference in the cmdb\_ci\_win\_server.cmdb\_ot\_entity field pointing to a record in the cmdb\_ot\_entity table that describes its function in OT and other OT characteristics like Purdue Level, site, and so on.

</td></tr></tbody>
</table>**Parent Topic:**[Implementing the CSDM framework for Operational Technology](../concept/ot-use-case-product-view.md)

