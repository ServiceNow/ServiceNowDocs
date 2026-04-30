---
title: Synchronize Data Separation
description: Synchronize Data Separation when the configuration is changed in the lens, supported entities, or entity-group mappings tables.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Data Separation, Strategic Portfolio Management]
---

# Synchronize Data Separation

Synchronize Data Separation when the configuration is changed in the lens, supported entities, or entity-group mappings tables.

## Before you begin

Role required: sn\_ds.ds\_admin

## About this task

The **Is data synced** field value must be **true** for all records of the Data Separation configuration \(lens, entities, entity-group mappings\) to restrict the data according to the Data Separation configuration. If the **Is data synced** field value for any part of the configuration record is **false**, the data separation isn’t synchronized.

The **Is data synced** field value is **false** only when any of the configurations for Data Separation are changed.

## Procedure

1.  Perform the following steps to synchronize data separation depending on the type of configuration change made in Data Separation.

<table id="table_vjp_xk5_rpb"><thead><tr><th>

For this configuration change

</th><th>

Perform these steps

</th></tr></thead><tbody><tr><td>

-   Data Separation is turned off on the existing lens and then enabled again on the same lens
-   Data separation is turned off on the existing lens and then enabled again on another lens


</td><td>

1.  Navigate to **All** &gt; **Data Separation** &gt; **Hierarchy**.
2.  From the Lenses list view, select **Sync data separation** to synchronize the lens configuration for Data Separation.


</td></tr><tr><td>

Data Separation is enabled or turned off for an entity

</td><td>

1.  Navigate to **All** &gt; **Data Separation** &gt; **Supported Entities**.
2.  From the Supported Entities list view, select **Sync data separation** to synchronize the entity configuration for Data Separation.


</td></tr><tr><td>

A group is added, removed, or updated for an entity-group mapping record

</td><td>

1.  Navigate to **All** &gt; **Data Separation** &gt; **Entity-Group Mappings**.
2.  From the Entity-Group Mappings list view, select **Sync data separation** to synchronize the entity-group mappings for Data Separation.


</td></tr></tbody>
</table>
**Parent Topic:**[Configuring Data Separation](../concept/configuring-data-separation.md)

