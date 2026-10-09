---
title: Mapped ISA Entity field
description: The Mapped ISA Entity reference field for mapped OT devices identifies which Equipment Model entity the device is automated by. The mapped ISA entity is associated to a site.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/r-mapped-isa-entity-field.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 1
breadcrumb: [Equipment Model entity access control tables, Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# Mapped ISA Entity field

The Mapped ISA Entity reference field for mapped OT devices identifies which Equipment Model entity the device is automated by. The mapped ISA entity is associated to a site.

## Field definition

|Property|Value|
|--------|-----|
|Field name \(API\)|**mapped\_isa\_entity**|
|Field label|Mapped ISA Entity|
|Field type|Reference field|
|References table|\[**cmdb\_ci\_ot\_isa\_entity**\]|
|Location|Industrial workspace OT device lists only|
|Visibility on forms|Not visible on any form \(platform or workspace\)|
|Default edit mode|Read-only for most users|

## Field behavior

The Mapped ISA Entity field displays only ISA entities related to the OT device through Automates relationships in the same site. When a device has no mapped ISA entity, the field is empty in workspace lists.

## Field access control

|Access level|Roles required|Additional condition|
|------------|--------------|--------------------|
|Read|cmdb\_ot\_viewer and cmdb\_ot\_isa\_viewer|None|
|Write|cmdb\_ot\_editor and cmdb\_ot\_isa\_viewer|User must have full site-level access to the device site|
|Report view|cmdb\_ot\_isa\_viewer|Admins cannot override|

## Workspace list visibility

The Mapped ISA Entity field appears in the following Industrial workspace OT device lists:

-   All OT Devices list
-   OT Control System list
-   OT Field Devices list
-   OT Network Devices list
-   Unclassed OT Devices list

In each list, the field appears immediately after the **isa\_entity\_site** column.

The field does not appear in platform list views of the OT devices table.

**Note:** This information was developed with assistance from the AI tool, Claude.

-   **[Edit the Mapped ISA Entity on an OT device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/t-edit-mapped-isa-entity-ot-device.md)**  
The Mapped ISA Entity field identifies which ISA entity automates an OT device. Edit this field in Industrial workspace lists to establish the relationship between devices and their controlling entities.

**Parent Topic:**[Equipment Model entity access control tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/tables-equipment-model-access-control-tables.md)

