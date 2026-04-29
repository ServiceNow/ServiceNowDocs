---
title: Create a linter check
description: Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.
locale: en-US
release: australia
product: Instance Scan
classification: instance-scan
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a check, Using Instance Scan, Instance Scan, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Create a linter check

Create a linter check to identify any issues in a script. When a linter check is run on a record, an abstract syntax tree for its code is generated. You can use the abstract syntax tree to analyze issues with the code.

## Before you begin

Role required: scan\_admin.

```
Before performing this task you must complete [Create a check](hs-create-health-check.md).
```

## Procedure

1.  Select **Create a new Linter Check**.

2.  On the form, fill in the fields.

<table id="table_rrj_m3k_gnb"><thead><tr><th>

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

The script that executes against each record that matches the condition. By default, this field has an engine object to use. This engine object contains other objects like `engine.finding` which you can call `engine.finding.increment()` to manually increment the **Count** field on that specific finding. Another object is `engine.current` which is the current GlideRecord that the check would be viewing when running.**Note:** This is new to Quebec release, where previously you would call `finding` and `current` directly.

</td></tr></tbody>
</table>
-   **[Advanced linter check scripts](../concept/hs-linter-check-scripts.md)**  
Linter check scripts helps you in writing checks that look for issues in scripts. When a linter check is run on a record, it provides an abstract syntax tree for its code. You can use this abstract syntax tree to analyze issues with the code such as too many nested if statements or usages of slow API in a while loop.

**Parent Topic:**[Create a check](hs-create-health-check.md)

