---
title: Enhanced Sync Properties
description: You can define the behavior of sync operations by configuring the Enhanced Sync properties.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Enhanced Sync Properties

You can define the behavior of sync operations by configuring the Enhanced Sync properties.

To access the Enhanced Sync properties, navigate to **All** &gt; **Workplace Core** &gt; **Enhanced Sync** &gt; **Enhanced Sync Properties**

You must have the sn\_wsd\_indoor\_map.admin role or the sn\_wsd\_core.workplace\_manager role to configure the enhanced sync properties.

<table id="table_ddg_4q2_5fc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_indoor\_map.es\_automate\_create

</td><td>

Enables the creation of WSD location records as part of the sync process.You can enter the following options to enable creation of location records.

-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_automate\_update

</td><td>

Enables the updating of WSD location records as part of the sync process.You can enter the following options to enable updating of location records.

-   campus
-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_automate\_retire

</td><td>

Enables the retirement of WSD location records as part of the sync process. All retirements require review and acknowledgment.You can enter the following options to enable retirement of location records.

-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_sync\_activity\_enabled

</td><td>

Option to log activities for enhanced sync.You can view the enhanced sync activities by navigating to **All** &gt; **Workplace Core** &gt; **Enhanced Sync** &gt; **Enhanced Sync Activities**.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_automate\_link

</td><td>

Enables or disables the linking of WSD location records as part of the sync process.You can enter the following options to enable updating of location records.

-   campus
-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr></tbody>
</table><table id="table_wy4_d52_5fc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_wsd\_indoor\_map.es\_sync\_name\_to\_im

</td><td>

Enables synchronizing name changes from WSD to Indoor Mapping.You can enter the following options to enable synchronization of location records.

-   campus
-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_sync\_title\_to\_im

</td><td>

Enables synchronizing title changes from WSD to Indoor Mapping.You can enter the following options to enable synchronization of location titles.

-   campus
-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_sync\_spacetype\_to\_im

</td><td>

Enables synchronizing space-type changes from WSD to Indoor Mapping.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_default\_space\_type

</td><td>

WSD space type to be used when no place type mapping is found.

</td></tr><tr><td>

sn\_wsd\_indoor\_map.es\_automate\_deactivate

</td><td>

Enables the deactivation of Indoor Mapping records as part of the sync process.You can enter the following options to enable deactivation of Indoor Mapping records.

-   campus
-   building
-   floor
-   space

You can enter multiple options by separating them with a comma.

</td></tr></tbody>
</table>**Parent Topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

**Previous topic:**[Floor map import group form](import-group-form.md)

**Next topic:**[Bulk upload Excel columns](bulk-template-columns.md)

