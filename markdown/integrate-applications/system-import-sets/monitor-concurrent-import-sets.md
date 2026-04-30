---
title: Monitor concurrent import sets
description: Monitor concurrent import sets to check the status of import sets and import set jobs, resume or reprocess import sets, and view transform history.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Importing data using import sets, Import sets, Imports, Data and Automation]
---

# Monitor concurrent import sets

Monitor concurrent import sets to check the status of import sets and import set jobs, resume or reprocess import sets, and view transform history.

## Before you begin

After executing a concurrent data import, use the Concurrent Import Set Jobs to verify the status.

Role required: import\_admin.

## About this task

When a scheduled concurrent import runs, each concurrent import creates a concurrent import set record. All related import sets, concurrent import set jobs, and transform histories are shown in the form view.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Concurrent Import Set Jobs**.

2.  Select the scheduled import for which you want to check the status.

3.  Reprocess or continue import sets, check the status of import sets or concurrent import set jobs, view transform history, or display a list of executions records by clicking one of the following related links.

<table id="choicetable_m23_bsg_wfb"><tbody><tr><td id="d376765e85">

**Reprocess**

</td><td>

Start another scheduled import to reprocess the records.

</td></tr><tr><td id="d376765e94">

**Continue**

</td><td>

Restart a scheduled import that is not complete.

</td></tr><tr><td id="d376765e103">

**Import Sets**

</td><td>

State of import sets.**State**

-   **Pending** if the system has not started processing the import set.
-   **Running** if the system is processing the import set.
-   **Processed** if the system has completed processing the import set.
-   **Error** if the import set processing failed.
 Select an import set to see processing details for Import Set Runs and Import Set Rows for the import set.

</td></tr><tr><td id="d376765e142">

**Concurrent Import Set Jobs**

</td><td>

Type and state of concurrent import set jobs:-   **Type**
    -   **Regular** if you are running the scheduled import for the first time.
    -   **Reprocessing** if you are rerunning the scheduled import.
    -   **Resuming** if you are resuming a scheduled import that had an error.
-   **State**
    -   **Pending** if the system has not started processing the import set.
    -   **Running** if the system is processing the import set.
    -   **Completed** if the system has completed processing the import set.
    -   **Error** if the import set processing failed.
 Select an import set job to see processing details for Import Set Runs and Import Set Rows for the import set job.

</td></tr><tr><td id="d376765e212">

**Transform Histories**

</td><td>

Check statistics in the transform histories for the scheduled import.Select a start time to see Import Set Row Errors \(including error codes and messages\) and the Import Log for the scheduled import.

</td></tr><tr><td id="d376765e225">

**Executions**

</td><td>

Executions contexts-   The parent import scheduled data import record.
-   The execution record numbers for each scheduled import in a concurrent import.
-   Import set records that are part of a scheduled import.
-   The scheduled import record names.
-   The date that the execution context was created.


</td></tr></tbody>
</table>
**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

