---
title: Return Value workflow activity
description: The Return Value activity returns a value to a parent workflow, when run from a subflow.
locale: en-US
release: zurich
product: Workflow Activities
classification: workflow-activities
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Utility workflow activities, Workflow activities reference, Workflow activities, Classic Workflow, Build workflows]
---

# Return Value workflow activity

The **Return Value** activity returns a value to a parent workflow, when run from a subflow.

This activity has no variables or conditions. For more information, see [Workflows used as subflows](workflows-as-subflows.md).

Use this activity within a subflow to store data that the parent flow can access. The **Return Value** activity adds the data from the subflow's *value* variable to the parent workflow's [scratchpad](../../using-workflows/concept/c_UsingVariablesInAWorkflow.md#).

## Scratchpad entries

The activity uses the workflow scratchpad to read and write persistent values.

|Variable|Description|
|--------|-----------|
|value|The activity writes the value from the subflow *value* variable to the parent scratchpad. The parent workflow activity that runs the subflow includes a *Map return value to* variable that defines where the parent workflow stores the returned data. This data can be scalar, a stringifiable JavaScript object, or an expression that evaluates to a stringifiable JavaScript object.|

**Related topics**  


[Workflow scratchpad variables](../../using-workflows/concept/c_UsingVariablesInAWorkflow.md#)

[Using variables in a workflow](../../using-workflows/concept/c_UsingVariablesInAWorkflow.md#)

