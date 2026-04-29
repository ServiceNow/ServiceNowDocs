---
title: Create a column type check
description: Retrieve all records containing a specific column field type from all tables in an instance by selecting Create a new Column Type Check. The Column Type Check type implements the rule you created to iterate all records matching the target column field type.
locale: en-US
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a check, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Create a column type check

Retrieve all records containing a specific column field type from all tables in an instance by selecting **Create a new Column Type Check**. The **Column Type Check** type implements the rule you created to iterate all records matching the target column field type.

## Before you begin

Role required: scan\_admin

```
Before performing this task you must complete [Create a check](hs-create-health-check.md).
```

## Procedure

1.  Select **Create a new Column Type Check**.

    A New record form appears.

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

Column Type

</td><td>

Column type queried for this check.

</td></tr><tr><td>

Documentation URL

</td><td>

Documentation link for the check details.**Note:** A scan\_user can't edit the **Documentation URL** field.

</td></tr><tr><td>

Run Condition

</td><td>

Boolean field that determines if the check should be run.

</td></tr><tr><td>

Column Type

</td><td>

Type of columns that will run.

</td></tr><tr><td>

Script

</td><td>

Script that executes against each record in a table containing a field of the defined column type.

</td></tr></tbody>
</table>
**Parent Topic:**[Create a check](hs-create-health-check.md)

