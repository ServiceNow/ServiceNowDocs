---
title: Configure bulk import
description: This system property enables you to update the bulk import functionality in Portfolio Planning with PPM.
locale: en-US
release: yokohama
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Portfolio Planning with PPM, Configure, Portfolio Planning, Strategic Portfolio Management]
---

# Configure bulk import

This system property enables you to update the bulk import functionality in Portfolio Planning with PPM.

## Before you begin

Role required: sn\_align\_core.apw\_admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Search for **com.sn\_align\_cmn\_int.bulk\_import**.

3.  Set the property value to either of the following options.

    |Value|Description|
    |-----|-----------|
    |**UPSERT**|Enables update and inserting of new work items.|
    |**INSERT**|Enables inserting new work items only. This is the default value.|

    When the records are imported from PPM to Portfolio Planning, only the last comment will be imported.


