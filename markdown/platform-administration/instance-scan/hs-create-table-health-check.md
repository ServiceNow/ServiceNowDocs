---
title: Create a table type check
description: Create a check by selecting Create a new Table Check if you know which specific table and conditions you want to test. This check type is applied on only one table at a time. You can also include your own script for more complex capabilities by selecting the Advanced option on the form.
locale: en-US
release: yokohama
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a check, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Create a table type check

Create a check by selecting **Create a new Table Check** if you know which specific table and conditions you want to test. This check type is applied on only one table at a time. You can also include your own script for more complex capabilities by selecting the **Advanced** option on the form.

## Before you begin

Role required: scan\_admin

```
Before performing this task you must complete [Create a check](hs-create-health-check.md).
```

## Procedure

1.  Select **Create a new Table Check**.

2.  On the form, fill in the fields.

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

Table

</td><td>

Table queried for this check.

</td></tr><tr><td>

Conditions

</td><td>

Conditions that filter records on a table. Only the records that meet the criteria are scanned.

</td></tr><tr><td>

Advanced

</td><td>

Option to execute the defined script against each record that matches the condition and control when a finding is generated if **Advanced** is true. If **Advanced** is false, a finding is generated for every record that matches the condition in the defined table.

</td></tr><tr><td>

Documentation URL

</td><td>

Documentation link for the check details.**Note:** A scan\_user can't edit the **Documentation URL** field.

</td></tr><tr><td>

Run Condition

</td><td>

Boolean field that determines if the check should be run.

</td></tr><tr><td>

Table

</td><td>

Table from which records will be scanned

</td></tr><tr><td>

Conditions

</td><td>

Conditions that determine which records will run

</td></tr><tr><td>

Script

</td><td>

The script that executes against each record that matches the condition in the defined table.**Note:** This field shows up only if the **Advanced** check box is selected.

</td></tr></tbody>
</table>
**Parent Topic:**[Create a check](hs-create-health-check.md)

