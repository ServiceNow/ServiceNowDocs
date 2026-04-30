---
title: Monitor concurrent import set jobs
description: Check the status of concurrent import set jobs.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Data and Automation]
---

# Monitor concurrent import set jobs

Check the status of concurrent import set jobs.

## Before you begin

Role required: import\_admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Concurrent Import Set Jobs**.

2.  Review the **Type** and **State** of each parent import set job.

<table id="choicetable_x4w_hjd_vfb"><tbody><tr><td id="d503790e76">

**Type**

</td><td>

Type of concurrent import set job:-   **Regular** if you are running the scheduled import for the first time
-   **Reprocessing** if you are rerunning the scheduled import
-   **Resuming** if you are resuming a scheduled import that had an error


</td></tr><tr><td id="d503790e103">

**State**

</td><td>

Status of the import set job:-   **Pending** if import processing has not started
-   **Running** when import processing has started
-   **Completed** when import processing has finished
-   **Error** if import processing did not finish successfully


</td></tr></tbody>
</table>3.  Select a parent import set job to review the **Type** and **State** of each of its child import set jobs.


**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

