---
title: Migrate locations from Location table to Workplace locations table
description: After you configure the location migration records, perform the migration action to migrate the locations from the ServiceNow Location table \[cmn\_location\] to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table in Workplace Service Delivery.
locale: en-US
release: zurich
product: Workplace Core
classification: workplace-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure location migration hierarchy, Location migration, Manage, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Migrate locations from Location table to Workplace locations table

After you configure the location migration records, perform the migration action to migrate the locations from the ServiceNow® Location table \[cmn\_location\] to the Workplace Location \[sn\_wsd\_core\_workplace\_location\] table in Workplace Service Delivery.

## Before you begin

Ensure the following:

-   The location migration configurations are active. For more information, refer to [Configure location migration hierarchy](add-location-migration-hierarchy.md).
-   The location migration configuration from Campus to lower levels must always be in the Campus &gt; Building &gt; Floor &gt; Area &gt; Room/Space order. You can also have an optional hierarchy for a location migration configuration.

If you want to change the location type of a location created in the Location table \[cmn\_location\], see [Set the location type in Location table](set-loc-type-in-loc-table.md).

Role required: sn\_wsd\_core.admin

## Procedure

1.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Location migration configuration**.

2.  On the Location Migration Configurations page, select the location migration configurations that you want to migrate.

    **Note:** Ensure that the location migration configurations are active.

3.  Click **Migrate Locations**.

4.  In the confirmation dialog box, click **OK**.


## Result

The location migration process runs in the background.

