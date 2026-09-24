---
title: Migrating site user access to user criteria and groups
description: When you upgrade to version 1.0.12 of the ISA Equipment Model, the migration from site user access to user criteria and groups begins automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/migrating-site-user-access-to-user-criteria-and-groups.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference, Industrial Process Manager, Operational Technology]
---

# Migrating site user access to user criteria and groups

When you upgrade to version 1.0.12 of the ISA Equipment Model, the migration from site user access to user criteria and groups begins automatically.

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

**Parent Topic:**[Industrial Process Manager reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/manufacturing-process-mgr-reference.md)

