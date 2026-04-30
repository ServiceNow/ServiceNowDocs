---
title: Configure role-based access in Indoor Mapping
description: Configure Indoor Mapping to update role-based access for map administrators, map editors and the map editor limited roles.
locale: en-US
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Configure role-based access in Indoor Mapping

Configure Indoor Mapping to update role-based access for map administrators, map editors and the map editor limited roles.

## Before you begin

Role-based access to Indoor Mapping Map Studio requires the following three roles:

-   Map administrator \(sn\_map\_core.map\_admin\): Map admins in Map Studio can set up the map data and objects in Indoor Mapping Map Studio and has complete access to the application. Map admins can also manage user criteria records.
-   Map editor \(sn\_map\_core.map\_editor\): Map editors can set up maps in the Indoor Mapping Map Studio, import floor plans, and can manage maps \(edit or delete\) in the Map Studio.
-   Map editor limited \(sn\_map\_core.map\_editor\_limited\): This role has limited access to a campus or only few campuses. Users with this role can view and edit campuses that are assigned to them. The Indoor Mapping **All** &gt; **Indoor Mapping** &gt; **Map Studio** menu is hidden and is not available for this role.

    Map administrators can add user criteria record to provide access to a campus for the map editor limited role. Users with map editor limited role cannot view a Campus in the application context menu search **All** &gt; **Indoor Mapping** &gt; **Campuses**.


Add a user criteria record to decide which users, roles, and groups can access a campus.

Role required: map admin

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Select and open a user record.

3.  In the **Roles** related list, click **Edit**.

4.  In the **Collection** list, select the **sn\_map\_core.map\_editor\_limited** role, and click **Add**.

5.  Select **Save**.

6.  To provide access to a campus in Map Studio, navigate to **All** &gt; **Indoor Mapping** &gt; **Campuses**.

7.  From the Campus page, select a campus to open it.

    Select a campus for which you want which you want to provide the map editor limited role access.

8.  Select **Campus Editors** tab in the Related List section.

9.  Select **User criteria**, click **New**.

    On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |User criteria|Search and select Users with sn\_map\_core\_map\_editor\_limited role.|
    |Campus|Select a campus or create a new campus to provide user access to this role.|

10. Click **Submit**.

    **Note:** If a user with map editor limited role deletes a building, the building is only made inactive in the database and is not actually deleted from the database.


**Parent Topic:**[Configure Indoor Mapping](../concept/configure-ind-mapping.md)

**Previous topic:**[Configure your map instance data](configure-map-data.md)

**Next topic:**[Indoor Mapping properties](indoor-mapping-properties.md)

