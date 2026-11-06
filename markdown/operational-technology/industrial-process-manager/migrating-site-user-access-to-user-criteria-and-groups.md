---
title: Migrating site user access to user criteria and groups
description: When you upgrade to version 1.0.12 of the ISA Equipment Model, the migration from site user access to user criteria and groups begins automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/operational-technology/industrial-process-manager/migrating-site-user-access-to-user-criteria-and-groups.html
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# Migrating site user access to user criteria and groups

When you upgrade to version 1.0.12 of the ISA Equipment Model, the migration from site user access to user criteria and groups begins automatically.

**Note:** Current users can decide whether to migrate to other available versions of the ISA Equipment Model. However, user criteria configurations aren't available with the ISA Equipment Model version 4.2.0. For more information, see .

## Upgrading to ISA Equipment Model version 4.2.0

The following changes occur when you upgrade to version 4.2.0 of the ISA Equipment Model.

-   Granular access for Equipment Model Entities replaces the user criteria access.For more information see, .
-   With version 4.2.0 the existing query business rules on the OT Entity \(cmdb\_ot\_isa\_entity\) table are turned off.
-   The OT administrator sets users and groups permission to write, or edit, a site's equipment model entities.
-   Access rules are set by three tables:

    -   Equipment Model Entity Access \(isa\_entity\_access\)
    -   Equipment Model Entity User Access \(isa\_entity\_user\_access\)
    -   Equipment Model Entity Group Access \(isa\_entity\_group\_access\)
    For more information see, .

-   The access control tables enforce two validation rules:

    -   A site is required. You must select a site before you can assign access to an entity.
    -   The **Equipment Model Entity** field is hidden until you select a site. After you select a site, the entity field displays only entities that belong to that site.
-   There are two options for creating or editing users and groups accesses to a new equipment model entity. Navigate to **All &gt; Equipment Model - ISA** then select from these options:
    -   ISA Access - by User: for more information see, .
    -   ISA Access - by Group: for more information see, .
-   The Primary Equipment model field has been added to workspace OT device lists. The **Primary Equipment Model** \(mapped\_isa\_entity\) field displays which equipment model entity has an Automates relationship with Operational Technology \(OT\) device. This field is associated with a specific site. For more information see, .

For more information, see 

## Upgrading to ISA Equipment Model version 1.0.12

The following changes occur when you upgrade to version 1.0.12 of the ISA Equipment Model.

-   Improved site level access control that uses user criteria to define read or write level user access to equipment model entity sites. Assign the OT viewer \(cmdb\_ot\_viewer\) or OT Editor \(cmdb\_ot\_editor\) role to have view or edit access to OT devices in the assigned sites.
-   When you upgrade to version 1.0.12 of ISA Equipment Model, existing site user records are migrated to an improved access control model using user criteria to preserve the same access permissions. For each site with ISA Entity Site User records, the following changes occur.
    -   For users with viewer access:
        -   A new user criteria record is created and named **Read User Criteria for &lt;site name&gt; Site \[System Generated\]**
        -   A new user group with all site users from this site is created and named **Read Group for &lt;site name&gt; Site \[System Generated\]**
        -   A new record in the new Equipment Model Entity View Access table \(isa\_entity\_m2m\_user\_criteria\_can\_view\) is created with the new user criteria and user group.
    -   For users with editor access:
        -   A new user criteria record is created and named **Edit User Criteria for &lt;site name&gt; Site \[System Generated\]**
        -   A new user group with all site users from this site is created and named **Edit Group for &lt;site name&gt; Site \[System Generated\]**
        -   A new record in the new Equipment Model Entity Edit Access table \(isa\_entity\_m2m\_user\_criteria\_can\_edit\) is created with the new user criteria and user group.
-   The Site User application menu and Site Users related list on the Equipment Model Entity record for a site is removed.
-   All site user \(isa\_entity\_site\_user\) records are set to inactive.
-   The **Site User – Can Read** and **Site User – Can Edit** application menu items are added to the ServiceNow AI Platform.
-   The **Can Read Equipment Models** and **Can Edit Equipment Models** related lists are added to the Equipment Model Entity record for a site.

**Parent Topic:**[Industrial Process Manager reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/industrial-process-manager/manufacturing-process-mgr-reference.md)

