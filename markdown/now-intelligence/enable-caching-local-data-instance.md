---
title: Enable data caching for a local data instance
description: To help reduce the load time of data visualizations, and if real time or very fresh data is not necessary, enable data caching on the data source.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use a local data instance with a data visualization, Technical dashboards, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Enable data caching for a local data instance

To help reduce the load time of data visualizations, and if real time or very fresh data is not necessary, enable data caching on the data source.

## Before you begin

Role required: ui\_builder\_admin, admin

## Procedure

1.  Open the UI Builder page with the local data instance whose data you want to cache.

2.  In the Data and scripts drawer, under Data resources, select the desired local data instance.

3.  Scroll down to **Use data cache** and turn it on.

    Any data visualization that uses this data source, uses the cache settings on the data source. The data cache settings on the visualization itself are removed from the configuration panel.

4.  Set other caching properties as needed.

    |Property|Description|
    |--------|-----------|
    |Cache expiration time|How long the cache, once created, is retained before being updated in the cache refresh job.|
    |Invalidate cache|Use this setting with extra logic you create to invalidate the cache and fetch fresh data. For example, you can add a Button component to the page and script its event handler to invalidate the cache.|
    |Additional key|Enter a string that will contribute to generating the unique hash key for each data cache created on this data instance. Use a unique additional key value for each local data instance.|


**Parent Topic:**[Use a local data instance with a data visualization](dv-local-data-instance.md)

