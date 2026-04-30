---
title: Permissions management for Cloud Governance roles
description: Permissions are user group-level access rights to features in the Cloud Provisioning and Governance application and to specific records in the instance, such as blueprints or cloud accounts.
locale: en-US
release: yokohama
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Permissions management for Cloud Governance roles

Permissions are user group-level access rights to features in the Cloud Provisioning and Governance application and to specific records in the instance, such as blueprints or cloud accounts.

You can refine the actions that are allowed or prohibited for users based on user group. By default, each role includes access rights, but not all users with the same role can see or edit each others records. For example, by default users with the cloud\_designer role have full read and write access to their own blueprints, but they do not have read or write access to blueprints created by other cloud designers. If you want them to have access, you must put the users into a group that has the cloud\_designer role, then give that group read and write access to particular blueprints.

## Permission types

-   **Access \[Read\]**

    Users can see the record, but not edit or delete.

-   **Manage \[Create &amp; Update\]**

    Users can see the record and create and update new records in the same table, but cannot delete any records.

-   **Delete**

    Users can delete specified records or all records in the table.

-   **Execute**

    Users can execute an action on records in the table.

-   **All**

    Users have permissions on all records in the table.


## Permissions suggestions

Consider granting these permissions in your organization:

<table id="table_kjf_bqr_1z"><thead><tr><th>

Suggested group and role

</th><th>

Type of users in the group

</th><th>

Suggest permissions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog user groupCloud user `[sn_cmp.cloud_service_user]`

</td><td>

Users who order similar items from the catalog in the Cloud User Portal.

</td><td>

Access \[read\] or Execute

</td><td>

Catalog items, even after they are published, cannot be seen by users in the Cloud User Portal until you grant a user group to which that user belongs read access to the items. Grant Access and Execute permissions to cloud users on the Blueprint Catalog Item table and the Cloud Account table.

</td></tr><tr><td>

Blueprint designersService Designer \[sn.cmp.cloud\_service\_designer\]

</td><td>

Users who design blueprints.

</td><td>

Manage \[Create and update\]

</td><td>

Blueprint designers cannot see or edit other blueprints or catalog items by default. To collaborate or reuse existing blueprints and catalog items, blueprint designers need access to each others' blueprints through the Manage permission.

</td></tr><tr><td>

Cloud admins Cloud administrator `[sn_cmp.cloud_admin]`

</td><td>

Users who create and manage cloud accounts.

</td><td>

Manage \[Create and update\]

</td><td>

Cloud admins must map templates to appropriate resource profiles. To collaborate or reuse existing resource profiles and templates.

</td></tr></tbody>
</table>-   **[Assign a cloud permission](../task/create-permissions.md)**  
Assign a permission to refine the actions that are allowed or prohibited for users based on the user group they belong to.

**Parent Topic:**[Cloud Admin Portal](cloud-admin-portal.md)

