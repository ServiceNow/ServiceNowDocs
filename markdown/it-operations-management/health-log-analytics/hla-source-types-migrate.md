---
title: Export source types to an update set
description: Export source types to an update set separate from the Health Log Analytics data input configuration. You can then import the update set to the target environment.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, source types, migration, data input configuration, update set, export]
breadcrumb: [Migrating Health Log Analytics data input configurations between instances, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Export source types to an update set

Export source types to an update set separate from the Health Log Analytics data input configuration. You can then import the update set to the target environment.

## Before you begin

For an overview of this feature, see [Migrating Health Log Analytics data input configurations between instances](../concept/hla-data-input-migration.md).

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Data Input** &gt; **Source Types**.

2.  In the Source Types list, select one or more source types that you want to export.

3.  From the **Actions on selected rows** drop-down menu, choose **Export Source Types**.

    The source types are exported to an update set.

    **Note:** An update set can act as the parent for multiple child update sets.

4.  Select **Download update set** to download the update set to the instance.

    The update set is downloaded as an XML file.


## What to do next

Import the update set to the required ServiceNow instance. For more information, see [Import source types to a target instance](hla-source-types-import.md).

**Parent Topic:**[Migrating Health Log Analytics data input configurations between instances](../concept/hla-data-input-migration.md)

