---
title: Review and update the equipment model details
description: Review and update the details for an equipment model that you imported into the ServiceNow AI Platform so that you can make sure that the information is correct. You can also manually create a new equipment model entity and then add details to it.
locale: en-US
release: yokohama
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Review and update the equipment model details

Review and update the details for an equipment model that you imported into the ServiceNow AI Platform so that you can make sure that the information is correct. You can also manually create a new equipment model entity and then add details to it.

## Before you begin

Import equipment model data to the ServiceNow AI Platform. To learn more, see [Importing equipment model data](../concept/importing-isa95-equipment-model-etl.md).

Role required: cmdb\_ot\_isa\_viewer, cmdb\_ot\_isa\_editor, cmdb\_ot\_isa\_admin.

## About this task

If you have an assigned cmdb\_ot\_isa\_viewer role, you can only view equipment model entities. If you have any of the other assigned cmdb\_ot\_isa roles, you can also edit equipment model entities.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Manager**.

2.  In the **Equipment model view for** field, select the site that you want to view the equipment model information for.

    You can search for a site by typing in the site name or its short code.

3.  Review an existing equipment model entity, or create one.

<table id="choicetable_nnq_bxc_3qb"><thead><tr><th align="left" id="d31169e111">

Task

</th><th align="left" id="d31169e114">

Description

</th></tr></thead><tbody><tr><td id="d31169e120">

**Review and update an existing equipment model**

</td><td>

In the selector pane, do the following actions:1.  Expand the equipment model hierarchy.
2.  Click the entity that you want to view.


</td></tr><tr><td id="d31169e138">

**Create an equipment model entity and populate the details**

</td><td>

1.  Click **Create new entity**.
2.  In the Create new entity form, fill in the details. To learn more, see [Create an entity for a new equipment model](create-entity-new-equipment-model.md).
3.  Click **Save**.
4.  Use the Equipment model view details form to enter the remaining details for the new equipment model entity.


</td></tr></tbody>
</table>4.  On the form, review and update the fields.

<table id="table_mgm_jsv_hqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity name

</td><td>

Name of the equipment model entity.**Note:** You can update the Entity name field after the equipment model entity is created. Updating this field also updates the tree component and site filter.

For more information, see [Update the entity name or parent of an equipment model entity](update-the-name-or-parent-equipment-model-entity.md).

</td></tr><tr><td>

Parent

</td><td>

Name of the entity, if any, that is the parent to this equipment model entity. This field is empty for the top-level parent entity, which has no parent. The top-level parent entity is referred to as a site.**Note:** You can update the Parent field after the equipment model entity is created.

Updating this field also updates the tree component and site filter. For more information, see [Update the entity name or parent of an equipment model entity](update-the-name-or-parent-equipment-model-entity.md).

</td></tr><tr><td>

Template

</td><td>

Equipment model template that is assigned to an equipment model entity you manually create.**Note:** You can't assign an equipment model template to an equipment model that you imported into the ServiceNow AI Platform® using the Integration Hub ETL or a third-party integration.

</td></tr><tr><td>

Level

</td><td>

Hierarchical level that is assigned from the selected equipment model template for data sorting and structuring purposes. Examples are as follows:-   **Site**

Industrial site.

-   **Area**

Area in an industrial site.

-   **Work Center**

Work center in an industrial site.

 Search for and select an equipment level to assign to the equipment model entity. To learn more, see [Create hierarchical sorting levels for an equipment model template](create-equipment-model-template-levels.md).

</td></tr><tr><td>

Type

</td><td>

Name of the level type that is assigned to the equipment model template level. For example, Material Assembly or Production Cell for a Work Center level. To learn more, see [Create equipment model level types](create-equipment-model-template-type.md).

</td></tr><tr><td>

Short description

</td><td>

Short description of this equipment model entity and its purpose.

</td></tr><tr><td>

Short Code

</td><td>

Short code that is assigned to this equipment model entity.

</td></tr><tr><td>

Path

</td><td>

Concatenation of the short codes of this equipment model entity and all its parent entities. For example, `ATL-B42-MQSTOR-Z1` is the concatenation of the following short codes: -   ATL short code for the Atlanta site.
-   B42 short code for Building B42.
-   MQSTORE short code for Model M and Q.
-   Z1 short code for the Zone 1 transfer storage zone for Model M and Q.


</td></tr><tr><td>

Location

</td><td>

Location of the equipment model entity. For example, Atlanta Building 64 would be the location for each associated equipment model that is located there. Search for and select the location to assign to the equipment model entity.

</td></tr><tr><td>

Company

</td><td>

Name of the company that is associated with the equipment model entity. Search for and select a company to assign to the entity.

</td></tr><tr><td>

Assigned to

</td><td>

Assigned user who operates and handles this equipment model entity. Search for and select the user to assign to the entity.

</td></tr><tr><td>

Managed by

</td><td>

Name of the assigned person who owns and is responsible for managing this entity record. Search for and select the user to assign to the equipment model entity.

</td></tr><tr><td>

Process criticality

</td><td>

Measure of how critical, or important, the equipment model entity is to the industrial process. Select the process criticality for the entity. For example:-   1 - most critical.
-   2 - somewhat critical.


</td></tr><tr><td>

Support Group

</td><td>

Name of the group that supports this equipment model entity. Search for and select the user group to assign to the equipment model entity.

</td></tr><tr><td>

Managed by Group

</td><td>

Name of the assigned group that owns and is responsible for managing this entity record. Search for and select the user group to assign to the entity.

</td></tr><tr><td>

Company

</td><td>

Name of the company that the equipment model entity belongs to. The core\_company value is stored in the CMDB in the ServiceNow AI Platform as a reference.

</td></tr><tr><td>

Operational status

</td><td>

Current operational status of the equipment model entity:-   **Operational**

Entity that is fully operational in the production process.

-   **Non-Operational**

Entity that is non-operational in the production process.

-   **Not in use**

Entity that is operational but intentionally offline. You can use this value to designate which sites are included for licensing purposes.

The sites marked as **Not in use** won't be visible in the Equipment Model Manager of the Industrial Workspace.

</td></tr></tbody>
</table>5.  Review the associated equipment model data in the related list tabs as follows:

<table id="table_tlh_qxq_bqb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View the equipment model hierarchy

</td><td>

See [View the equipment model hierarchy](viewing-equipment-model-hierarchy.md).

</td></tr><tr><td>

Map the upstream production processes for the equipment model entity.

</td><td>

1.  Click **Upstream Process**.
2.  To learn more, see [Map the upstream production processes for the selected equipment model entity](map-upstream-production-processes-equipment-model-entity.md).


</td></tr><tr><td>

Map the downstream production processes for the equipment model entity.

</td><td>

1.  Click **Downstream Process**.
2.  To learn more, see [Map the downstream production processes for the selected equipment model entity](map-downstream-production-processes-equipment-model-entity.md).


</td></tr><tr><td>

View the child entities for the equipment model entity.

</td><td>

1.  Click **Child Entities**.
2.  To learn more, see [Review the child entities for the equipment model entity](view-child-entities-equipment-model-entity.md).


</td></tr><tr><td>

View the OT devices that are associated with the current equipment model entity and its child entities.

</td><td>

1.  Click **Mapped OT Devices**.
2.  To learn more, see [Add OT devices that are associated with the selected equipment model entity](../concept/view-ot-assets-equipment-model-entity.md).
 **Note:** By default, you cannot see OT control modules in this list.

</td></tr></tbody>
</table>6.  When you finish reviewing and updating the equipment model details, do one of the following actions.

    |Action|Description|
    |------|-----------|
    |**Save the updated equipment model entity**|Click **Save**.|
    |**Delete the equipment model entity**|Click **Delete**.|


## What to do next

To view the roll up for OT data associated with the equipment model entity and its child entities, you can use the following related lists in the equipment model entity record. The roll up view represents the OT devices, OT incidents, OT changes, and so on that automate the entire hierarchy of an equipment model entity.

-   Mapped OT Devices
-   OT Incidents
-   OT Change Requests
-   Vulnerable Items
-   Remediation Tasks

-   **[Create an entity for a new equipment model](create-entity-new-equipment-model.md)**  
Create an entity for a new equipment model. You do this task when you want to manually create a new equipment model entity directly in the ServiceNow AI Platform rather than import the equipment model data from an external source.
-   **[View the equipment model hierarchy](viewing-equipment-model-hierarchy.md)**  
View a graphical representation of the hierarchical structure of the selected equipment model entity, and its relationships to other entities in the production process.
-   **[View the equipment model OT device map](view-equipment-model-ot-device-map.md)**  
View the graphical representation of the selected equipment model entity and its relationship to other Operational Technology \(OT\) devices in the production process.
-   **[View the equipment model OT dependency map](view-equipment-model-ot-dependency-map.md)**  
View the graphical representation of the hierarchical structure of the selected equipment model entity and its relationship with other entities and devices in the production process.
-   **[Map the upstream production processes for the selected equipment model entity](map-upstream-production-processes-equipment-model-entity.md)**  
Use the upstream process to review upstream production processes for the selected equipment model entity. You can also create and map a new upstream production process for the equipment model entity.
-   **[Map the downstream production processes for the selected equipment model entity](map-downstream-production-processes-equipment-model-entity.md)**  
Use the downstream process to review the downstream production processes for the selected equipment model entity. You can also create and map a new downstream production process for the equipment model entity.
-   **[Review the child entities for the equipment model entity](view-child-entities-equipment-model-entity.md)**  
Review the child entities that are associated with the selected equipment model entity. You can review the relationships of the associated entities that are subordinate to a higher-level entity.
-   **[Add OT devices that are associated with the selected equipment model entity](../concept/view-ot-assets-equipment-model-entity.md)**  
Use OT devices to review the OT devices that are associated with the selected equipment model entity and its child entities. You can also select and associate other OT devices to the selected equipment model entity.
-   **[Update the entity name or parent of an equipment model entity](update-the-name-or-parent-equipment-model-entity.md)**  
Update the entity name or parent fields in an equipment model entity record as needed to help keep your equipment model information up to date.
-   **[Bulk edit a site's Operational Technology Vulnerability Response assignment group](../../mftg-manufacturing-ot-vulnerability-response/task/bulk-edit-assignment-group-otvr.md)**  
Use the bulk edit feature to update the Operational Technology Vulnerability Response \(OT VR\) assignment group field in multiple site records at once.
-   **[Search for an equipment model entity](search-equipment-model-entities.md)**  
Search for an equipment model entity in the Industrial Workspace so that you can find the entity more quickly and efficiently.
-   **[View all OT devices by managed network](view-ot-devices-managed-by-network.md)**  
View your Operational Technology \(OT\) devices by managed network on the ServiceNow AI Platform.
-   **[Filter equipment model entities by operational status](filter-out-non-operational-equipment-model-entities.md)**  
Filter how equipment model entities appear in the Equipment Model Manager on the Industrial Workspace using a system property. Filtering equipment model entities can help you organize the data shown on the Industrial Workspace.
-   **[Favorite a child equipment model entity](favorite-child-equipment-model-entity.md)**  
Favorite a child equipment model entity in the Equipment Model Manager of the Industrial Workspace so that you can access a tailored view of your favorites while working.

**Parent Topic:**[Managing equipment models](managing-equipment-models-after-data-import.md)

