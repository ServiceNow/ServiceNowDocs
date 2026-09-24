---
title: Create an entity for a new equipment model
description: Create an entity for a new equipment model. You do this task when you want to manually create a new equipment model entity directly in the ServiceNow AI Platform rather than import the equipment model data from an external source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/create-entity-new-equipment-model.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# Create an entity for a new equipment model

Create an entity for a new equipment model. You do this task when you want to manually create a new equipment model entity directly in the ServiceNow AI Platform rather than import the equipment model data from an external source.

## Before you begin

Role required: cmdb\_ot\_isa\_editor or cmdb\_ot\_isa\_admin

## About this task

Users with an cmdb\_ot\_isa\_admin role can view equipment model entities for any site. However, users with an assigned cmdb\_ot\_isa\_editor role can access only those sites that an administrator has granted access to for specific users. To learn more about granting site access, see [Manage equipment model site access for non-administrators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/create-user-criteria-for-equipment-model-entity-site-users.md).

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** &gt; **Equipment Model Manager**.

2.  In the **Equipment model view for** field, select a site.

    Search for a site by entering the site name or short code.

3.  Select **Create new entity**.

4.  In the **Create new entity** window, search for and select the parent entity.

    **Note:** Search by short code or name.

5.  Complete the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Parent|Name of the entity, if any, that is the parent to this entity. The currently selected equipment model appears as the parent entity. To change the parent, search for and select a different entity that is a parent to the entity that you're creating.|
    |Entity name|Name of the equipment model entity.|
    |Short Code|Short code assigned to this entity.|
    |Entity type|Name of the level type that is assigned to the equipment model template level. For example, Material Assembly or Production Cell for a Work Center level. Search for and select an entity type. For more information, see [Create equipment model level types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/create-equipment-model-template-type.md).|

6.  Select **Save**.

7.  In the Details form, complete the additional fields for the equipment model entity.

    For more information, see [Review and update the equipment model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/equipment-model-workspace.md).


**Parent Topic:**[Review and update the equipment model details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/equipment-model-workspace.md)

