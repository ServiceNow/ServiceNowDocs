---
title: Configure the migration of a custom ITSM table from ITSM Agent Workspace to Service Operations Workspace for ITSM
description: If you have a custom ITSM table that must be migrated, you must enable the migration of the associated list categories and modules, list actions, related list actions, and New record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the migration of a custom ITSM table from ITSM Agent Workspace to Service Operations Workspace for ITSM

If you have a custom ITSM table that must be migrated, you must enable the migration of the associated list categories and modules, list actions, related list actions, and New record menu items from ITSM Agent Workspace to Service Operations Workspace for ITSM.

## Before you begin

Role required: admin

## Procedure

1.  From the **All** menu, in the navigation filter, enter **sys\_properties.list**.

2.  Search for the **sn\_sow\_migration.itsm\_aw\_migration\_tables** system property.

3.  In the **Value** field, add the custom ITSM table's id to the comma-separated list.

    By default, the **Value** field contains all ITSM tables whose list categories and modules, list actions, related list actions, and New record menu items should be migrated from ITSM Agent Workspace to Service Operations Workspace for ITSM.

4.  Select **Update**.


**Parent Topic:**[Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../concept/migration-from-itsm-aw-sow.md)

