---
title: Monitor scheduled data import executions
description: Monitor scheduled data import executions to see the hierarchy and flow of the scheduled chained imports.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Monitor scheduled data import executions

Monitor scheduled data import executions to see the hierarchy and flow of the scheduled chained imports.

## Before you begin

If after executing a scheduled concurrent data import there are indications of a problem, use the Execution Contexts to see the details necessary to diagnose the issue.

Role required: import\_admin

## About this task

The execution contexts feature enables you to identify the order of execution of concurrent import sets. You can also open the import set records to access the import log.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Execution Contexts**.

2.  In the list of execution contexts, select one record.

    The table lists:

    -   The parent import scheduled data import record.
    -   The execution record numbers for each scheduled import in a concurrent import.
    -   All the import set records that are part of a scheduled import.
    -   The scheduled import record names.
    -   The date that the execution context was created. This date is when the import executed.
3.  To add any of the following fields, click the personalized list icon \(![Personalized list icon.](../image/gearicon.png)\):

    -   **Created by**
    -   **Import Set Table**
    -   **Updated**
    -   **Tags**
    -   **Updated by**
    -   **Updates**
4.  To open a record, click a record name or number.

5.  To display the execution record, click the execution record number.

    The execution record shows:

    -   Scheduled import name.
    -   Import set table.
    -   Import Set number.
    You can open the import set record from the execution record.


**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

