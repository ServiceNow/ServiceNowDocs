---
title: Enable the CMN location property
description: To synchronize CMN Location types with Indoor Mapping, enable the system property sn\_map\_core.cmn\_location\_sync\_enabled.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Synchronize Indoor Mapping with CMN Locations, Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Enable the CMN location property

To synchronize CMN Location types with Indoor Mapping, enable the system property **sn\_map\_core.cmn\_location\_sync\_enabled**.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_properties.list**.

2.  In the System Properties page, search for **cmn** in the **Name** column.

3.  Select to open the **sn\_map\_core.cmn\_location\_sync\_enabled** property.

    ![CMN location synchronization enabled property](../images/wsd-cmn-location-system-properties.png)

    Default value of this property is **true**.

    **Note:** If Workplace Service Delivery is installed in your system, this property should be set to **false**. You can enable this property \(if it is set to false and if Workplace Service Delivery is not installed \) to synchronize CMN locations and location types with Indoor Mapping map data.


**Parent Topic:**[Synchronize Indoor Mapping with CMN Locations](../concept/sync-cmn-location.md)

**Previous topic:**[Synchronize Indoor Mapping with CMN Locations](../concept/sync-cmn-location.md)

**Next topic:**[Add CMN locations and map it to Indoor Mapping Place types](enable-cmn-location-types.md)

