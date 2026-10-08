---
title: Edit the Mapped ISA Entity on an OT device
description: The Mapped ISA Entity field identifies which ISA entity automates an OT device. Edit this field in Industrial workspace lists to establish the relationship between devices and their controlling entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/t-edit-mapped-isa-entity-ot-device.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [mapped ISA entity, OT device, ISA entity]
breadcrumb: [Mapped ISA Entity field, Equipment Model entity access control tables, Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# Edit the Mapped ISA Entity on an OT device

The Mapped ISA Entity field identifies which ISA entity automates an OT device. Edit this field in Industrial workspace lists to establish the relationship between devices and their controlling entities.

## Before you begin

Role required: `cmdb_ot_editor` and `cmdb_ot_isa_viewer`

You must have full site-level access to the OT device's site to edit this field.

## About this task

Mapping OT devices to ISA entities establishes the relationship between physical devices and the entities that control them. This mapping enables better asset tracking and operational visibility.

Edit the Mapped ISA Entity field in Industrial workspace OT device lists. This field is read-only in platform views and on forms. The reference picker displays only ISA entities related to the OT device via Automates relationships within the same site.

## Procedure

1.  Navigate to Industrial Workspace.

2.  Open an OT device list view.

    Available workspace lists:

    -   All OT Devices
    -   OT Control System
    -   OT Field Devices
    -   OT Network Devices
    -   Unclassed OT Devices
3.  In the Mapped ISA Entity column, select the field for the OT device you want to edit.

    The Mapped ISA Entity column appears after the Site column. The reference picker displays only ISA entities related to this device via Automates relationships in the same site.

4.  Select an ISA entity from the picker.

    If no entities appear, verify that ISA entities are related to this OT device via Automates relationships in the same site. To clear the field, select the empty option.

5.  Press **Enter** or select outside the field to save the change.


## Result

The OT device record now displays the selected ISA entity in the Mapped ISA Entity field. Users with access to that ISA entity can view this mapping in workspace lists.

**Note:** This information was developed with assistance from the AI tool, Claude.

**Parent Topic:**[Mapped ISA Entity field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/r-mapped-isa-entity-field.md)

