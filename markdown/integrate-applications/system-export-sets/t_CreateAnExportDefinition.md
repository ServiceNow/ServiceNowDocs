---
title: Create an export definition
description: Create an export definition to define what data to export in an export set.
locale: en-US
release: yokohama
product: System Export Sets
classification: system-export-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Export sets, Exports, Data and Automation]
---

# Create an export definition

Create an export definition to define what data to export in an export set.

## Before you begin

Role required: export\_set\_admin

## About this task

An export definition specifies the data to be exported in an export set. This data includes a table, one or more fields, and optionally a filter to limit the included records.

## Procedure

1.  Navigate to **All** &gt; **System Export Sets** &gt; **Export Definition**.

2.  Click **New**.

3.  Enter a descriptive **Name** for the export definition.

4.  Select the **Table** to export data from.

5.  Select one or more **Fields** from the selected table to export data from.

6.  Specify a **Filter** to export only certain records from the selected table.

    Specifying a filter condition on the Created \(sys\_created\_on\) or Updated \(sys\_updated\_on\) fields may prevent scheduled data exports from using delta exports functionality. Do not specify filter conditions on these fields if you intend to use scheduled delta exports.


