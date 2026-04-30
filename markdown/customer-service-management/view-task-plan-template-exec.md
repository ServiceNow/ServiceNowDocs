---
title: View task plan template executions
description: View tracking and diagnostic information for every execution of task plan templates in the Task Plan Template Executions table. The information available includes success, failure, and skipped details, along with references for traceability.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 2
breadcrumb: [Task Plan Templates, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# View task plan template executions

View tracking and diagnostic information for every execution of task plan templates in the Task Plan Template Executions table. The information available includes success, failure, and skipped details, along with references for traceability.

## Before you begin

Role required: sn\_task\_plan.viewer

## Procedure

1.  Navigate to **All** &gt; **Task plan templates** &gt; **Published Task Plan Templates**.

2.  Select a task plan template from the list, then navigate to the **Task Plan Template Execution** related list to see the execution record.

3.  In the record, view the information for each task plan template execution.

    The information available includes the following.

<table id="table_dqf_wkn_mhc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The task plan template execution number

</td></tr><tr><td>

Expected records

</td><td>

The total number of records expected to be created.

</td></tr><tr><td>

Created records

</td><td>

How many records actually created, once the task plan is applied.

</td></tr><tr><td>

Errored records

</td><td>

How many records were not created due to an error encountered somewhere \(for example, if there is a business rule preventing insert on the target table of the template item\)

</td></tr><tr><td>

Skipped records

</td><td>

How many records were skipped and not created, due to a condition check failing on the Template Item condition record \[sn\_task\_plan\_template\_item\_condition\]

</td></tr><tr><td>

Execution status

</td><td>

Status can be `Completed`, `In_progress`, or `Completed with Errors`.

 If the task plan has been applied, but there are remaining template items yet to be visited/used to create records, then the status is set to `In_progress`.

 If the task plan has fully been applied with NO errors, then the status is set to `Completed`.

 If the task plan has fully been applied with NO errors, but some records were skipped, then the status is set to `Completed`.

 If the task plan has fully been applied with at least ONE error spotted when attempting to create a record using a template item, then the status is set to `Completed with Errors`.

</td></tr><tr><td>

Execution details

</td><td>

This is a field of type JSON. At the bare minimum, if the task plan has been applied and no records have been `"skipped"` or `"errored"`, then the JSON object looks something like this:

 ```
{
Status: "Completed",
ParentRecord: ['CS0001', 'CS0002'],
RequestNumber: TPEX00001
}
```

 The `Status` key in the JSON object is the same as the `execution_status` field.

 The `ParentRecord` key represents the top-level parent record\(s\) within the newly created hierarchy. It may either represent a singular Glide Record \(record existing in the database\) that was provided, or an array holding the first level of records created from ROOT template items. Root template items are template items without any parent \(top-level\).

 The `RequestNumber` key points back to the `Number` of the Task Plan Template Execution record.

 If there are skipped records or errored records, then the Template Item number of the skipped/errored item is provided. The following is an example where both 'Skipped' and 'Errored' template items were encountered during task plan execution:

 ```
{
Status: "Completed with Errors", //status is set to Completed With Errors, as we encountered an errored record
ParentRecord: ['CS0001', 'CS0002'],
RequestNumber: TPEX00001,
 Skipped: ['TP0002', 'TP0005'],
Errors: ['TP0008']
}
```

</td></tr></tbody>
</table>
