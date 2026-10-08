---
title: Assign ISA Access edit permissions by group
description: Grant groups edit access to specific equipment model entities for ISA Access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/industrial-process-manager/assign-isa-access-edit-permissions-by-group.html
release: brazil
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ISA Access by Group, Equipment Model entity access control tables, Configure the Industrial Process Manager, Industrial Process Manager, Operational Technology]
---

# Assign ISA Access edit permissions by group

Grant groups edit access to specific equipment model entities for ISA Access.

## Before you begin

Role required: cmdb\_ot\_isa\_admin or admin

## About this task

The Equipment Model Entity access control interface lets you manage which groups can access specific equipment model entities and what permission level they have. By default, groups have read-only access. Use this procedure to grant edit access to a group for a specific equipment model entity at a site.

## Procedure

1.  Navigate to **All** &gt; **Equipment Model – ISA** &gt; **ISA Access – By Group**.

    The Equipment Model Entity Group Access page opens, showing groups with current access assignments.\[Omitted image ""\] Alt text: Equipment Model Entity Group Access page showing a list of groups with their assigned sites, entities, and access types

2.  Select **New** to create a group access record.

3.  In the **Group** field, enter a group name or select the search icon and select a group from the list.

4.  In the **Site** field, select the search icon to select a site related to this group.

    A site selection is required.

5.  In the **Equipment Model Entity** field, select the search icon and select an entity available from this site.

6.  From the **Access Type** list, select **Edit**.

7.  Select **Submit**.

    The group access record is added to the Equipment Model Entity Group Access list.


## Result

The group can access the equipment model entities with edit permissions. The access is scoped to the selected site and takes effect immediately.

**Parent Topic:**[ISA Access by Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/industrial-process-manager/c-isa-access-by-group.md)

