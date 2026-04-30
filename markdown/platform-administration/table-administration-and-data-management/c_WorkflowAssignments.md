---
title: Workflow assignments
description: An alternative to creating data lookup or assignment rules is to create one or more workflow tasks that assign a task record as part of a workflow.
locale: en-US
release: yokohama
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Assignment rules, Work with the Task table, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Workflow assignments

An alternative to creating data lookup or assignment rules is to create one or more workflow tasks that assign a task record as part of a workflow.

Consider using [Task workflow activities](https://www.servicenow.com/docs/access?context=r_TaskActivities&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for assignment if your process includes multiple steps or conditions such as requiring a particular group approve a request.

When using a workflow to manage task assignments, add a brief [Timer workflow activity](https://www.servicenow.com/docs/access?context=r_Timer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) to the start of the workflow. Without this timer activity, the workflow runs before the parent record, the current record, is inserted into the database. After the timer activity completes, the workflow resumes using the parent record information from the database instead of the original current. Pausing a workflow in this way does not change a default workflow to a deferred workflow. For more information on how the workflow engine interacts with the database, see [Workflow engine operation order](https://www.servicenow.com/docs/access?context=c_WorkflowEngineOperationOrder&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Parent Topic:**[Defining assignment rules](c_DefineAssignmentRules.md)

**Related topics**  


[Assignment rules module](c_AssignmentRulesModule.md)

[Data lookup rules](c_DataLookupRules.md)

[Precedence between data lookup, assignment, and business rules](c_PrecBetweenAssignmentAndBusRules.md)

[Baseline assignment rules example](../reference/r_BaselineAssignmentRulesExample.md)

[Create an assignment rule](../task/t_AssignmentModuleRule.md)

[Create an assignment data lookup rule](../task/t_DataLookupRule.md)

