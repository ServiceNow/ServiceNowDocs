---
title: CostPlanBatchOperations - Global
description: The CostPlanBatchOperations script include provides methods that enable the creation of a large number of cost plan records for demands and projects using batch processing. Use this script include instead of GlideRecord to more efficiently create multiple cost plan records.Adds one or more cost plans to a specified task \(project or demand\). Use this method when you want to create multiple cost plans.Removes all cost plan objects that were added using the CostPlanBatchOperations.add\(\) method.Processes all of the cost plans that were added using the CostPlanBatchOperations.add\(\) method and creates corresponding cost plans and relevant rollups.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CostPlanBatchOperations- Global

The CostPlanBatchOperations script include provides methods that enable the creation of a large number of cost plan records for demands and projects using batch processing. Use this script include instead of GlideRecord to more efficiently create multiple cost plan records.

Use the CostPlanBatchOperations.add\(\) method to add any number of cost plans to a batch queue. Once you have added all the required cost plans, use the CostPlanBatchOperations.process\(\) method to create/insert the cost plans in your instance. Until you call the CostPlanBatchOperations.process\(\) method, the add requests remain in the batch queue \(they are not yet added to your instance\). If for some reason you need to remove all of the cost plans in the batch queue, use the CostPlanBatchOperations.clear\(\) method.

To use this script include you must activate the PPM Standard \(com.snc.financial\_planning\_pmo\) plugin.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CostPlanBatchOperations - add\(Object costPlan\)

Adds one or more cost plans to a specified task \(project or demand\). Use this method when you want to create multiple cost plans.

Once processed, the cost plans are inserted into the specified project or demand. You can then view and modify them within your instance. For additional information, see [Create a project cost plan](https://www.servicenow.com/docs/access?context=t_CreateAProjectCostPlan&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) and [Create a demand cost plan](https://www.servicenow.com/docs/access?context=t_CreateADemandCostPlan&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

**Note:** This method only defines the cost plans to add to your instance. The cost plans are not inserted into your instance until the costPlanBatchOperations.process\(\) is called.

<table id="table_ebg_mhf_kjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

costPlan

</td><td>

Object

</td><td>

One or more objects or an array of objects that describe each of the cost plans to add to an existing task.

</td></tr><tr><td>

costPlan.name

</td><td>

String

</td><td>

Name of the cost plan.Maximum length: 130 characters

</td></tr><tr><td>

costPlan.task

</td><td>

String

</td><td>

Sys\_id of the project or demand to associate with this cost plan. You can locate this value in one of the following tables:-   Project \[pm\_project\]
-   Project Task \[pm\_project\_task\]
-   Demand \[dmn\_demand\]

</td></tr><tr><td>

costPlan.unit\_cost

</td><td>

Number

</td><td>

Cost of a single unit of the specified resource.

</td></tr><tr><td>

costPlan.resource\_type

</td><td>

String

</td><td>

Sys\_id of the record that defines the cost type associated with this cost plan. The available values for this parameter are defined in the Cost Type Definition \[resource\_type\_definition\] table.

</td></tr><tr><td>

costPlan.start\_fiscal\_period

</td><td>

String

</td><td>

Sys\_id of the record that defines the starting fiscal period to associate with this cost plan. The available values for this parameter are defined in the Fiscal period \[fiscal\_period\] table.

</td></tr><tr><td>

costPlan.end\_fiscal\_period

</td><td>

String

</td><td>

Sys\_id of the record that defines the ending fiscal period to associate with this cost plan. The available values for this parameter are defined in the Fiscal period \[fiscal\_period\] table.

</td></tr><tr><td>

costPlan.&lt;optional&gt;

</td><td>

Varied

</td><td>

Optional. You can pass in additional parameters to add to a cost plan. The available parameters depend on the type of cost plan that you are creating.Refer to the Cost Plan \[cost\_plan\] table for the list of additional parameters that you can pass.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example shows how to add a simple batched cost plan.

```
//Define Array of Cost Plan records in JSON format
var costPlanRecords= [];
costPlanRecords.push({
   name:'Capital Expense',
   task:'f7a36d1bdb58001025c85a35dc96193a', // sys_id of the task
   unit_cost:1000.00, //decimal 
   resource_type:'a546eaf79330120064f572edb67ffb70', // sys_id of the cost type definition
   start_fiscal_period:'091b6e60cb111200f2de77a4634c9c2e', // sys_id of the start fiscal period record 
   end_fiscal_period:'0d1b6e60cb111200f2de77a4634c9c2f',// sys_id of the end fiscal period record 
   quantity:1 // Optional cost plan record attributes
});
 
var costPlanBatchOperations = new CostPlanBatchOperations();
costPlanBatchOperations.add(costPlanRecords);
var costPlanSysIds = costPlanBatchOperations.process();


```

## CostPlanBatchOperations - clear\(\)

Removes all cost plan objects that were added using the CostPlanBatchOperations.add\(\) method.

**Note:** This method only works for cost plans that have been added. Once a cost plan is processed, this method cannot remove it. Processed cost plans must be removed manually through the UI.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to clear the batch queue after adding cost plans.

```
//Define Array of Cost Plan records in JSON format
var costPlanRecords= [];
costPlanRecords.push({
   name:'Capital Expense',
   task:'f7a36d1bdb58001025c85a35dc96193a', // sys_id of the task
   unit_cost:1000.00, //decimal 
   resource_type:'a546eaf79330120064f572edb67ffb70', // sys_id of the cost type definition
   start_fiscal_period:'091b6e60cb111200f2de77a4634c9c2e', // sys_id of the start fiscal period record 
   end_fiscal_period:'0d1b6e60cb111200f2de77a4634c9c2f',// sys_id of the end fiscal period record 
   quantity:1 // Optional cost plan record attributes
});
 
var costPlanBatchOperations = new CostPlanBatchOperations();
costPlanBatchOperations.add(costPlanRecords);
var costPlanSysIds = costPlanBatchOperations.process();
costPlanBatchOperations.clear();
```

## CostPlanBatchOperations - process\(\)

Processes all of the cost plans that were added using the CostPlanBatchOperations.add\(\) method and creates corresponding cost plans and relevant rollups.

Once the cost plans are successfully processed, the cost plan queue is cleared.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Sys ID for each generated cost plan.|

This example shows how to process a simple batched cost plan.

```
//Define Array of Cost Plan records in JSON format
var costPlanRecords= [];
costPlanRecords.push({
   name:'Capital Expense',
   task:'f7a36d1bdb58001025c85a35dc96193a', // sys_id of the task
   unit_cost:1000.00, //decimal 
   resource_type:'a546eaf79330120064f572edb67ffb70', // sys_id of the cost type definition
   start_fiscal_period:'091b6e60cb111200f2de77a4634c9c2e', // sys_id of the start fiscal period record 
   end_fiscal_period:'0d1b6e60cb111200f2de77a4634c9c2f',// sys_id of the end fiscal period record 
   quantity:1 // Optional cost plan record attributes
});
 
var costPlanBatchOperations = new CostPlanBatchOperations();
costPlanBatchOperations.add(costPlanRecords);
var costPlanSysIds = costPlanBatchOperations.process();


```

