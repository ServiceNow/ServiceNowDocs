---
title: Roles in CDM
description: List of roles and permissions in CDM.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [DevOps Config roles, DevOps Config reference, DevOps Config, IT Service Management]
---

# Roles in CDM

List of roles and permissions in CDM.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## CDM roles

![CDM role hierarchy](../image/cdm-role-hierarchy.png)

<table id="table_cqv_djm_nnb"><thead><tr><th>

Role title \[name\]

</th><th>

Permissions

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

CDM Viewer \[sn\_cdm.cdm\_viewer\]

</td><td>

-   Read config data from any application that they have access to \(governed through user groups that are set by the **Maintained by** property\).
-   View the list and content of component libraries as well as the shared components contained within them.
-   View the list and content of changesets.
-   View the list and content of snapshots and validation results.
-   Export snapshots.
-   View exporters.
-   View policies and policy mappings.
-   View the Investigate page for a change request \(CHG\) on the Service Operations Workspace.

 **Note:** If the **Maintained by** group is set at the application level to view config data, then this user must be a member of the group.

</td><td>

-   \[sn\_pace.policy\_reader\]
-   \[itil\]
-   \[canvas\_user\]

</td></tr><tr><td>

Event Management user \[evt\_mgmt\_user\]

</td><td>

-   View the contents of the snapshots.
-   View the Investigate page for a change request \(CHG\) on the Service Operations Workspace.
-   View snapshots, nodes, and changesets, regardless of whether this user is a member of **Maintained by** groups set at the application level.

</td><td>

itil

</td></tr><tr><td>

CDM Editor \[sn\_cdm.cdm\_editor\]

</td><td>

-   Create/update/delete config data within components and collections, including variables, overrides, and includes.
-   Create and commit changesets.
-   Validate snapshots.
-   Publish and unpublish snapshots.
-   Create, update, and delete config data withing CDM applications.
-   Add and manage component libraries.
-   Add and delete shared components in a component library.

 **Note:** The cdm\_editor role doesn’t grant permission to create/update/delete an application and its deployables, or to change the **Enforce validation** setting on deployables.

If the **Maintained by** group is set at the application level to view config data, then this user must be a member of the group.

</td><td>

cdm\_viewer

</td></tr><tr><td>

CDM Exporter Editor \[sn\_cdm.cdm\_exporter\_editor\]

</td><td>

Create/update/delete exporters.

</td><td>

cdm\_viewer

</td></tr><tr><td>

CDM Policy Editor \[sn\_cdm.cdm\_policy\_editor\]

</td><td>

-   Create/update/delete policies.
-   Map policies to deployables.

</td><td>

-   cdm\_viewer
-   \[sn\_pace.admin\]

</td></tr><tr><td>

CDM Secrets \[sn\_cdm.cdm\_secrets\]

</td><td>

-   Read and export encrypted data \(when granted to a user with the cdm\_viewer role\).
-   Permanently encrypt / decrypt data \(when granted to a user with the cdm\_editor role\).
-   Edit encrypted data \(when granted to a user with the cdm\_editor role\).

 **Note:** The cdm\_secrets role is effective only with the cdm\_viewer, cdm\_editor, or cdm\_admin role.

</td><td>

None

</td></tr><tr><td>

Application Service Admin \[sn\_cdm.app\_service\_admin\]

</td><td>

Enables the CDM Admin to create an application service.

</td><td>

None

</td></tr><tr><td>

CDM Admin \[sn\_cdm.cdm\_admin\]

</td><td>

-   Create/update/delete applications.
-   Create/update/delete deployables.
-   Create/update/delete config data.
-   Change settings on deployables to enforce snapshot validation.

</td><td>

-   cdm\_editor
-   cdm\_exporter\_editor
-   cdm\_policy\_editor
-   app\_service\_admin
-   Model\_manager \(for create/update/delete of application model\)
-   \[itil\] \(for create/update/delete of SDLC components\)
-   \[itil admin\]

</td></tr><tr><td>

CDM All App Access \[sn\_cdm.cdm\_all\_app\_access\]

</td><td>

**Note:** The cdm\_all\_app\_access role is effective only with the cdm\_admin, cdm\_editor, or cdm\_viewer roles.

 -   Users with the cdm\_all\_app\_access and cdm\_admin role can update or delete an application or shared component library regardless of whether they’re a member of the user groups that maintain the application \(**Maintained by** field\) or library \(**Authoring groups** field\).
-   Users with the cdm\_all\_app\_access and cdm\_editor role can edit an application or shared component library regardless of being a member of any of the user groups that maintain the application or library.
-   Users with the cdm\_all\_app\_access and cdm\_viewer role can view an application regardless of being a member of any of the user groups that maintain the application.

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[DevOps Config roles](../../devops-config/reference/devops-config-roles.md)

