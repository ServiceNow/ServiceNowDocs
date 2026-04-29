---
title: Assignment rules module
description: The Assignment rules module allows you to automatically set a value in the assigned\_to and assignment\_group fields when a set of conditions occurs.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assignment rules, Working with Task table, Table admin, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Assignment rules module

The Assignment rules module allows you to automatically set a value in the assigned\_to and assignment\_group fields when a set of conditions occurs.

An assignment rule must also meet these additional criteria to run:

-   The task record has been created or updated. Assignment rules do not apply to unsaved changes on a form.
-   The task record must be unassigned. The record cannot have an existing value for either the assigned\_to or assignment\_group fields. Assignment rules cannot overwrite existing assignments \(including assignments set by a default value or a previously run assignment rule\).
-   The assignment rule is the first rule that matches the table and conditions. If more than one assignment rule matches the conditions, only the rule with the lowest order value runs.

**Parent Topic:**[Defining assignment rules](c_DefineAssignmentRules.md)

**Related topics**  


[Data lookup rules](c_DataLookupRules.md)

[Precedence between data lookup, assignment, and business rules](c_PrecBetweenAssignmentAndBusRules.md)

[Workflow assignments](c_WorkflowAssignments.md)

[Baseline assignment rules example](../reference/r_BaselineAssignmentRulesExample.md)

[Create an assignment rule](../task/t_AssignmentModuleRule.md)

[Create an assignment data lookup rule](../task/t_DataLookupRule.md)

