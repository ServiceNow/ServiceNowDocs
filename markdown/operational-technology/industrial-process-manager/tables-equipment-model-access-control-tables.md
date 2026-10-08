---
title: Equipment Model entity access control tables
description: Equipment Model entity access control tables store permissions that determine which users or groups can view or modify equipment model entities. By default, users and groups can view \(read\) equipment model entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/tables-equipment-model-access-control-tables.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Equipment Model entity access control, ISA-95 access control, OT entity permissions]
breadcrumb: [Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# Equipment Model entity access control tables

Equipment Model entity access control tables store permissions that determine which users or groups can view or modify equipment model entities. By default, users and groups can view \(read\) equipment model entities.

## Base and extension tables

The access control tables provide the data model foundation for fine-grained access control over Operational Technology \(OT\) equipment model entities. These tables enable ISA administrators to assign access permissions based on individual users or user groups.

The access control data model consists of a base table and two extension tables, all within the ISA Equipment Model \(`sn_isa_model`\) scope:

-   Equipment Model Entity Access \[`isa_entity_access`\]: the base table that stores the entity, the entity site, and whether the grant allows editing.
-   Equipment Model Entity User Access \[`isa_entity_user_access`\]: extends the base table to assign access to individual users.
-   Equipment Model Entity Group Access \[`isa_entity_group_access`\]: extends the base table to assign access to user groups.

The base table contains three key fields: the entity reference, the entity site reference \(limited to top-level entities\), and a Boolean field that controls whether edit access is permitted. Each extension table adds a specific field to support its access assignment method.

## Access scope and granularity

Entity-level access control is more granular than site-level access control. Site-level access controls apply to an entire equipment model entity site, while entity-level access controls apply to individual entities within a site. This granularity enables you to assign different permission levels to different equipment model entities within the same site hierarchy.

## Access assignment methods

The two extension tables support different approaches to assigning access.

|Access level|Description|
|------------|-----------|
|User-based access|Assigns permissions to individual user accounts. Use this method when specific users need access to particular entities.|
|Group-based access|Assigns permissions to user groups. Use this method to grant access to all members of a team or department.|

For more information on ISA access levels, see [ISA Access by User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/c-isa-access-by-user.md) or [ISA Access by Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/c-isa-access-by-group.md).

## Permission levels

Access records provide two permission levels.

|Permissions|Description|
|-----------|-----------|
|Read-only access|Users can view the entity but cannot modify it. This is the default permission level.|
|Edit access|Users can view and modify the entity. This permission is granted when **Active** is set to true.|

## Validation rules

The access control tables enforce two key validation rules:

-   The entity site field is required. Select a site before you can assign access to an entity.
-   The entity field is hidden until you select a site. After you select a site, the entity field displays only entities that belong to that site.

## Connection between OT devices and Equipment Model entities

OT devices and Equipment Model entities represent different aspects of your operational technology environment:

-   **OT devices**: The actual physical or virtualized devices discovered in your network \(controllers, sensors, gateways, and similar equipment\).
-   **Equipment Model entities**: The logical hierarchy that represents how equipment is organized and relates to production processes. Equipment Model entities follow ISA-95 standards.

The **Mapped ISA Entity** field on OT devices links physical devices to logical entities. This mapping enables access control to apply consistently across both representations of your OT environment.

When you grant a user access to an Equipment Model entity, that user also gains access to OT devices mapped to that entity \(subject to site-level permissions\).

For more information on the Mapped ISA entity, see [Mapped ISA Entity field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/r-mapped-isa-entity-field.md).

## Legacy query business rule

The existing query business rule on the OT Entity \[`cmdb_ot_entity`\] table is turned off. Row-level access is now handled entirely by the read ACL rules.

**Note:** This information was developed with assistance from the AI tool, Claude.

-   **[ISA Access by User](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/c-isa-access-by-user.md)**  
ISA Access by User lets you assign view or edit permissions to individual users for specific equipment model entities. Use this method when particular users need access to equipment model entities.
-   **[ISA Access by Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/c-isa-access-by-group.md)**  
ISA Access by Group lets you assign view or edit permissions to user groups for specific equipment model entities. Use this method when all members of a team or department need the same access level to particular entities.
-   **[Mapped ISA Entity field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/r-mapped-isa-entity-field.md)**  
The Mapped ISA Entity reference field for mapped OT devices identifies which Equipment Model entity the device is automated by. The mapped ISA entity is associated to a site.

**Parent Topic:**[Configure the Industrial Process Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/configuring-manufacturing-process-mgr.md)

