---
title: Roles to class mapping for configurable workspaces
description: In configurable workspaces, roles can access classes in addition to the default seeded classes for each specific role.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configurable workspaces, Explore, Enterprise Asset Management, IT Asset Management]
---

# Roles to class mapping for configurable workspaces

In configurable workspaces, roles can access classes in addition to the default seeded classes for each specific role.

New roles are assigned to each configurable workspace. New roles are based on the following applications and their designated workspace.

<table id="table_p4c_jy5_g2c"><thead><tr><th>

Application

</th><th>

Designated workspace

</th><th>

Roles

</th></tr></thead><tbody><tr><td>

Enterprise Asset Management for Healthcare

</td><td>

Medical Asset Workspace

</td><td>

-   sn\_eamhc.medical\_asset\_manager
-   sn\_eamhc.medical\_asset\_technician

</td></tr><tr><td>

Enterprise Asset Management for Facilities

</td><td>

Facility Asset Workspace

</td><td>

-   sn\_eamfam.facility\_asset\_manager
-   sn\_eamfam.facility\_asset\_technician

</td></tr><tr><td>

Operational Technology \(OT\) Asset Management

</td><td>

OT Asset Workspace

</td><td>

-   sn\_otam.ot\_asset\_manage
-   sn\_otam.ot\_asset\_technician

</td></tr></tbody>
</table>A default configuration of classes is seeded for each role that maps to its corresponding model category.

The following mapping is a default configuration that is seeded for the Medical, the Facilities, and the OT technician roles.

**Note:** The manager roles include the respective technician roles for Enterprise Asset Management for Healthcare, Enterprise Asset Management for Facilities, and Operational Technology \(OT\) Asset Management applications.

<table id="table_ojr_zz5_g2c"><thead><tr><th>

Enterprise roles

</th><th>

Seeded model categories

</th><th>

Seeded enterprise classes for roles

</th></tr></thead><tbody><tr><td>

Medical techniciansn\_eamhc.medical\_asset\_technician

</td><td>

Medical

</td><td>

sn\_ent\_medical\_model

 sn\_ent\_medical\_device\_model

 sn\_ent\_medical\_asset

</td></tr><tr><td>

Facility technician sn\_eamfam.facility\_asset\_technician

</td><td>

Facilities

</td><td>

sn\_ent\_facility\_model

 sn\_ent\_facility\_asset

</td></tr><tr><td>

OT technician sn\_otam.ot\_asset\_technician

</td><td>

Industrial, Hardware

</td><td>

sn\_ent\_industrial\_asset

 sn\_ent\_industrial\_model, alm\_hardware

 cmdb\_hardware\_product\_model

 sn\_ent\_firmware\_model

 sn\_ent\_discov\_firmware\_model

</td></tr></tbody>
</table>The Roles to classes access table shows the various classes that each role has access to by default. For example, the facility technician role has access to the facility classes: sn\_ent\_facility\_model and sn\_ent\_facility\_asset. When a facility technician logs in to the Facility Asset Workspace, they will automatically get access to only the models and assets related to the Facilities model category.

Based on the mapping, roles get access to the respective asset and model classes. The roles further get access to the workflow tasks and work orders related to those classes. Additionally, you can view information only pertaining to your classes on all dashboards in the workspace. For example, a medical asset manager role can initiate disposal orders only for medical assets because of access configuration. Similarly, a facilities technician role can only work on disposal tasks created for facility assets.

The Enterprise admin \(sn\_eam.enterprise\_admin\) role can modify the default configuration to add more classes to a role. So, the roles for the Medical Asset Workspace, the Facilities Asset Workspace, and the OT Workspace can be configured to access additional classes from different model categories. For example, the Medical technician role can get access to the Facilities classes. Similarly, the Facilities technician role can get access to the Transportation classes. For more details on adding additional classes to a role, see [Map enterprise roles to enterprise classes](../task/map-ent-roles-ent-classes.md).

**Note:** A soft filter exists in configurable workspaces that shows information relevant to a particular workspace. You can remove that filter to display assets and models for all classes but only read access is available for the other classes.

