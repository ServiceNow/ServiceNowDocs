---
title: ISA Access by Group
description: ISA Access by Group lets you assign view or edit permissions to user groups for specific equipment model entities. Use this method when all members of a team or department need the same access level to particular entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/c-isa-access-by-group.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Equipment Model entity access control tables, Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# ISA Access by Group

ISA Access by Group lets you assign view or edit permissions to user groups for specific equipment model entities. Use this method when all members of a team or department need the same access level to particular entities.

## How group-based access works

When you assign access to a group, all members of that group receive the permission level you specify: view or edit. View access lets group members see the entity in read-only mode. Edit access lets group members view and modify the entity.

When you add or remove users from a group, their access to equipment model entities updates automatically based on the group's permissions.

## When to use group-based access

Use group-based access when multiple users need the same permissions to particular entities. This approach is most effective when:

-   Multiple users in a team or department need identical access
-   You want to manage access for large numbers of users efficiently
-   User membership in groups changes over time
-   You want permissions to apply automatically to new group members

For access requirements unique to individual users, user-based access is more appropriate.

## Who manages group-based access

Only users with the `cmdb_ot_isa_admin` role can create, read, update, or delete group-based access records. The ISA Access - By Group navigator module provides a dedicated list view for managing group access assignments.

**Note:** This information was developed with assistance from the AI tool, Claude.

-   **[Assign ISA Access edit permissions by group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/assign-isa-access-edit-permissions-by-group.md)**  
Grant groups edit access to specific equipment model entities for ISA Access.

**Parent Topic:**[Equipment Model entity access control tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/tables-equipment-model-access-control-tables.md)

