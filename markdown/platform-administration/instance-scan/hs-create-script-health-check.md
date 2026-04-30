---
title: Create a script only check
description: Create a check without specifying a table or a column type by selecting Create a new Script Only Check. You can verify meta data, configurations, and execute complex checks by writing your own script.
locale: en-US
release: zurich
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a check, Use, Instance Scan, Maintain and monitor, Administer]
---

# Create a script only check

Create a check without specifying a table or a column type by selecting **Create a new Script Only Check**. You can verify meta data, configurations, and execute complex checks by writing your own script.

## Before you begin

Role required: scan\_admin

```
Before performing this task you must complete [Create a check](hs-create-health-check.md).
```

## About this task

The script only check runs only during a full scan and executes only once during a scan.

## Procedure

1.  Select **Create a new Script Only Check** from the **Check Interceptor** list.

2.  On this form, fill in the fields.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the check record.

</td></tr><tr><td>

Application

</td><td>

Application that has the check record.

</td></tr><tr><td>

Category

</td><td>

Category of the check record.

</td></tr><tr><td>

Priority

</td><td>

Priority at which the findings should be resolved.

</td></tr><tr><td>

Version

</td><td>

Current version of the check record.**Note:** If you want to update an already existing check, the **Version** field increments itself.

</td></tr><tr><td>

Active

</td><td>

Option to activate this check record.

</td></tr><tr><td>

Short Description

</td><td>

Mandatory description about the check records.

</td></tr><tr><td>

Description

</td><td>

Additional information about the check records.

</td></tr><tr><td>

Resolution Details

</td><td>

Guideline to avoid check to go off against one or more tables.

</td></tr><tr><td>

Documentation URL

</td><td>

Documentation link for the check details.**Note:** A scan\_user can't edit the **Documentation URL** field.

</td></tr><tr><td>

Run Condition

</td><td>

Boolean field that determines if the check should be run.

</td></tr><tr><td>

Script

</td><td>

Option to write a custom script to generate findings.

</td></tr></tbody>
</table>
**Parent Topic:**[Create a check](hs-create-health-check.md)

