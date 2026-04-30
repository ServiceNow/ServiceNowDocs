---
title: Snapshot Impacted tables
description: Few Indoor Mapping and Workplace Indoor Mapping tables are impacted during the snapshot process when the Indoor Mapping backup data is migrated to Workplace Service Delivery instances.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: reference
last_updated: "2025-02-12"
reading_time_minutes: 1
breadcrumb: [Indoor Mapping references, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Snapshot Impacted tables

Few Indoor Mapping and Workplace Indoor Mapping tables are impacted during the snapshot process when the Indoor Mapping backup data is migrated to Workplace Service Delivery instances.

## Indoor Mapping Tables

**Note:** After moving the snapshots, the Space Details table \[sn\_wsd\_spcmgmt\_space\_detail\] in Workplace Space Management doesn't get populated with the snapshots. To get the updated Space details table record, manually run the fix script **Load space details table- current state**. Navigate to **All** &gt; **Fix Scripts** and search for Workplace Space Management **Load space details table- current state** fix script. Select **Run Fix Script** tab to run the script and get latest Space Details table \[sn\_wsd\_spcmgmt\_space\_detail\] record.

The following tables are affected during the snapshot process.

|Tables|
|------|
|Workplace Indoor Mapping Tables|
|sn\_wsd\_core\_campus|
|sn\_wsd\_core\_building|
|sn\_wsd\_core\_floor|
|sn\_wsd\_core\_space|
|sn\_wsd\_core\_area|
|Indoor Mapping Tables|
|sn\_map\_core\_campus|
|sn\_map\_core\_building|
|sn\_map\_core\_floor|
|sn\_map\_core\_node|
|sn\_map\_core\_route|
|sn\_map\_core\_connector|
|sn\_map\_core\_m2m\_route\_direction\_mode|
|sn\_map\_core\_layer|
|sn\_map\_core\_tile|
|sn\_map\_core\_autocad\_source|
|sn\_map\_core\_autocad\_source\_layer|
|sn\_map\_core\_autocad\_source\_block|
|sn\_map\_core\_autocad\_source\_text|
|sn\_map\_core\_geojson\_source|
|sn\_map\_core\_raster\_source|
|sn\_map\_core\_job|
|sn\_map\_core\_place|
|sn\_map\_core\_place\_entrance|
|sn\_map\_core\_place\_marker|
|sn\_map\_core\_place\_properties|
|sn\_map\_core\_view\_content|
|sn\_map\_core\_m2m\_campus\_editor|
|sn\_map\_core\_m2m\_view\_type\_campus\_direction\_mode|
|sn\_map\_core\_m2m\_view\_type\_campus\_reader|

**Parent Topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

**Previous topic:**[Indoor Mapping terminology](indoor-mapping-common-terminology.md)

**Next topic:**[Map printing options](map-printing-options.md)

**Related topics**  


[Create Snapshots to migrate Indoor Mapping data](../task/snapshot-ind-mapping.md)

