---
title: Configure catalogs
description: Enable your users to view and request their associated items in the Now Mobile app. If no catalogs are selected, users can view and request items from all catalogs in the system. By default, the app uses Service Catalog.
locale: en-US
release: zurich
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Configure catalogs

Enable your users to view and request their associated items in the Now Mobile app. If no catalogs are selected, users can view and request items from all catalogs in the system. By default, the app uses Service Catalog.

## Before you begin

Role required: admin

## About this task

Demonstrates configuring service catalogs, knowledge bases, and My Requests in the Now Mobile App.

## Procedure

1.  Navigate to **All** &gt; **Now Mobile App** &gt; **Catalogs**.

2.  In the portal catalogs \[m2m\_sp\_portal\_catalog\] table, add a catalog in addition to the base system catalog, or change the catalog that is associated with the base system record:

    1.  Click **New** or open the base system record.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Portal|Portal that you select. Select **Employee Center**.|
        |Catalog|Catalog that you would like to associate with the app.|
        |Order|Number that indicates the order that the configurations should run. If there are multiple configurations on a portal, the system runs the configurations from the lowest to the highest order that you selected.|


## Result

Your users can view and request items from all added catalogs.

