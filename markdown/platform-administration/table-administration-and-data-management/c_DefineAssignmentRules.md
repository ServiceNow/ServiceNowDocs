---
title: Defining assignment rules
description: The instance can automatically assign a task to a user or group based on pre-defined conditions by using data lookup rules and assignment rules.
locale: en-US
release: zurich
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with Task table, Table admin, Tables and data, Configure core features, Administer]
---

# Defining assignment rules

The instance can automatically assign a task to a user or group based on pre-defined conditions by using data lookup rules and assignment rules.

-   **[Assignment rules module](c_AssignmentRulesModule.md)**  
The Assignment rules module allows you to automatically set a value in the assigned\_to and assignment\_group fields when a set of conditions occurs.
-   **[Data lookup rules](c_DataLookupRules.md)**  
Data lookup rules offer a generic way to change any field value, not just assignment fields.
-   **[Precedence between data lookup, assignment, and business rules](c_PrecBetweenAssignmentAndBusRules.md)**  
Scripts, assignment rules, business rules, workflows, escalations, and engines all take effect in relation to a database operation, such as insert or update. In many cases, the order of these events is important.
-   **[Workflow assignments](c_WorkflowAssignments.md)**  
An alternative to creating data lookup or assignment rules is to create one or more workflow tasks that assign a task record as part of a workflow.
-   **[Baseline assignment rules example](../reference/r_BaselineAssignmentRulesExample.md)**  
A baseline instance contains certain assignment rules.
-   **[Create an assignment rule](../task/t_AssignmentModuleRule.md)**  
Automatically assign a record according to one or more conditions in an assignment rule. Assignment rules are designed to run at the time you open a record.
-   **[Create an assignment data lookup rule](../task/t_DataLookupRule.md)**  
Automatically assign a record using Data Lookup and Record Matching.

**Parent Topic:**[Working with the Task table](c_TaskTable.md)

