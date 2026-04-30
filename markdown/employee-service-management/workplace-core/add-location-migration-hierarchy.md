---
title: Configure location migration hierarchy
description: Create a hierarchy for how the location data from the ServiceNow Location table \[cmn\_location\] must be migrated to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table of Workplace Service Delivery.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Location migration, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Configure location migration hierarchy

Create a hierarchy for how the location data from the ServiceNow® Location table \[cmn\_location\] must be migrated to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table of Workplace Service Delivery.

## Before you begin

Role required: sn\_wsd\_core.admin

## About this task

The following location hierarchy is followed throughout the Workplace Service Delivery applications. The location migration configurations for these hierarchies are also available by default:

**Note:** The location migration configuration records of the following location hierarchies are inactive by default.

|Parent|Child|
|------|-----|
|None|Region|
|Region|Site|
|Site|Campus|
|Campus|Building|
|Building|Floor|
|Floor|Area|
|Area|Room|
|Area|Space|

For more information about location migration configuration and conditions, refer to [Location migration](../concept/location-migration.md).

After you create the location migration configurations, you must perform the migration separately. To perform the migration after location migration configuration, refer to [Migrate locations from Location table to Workplace locations table](migrate-locations-from-loc-table-to-workplaceloc-table.md).

**Note:** You cannot migrate locations if they are not as the same as the Workplace Service Delivery location migration hierarchy, which is Region &gt; Site &gt; Campus &gt; Building &gt; Floor &gt; Area &gt; \(Room &gt; Space\) or \(Space &gt; Room\).

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Location migration configuration**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Parent table|Parent workplace location table. The **Workplace location** is considered as the child workplace location table. The parent location is automatically generated after you select the **Workplace location**.|
    |Workplace location table|Child workplace location table. This location is set as the child location in the hierarchy configuration.|
    |Is optional hierarchy|Option to set this location migration configuration as optional. For example, if there are locations that do not match the Area &gt; Room hierarchy, then they are matched with the next hierarchy, which is Floor &gt; Room. If there are Rooms that are not assigned to any Areas, then they are matched with Floors directly because Area is optional.|
    |Application|Application of the location migration configuration. Ensure that **Workplace Safety Management** is selected. This field is automatically set.|
    |Active|Option to activate the location migration configuration.|
    |Domain|Domain of the location migration configuration. This field is automatically set.|
    |Location condition|Conditions based on which the locations must be filtered for migration. The locations are filtered based on their Location type for the migration.|

4.  Click **Submit**.


## Result

The location migration configuration record is added. The locations that match the specified conditions are filtered.

## What to do next

[Migrate locations from Location table to Workplace locations table](migrate-locations-from-loc-table-to-workplaceloc-table.md).

