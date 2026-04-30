---
title: Create an asset group in Enterprise Asset Management
description: Create asset groups to create a logical group of entities that includes assets, locations, and users.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-05-01"
reading_time_minutes: 3
breadcrumb: [Create and manage enterprise assets, Managing enterprise assets and models, Enterprise Asset Management, IT Asset Management]
---

# Create an asset group in Enterprise Asset Management

Create asset groups to create a logical group of entities that includes assets, locations, and users.

## Before you begin

Role required:

-   sn\_eam.enterprise\_admin
-   sn\_eam.enterprise\_asset\_manager
-   sn\_eamfam.facility\_asset\_manager
-   sn\_eamhc.medical\_asset\_manager
-   sn\_otam.ot\_asset\_manager

## About this task

Asset groups can be used and created in the Enterprise Asset Workspace, Facility Asset Workspace, Medical Asset Workspace, and the Operational Technology \(OT\) Asset Workspace. This task specifically describes how to create an asset group in the Enterprise Asset Workspace.

After you create an asset group, you can create subgroups and add assets to the subgroups.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Asset Workspace** &gt; **Enterprise asset estate** &gt; **Asset groups**.

    The Asset groups tab contains two subtabs:

    -   Asset groups: all the asset groups in your organization.
    -   Sites: equipment model entities that are picked up from the Equipment model \[cmdb\_ci\_ot\_isa\_entity\] table. The Equipment model table is a descendant of the Application Service CI \[cmdb\_ci\_service\_auto\] table.
    The Asset groups subtab is further classified into the following sites:

    -   Unassigned sites: sites not assigned to any asset group.
    -   Assigned sites: sites assigned to an asset group.
2.  Select **New** to open the Create New Asset group page.

3.  On the form, fill in the fields.

<table id="table_ik3_wyx_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

 

</td></tr><tr><td>

Service instance

</td><td>

Reference that you can assign to the asset group. This creates a bridge between the CI and the assets.If you assign a reference to the asset group, then the asset group is bound by the reference to the selected Service instance.

</td></tr><tr><td>

Description

</td><td>

Brief description of the asset group.

</td></tr><tr><td>

Parent

</td><td>

Parent group of the asset group.

</td></tr><tr><td>

Location

</td><td>

Specific geographical location of the asset group.

</td></tr><tr><td>

Site

</td><td>

Equipment model entities that are picked up from the Equipment model \[cmdb\_ci\_ot\_isa\_entity\] table.

</td></tr><tr><td>

State

</td><td>

The current state of the asset group. By default, a newly created asset group is in the **Build** state.

</td></tr><tr><td>

Substsate

</td><td>

The substate of the asset group.

</td></tr><tr><td>

Support group

</td><td>

The group to contact if you encounter any issues with the asset group.

</td></tr><tr><td>

Supported by

</td><td>

The person who can be contacted within the support group for any issues that you may encounter with the asset group.

</td></tr><tr><td>

Department

</td><td>

Department to which the asset group belongs.

</td></tr><tr><td>

Company

</td><td>

Company or organization to which the asset group belongs.

</td></tr><tr><td>

Owned by

</td><td>

Person who has financial ownership of the asset group. This can be different from the person in the **Managed by** field.

</td></tr><tr><td>

Managed by

</td><td>

Person who maintains the asset group. This can be different from the person in the **Owned by** field.

</td></tr><tr><td>

Assigned to

</td><td>

Person using or primarily responsible for this asset group. This field is visible when the asset state is **In Use**.

</td></tr><tr><td>

Assigned

</td><td>

Date on which the asset group was assigned to a user.

</td></tr><tr><td>

Installed

</td><td>

Date on which the asset group was assigned to the person mentioned in the **Assigned to** field.

</td></tr><tr><td>

Retired date

</td><td>

The date this asset group is retired.

</td></tr><tr><td>

Comments

</td><td>

Any comments to add.

</td></tr></tbody>
</table>4.  Select **Save**.

    The asset group record opens with related lists for adding subgroups and assets.

5.  Select the View dependency map icon, ![View dependency map](../image/dependency-map-icon.png), next to an asset group, in the Asset groups page, to view the relationship between an asset group, subgroups, and assets.

    ![Dependency map](../image/dependency-map-graphic.png)

    If you have the sn\_cmdb\_user role, you can further drill down by selecting the dependency map icon. For example, in the screenshot, select the dependency map icon on the Surgery Room 1 node to further drill down. Additionally, if you have the app\_service\_admin role, you can view the **Related items** contextual panel on the right side of the Dependency map page.


-   **[Create an asset subgroup in Enterprise Asset Management](create-asset-subgroup-eam.md)**  
Create a subgroup to add child asset groups to an asset group.
-   **[Add assets to an asset group or subgroup](add-assets-assetgroups.md)**  
Add existing assets to an asset group or a subgroup.

**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

