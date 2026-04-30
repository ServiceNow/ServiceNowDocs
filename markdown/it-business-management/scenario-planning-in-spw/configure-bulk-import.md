---
title: Configure bulk import
description: This system property enables you to update the bulk import functionality in Strategic Planning with PPM, Agile 2.0, and SAFe.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Strategic Planning with PPM, Agile 2.0, and SAFe, Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure bulk import

This system property enables you to update the bulk import functionality in Strategic Planning with PPM, Agile 2.0, and SAFe.

## Before you begin

Role required: sn\_align\_core.apw\_admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  Search for **com.sn\_align\_cmn\_int.bulk\_import**.

3.  Set the property value to either of the following options.

    |Value|Description|
    |-----|-----------|
    |**Upsert**|Enables update and inserting of new work items.|
    |**Insert**|Enables inserting new work items only. This is the default value.|

    When the records are imported from PPM, Agile Development 2.0, or SAFe to Strategic Planning , only the last comment will be imported.


