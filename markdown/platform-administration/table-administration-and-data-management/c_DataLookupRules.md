---
title: Data lookup rules
description: Data lookup rules offer a generic way to change any field value, not just assignment fields.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assignment rules, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data lookup rules

Data lookup rules offer a generic way to change any field value, not just assignment fields.

[Data lookup and record matching support](../../field-administration/concept/c_DataLookRecMatchSupport.md) offer the following improvements over the Assignment module:

-   Ability to change any field value not just an assignment field
-   More options to define when a rule runs:
    -   On form change \(Allows assignment rules to apply to unsaved changes on a form\)
    -   On record insert
    -   On record update
-   Option to replace existing values \(including default values\)

**Note:** You can define data lookup and Assignment rules at the same time. The system ignores any duplicate rules after an incident has been assigned unless you are using a data lookup definition option to replace existing values.

**Parent Topic:**[Defining assignment rules](c_DefineAssignmentRules.md)

**Related topics**  


[Assignment rules module](c_AssignmentRulesModule.md)

[Precedence between data lookup, assignment, and business rules](c_PrecBetweenAssignmentAndBusRules.md)

[Workflow assignments](c_WorkflowAssignments.md)

[Baseline assignment rules example](../reference/r_BaselineAssignmentRulesExample.md)

[Create an assignment rule](../task/t_AssignmentModuleRule.md)

[Create an assignment data lookup rule](../task/t_DataLookupRule.md)

[Precedence between data lookup, assignment, and business rules](c_PrecBetweenAssignmentAndBusRules.md)

