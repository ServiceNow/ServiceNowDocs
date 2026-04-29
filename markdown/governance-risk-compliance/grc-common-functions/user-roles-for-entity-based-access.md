---
title: User roles for Entity Based Access
description: Users with specific user roles have access to read or update the Entity Based Access configuration or the bulk access update configuration.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# User roles for Entity Based Access

Users with specific user roles have access to read or update the Entity Based Access configuration or the bulk access update configuration.

<table id="table_gtg_1yr_z2c"><thead><tr><th>

User role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_grc\_ent\_access.admin

</td><td>

Role that is part of the Entity Based Access application.Assign this role to users who need to enable or disable the **Entity based access on record types related to entity** property and configure Entity Based Access.

</td></tr><tr><td>

sn\_grc\_ent\_access.reader

</td><td>

Role that is part of the Entity Based Access application.Assign this role to users who require read access to the Entity Based Access configuration.

</td></tr><tr><td>

sn\_grc\_ent\_access.bulk\_access\_config\_admin

</td><td>

Role that is part of the Entity Based Access application.Assign this role to users who need write and update access to the bulk access update configuration.

</td></tr><tr><td>

sn\_grc\_ent\_access.bulk\_access\_config\_reader

</td><td>

Role that is part of the Entity Based Access application.Assign this role to users who require read access to the bulk access update configuration.

</td></tr><tr><td>

sn\_grc.eba\_restriction\_field\_editor

</td><td>

Role that is part of the Entity Based Access application.Assign this role to users who require write and update access to the **Entity based access restriction** field on issue records.

</td></tr></tbody>
</table>|User role|Description|
|---------|-----------|
|sn\_grc\_reg\_change.user|Regulatory change management user. This role is excluded from the Entity Based Access configuration.|
|sn\_ai\_governance.ai\_steward|The AI steward role. This role is excluded from the Entity Based Access configuration.|

**Parent Topic:**[Entity Based Access](../concept/entity-based-access.md)

