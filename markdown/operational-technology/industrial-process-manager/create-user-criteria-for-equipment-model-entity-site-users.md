---
title: Assign or remove equipment model site access for non-administrators
description: Assign or remove equipment model site access for non-administrators. You can create the user criteria to determine whether certain users can access the equipment model entities for specific sites.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Industrial Process Manager, Operational Technology]
---

# Assign or remove equipment model site access for non-administrators

Assign or remove equipment model site access for non-administrators. You can create the user criteria to determine whether certain users can access the equipment model entities for specific sites.

## Before you begin

Role required: admin

## About this task

Use the user criteria to determine whether certain users can read or edit equipment model entities for specific sites. After you create a user criteria record, you can assign it to a site to control who can read and edit the equipment model entities. You can further assign the OT roles to users or groups to enable them access to OT devices that are assigned to those same sites. For more information, see [Assign Operational Technology Manager roles](../../mftg-manufacturing-oper-tech-mgr/task/assign-operational-technology-manager-roles.md).

**Note:** For those users that are upgrading to version 1.0.12, their site user access is migrated to user criteria and groups. For more information, see [Migrating site user access to user criteria and groups](migrating-site-user-access-to-user-criteria-and-groups.md).

## Procedure

1.  Navigate to **All** &gt; **Knowledge Management** &gt; **Administration** &gt; **User Criteria**

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values, see [User criteria form](../reference/user-criteria-form-ipm.md).


## What to do next

After you create the user criteria, you can assign it to a site. For more information about assigning the Can Edit access to a site, see [Assign the user criteria for Can Edit access to a site](assign-user-criteria-for-can-edit-access.md). For more information about adding the Can Read access to a site, see [Assign the user criteria for Can Read access to a site](assign-user-criteria-for-can-read-access.md).

-   **[Assign the user criteria for Can Read access to a site](assign-user-criteria-for-can-read-access.md)**  
Assign the user criteria to a site to define which users can read or view the equipment model entities that belong to the selected site.
-   **[Assign the user criteria for Can Edit access to a site](assign-user-criteria-for-can-edit-access.md)**  
Assign the user criteria to a site to define which users can edit the equipment model entities that belong to the selected site.

**Parent Topic:**[Configuring the Industrial Process Manager](../concept/configuring-manufacturing-process-mgr.md)

