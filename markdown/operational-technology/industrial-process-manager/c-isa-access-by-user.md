---
title: ISA Access by User
description: ISA Access by User lets you assign view or edit permissions to individual users for specific equipment model entities. Use this method when particular users need access to equipment model entities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/c-isa-access-by-user.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Equipment Model entity access control tables, Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# ISA Access by User

ISA Access by User lets you assign view or edit permissions to individual users for specific equipment model entities. Use this method when particular users need access to equipment model entities.

## How user-based access works

When you assign access to a user, you specify which equipment model entity they can access and what permission level they have: view or edit. View access lets the user see the entity in read-only mode. Edit access lets the user view and modify the entity.

Each user access record is independent. You can grant one user view access to an entity while granting another user edit access to the same entity.

## When to use user-based access

Use user-based access when granting permissions to specific individuals. This approach is most effective when:

-   A small number of users need access to particular entities
-   Users have different permission levels for the same entity
-   Access requirements change frequently for individual users

For larger groups with the same permissions, group-based access is more efficient.

## Who manages user-based access

Only users with the `cmdb_ot_isa_admin` role can create, read, update, or delete user-based access records. The ISA Access - By User navigator module provides a dedicated list view for managing user access assignments.

**Note:** This information was developed with assistance from the AI tool, Claude.

-   **[Assign ISA Access edit permissions by user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/assign-isa-edit-permissions-by-user.md)**  
Configure access permissions to grant users edit access to Equipment Model entities.

**Parent Topic:**[Equipment Model entity access control tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/tables-equipment-model-access-control-tables.md)

