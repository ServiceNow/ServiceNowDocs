---
title: Define ETL entities
description: Define the Extract Transform Load \(ETL\) entities used by the Robust Transform Engine.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create Extract Transform Load \(ETL\) definitions, Robust Import Set Transformers, Import sets, Imports, Workflow Data Fabric]
---

# Define ETL entities

Define the Extract Transform Load \(ETL\) entities used by the Robust Transform Engine.

## Before you begin

Role required: import\_transformer

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **ETL Definitions**.

2.  Select an ETL definition.

3.  On the ETL Entities tab, click **New**.

4.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the ETL entity.|
    |Table|Target table for the ETL entity.|
    |Path|Unique path for this entity. Should not specify any path for the entity representing the import set table. When an entity represents a collection, the path must end with \[\*\]. This requirement applies to intermediate entries and the target table entity.|
    |Synchronize Inserts|Selected to guarantee only one record with unique coalesce field values by synchronizing record inserts. Unselected if you don't want to synchronize record inserts.|
    |Run business rules|Selected to run business rules. Unselected if you don't want to run business rules.|
    |Application|Application scope for this record.|
    |Definition|Selected ETL entity.|

5.  Click **Submit**.


