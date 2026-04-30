---
title: DevOps work item import for Azure Boards
description: Azure Boards work items are mapped to default ServiceNow DevOps states and types during import. You can use the DevOpsAzureDevOpsWorkItemHelper script include to customize the mappings.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# DevOps work item import for Azure Boards

Azure Boards work items are mapped to default ServiceNow DevOps states and types during import. You can use the DevOpsAzureDevOpsWorkItemHelper script include to customize the mappings.

## Default Azure Boards work item mapping

**Native State** and **Native Type** fields of the work item contain the original state and type values from the source tool.

<table id="table_rnv_ssx_glb"><thead><tr><th>

ServiceNow DevOps

</th><th>

Azure Boards Basic

</th><th>

Azure Boards Agile

</th><th>

Azure Boards Scrum

</th></tr></thead><tbody><tr><td>

Task

</td><td>

Task

</td><td>

Task

 Test case

</td><td>

Task

 Impediment

 Test case

</td></tr><tr><td>

Bug

</td><td>

Issue

</td><td>

Bug

 Issue

</td><td>

Bug

</td></tr><tr><td>

Story

</td><td>

--

</td><td>

User story

</td><td>

Product backlog item

</td></tr><tr><td>

Epic

</td><td>

Epic

</td><td>

Epic

</td><td>

Epic

</td></tr><tr><td>

Feature

</td><td>

--

</td><td>

Feature

</td><td>

Feature

</td></tr></tbody>
</table>**Note:** Historical import of Azure DevOps work items is not supported for Agile Boards CMMI process.

<table id="table_r41_4k2_vlb"><thead><tr><th>

ServiceNow DevOps

</th><th>

Azure Boards Basic

</th><th>

Azure Boards Agile

</th><th>

Azure Boards Scrum

</th></tr></thead><tbody><tr><td>

Planned

</td><td>

To Do

</td><td>

New

</td><td>

New

 Open

 Approved

 Committed

 To do

</td></tr><tr><td>

WIP

</td><td>

Doing

</td><td>

Active

 Design

</td><td>

In Progress

 Design

</td></tr><tr><td>

Complete

</td><td>

Done

</td><td>

Ready

 Closed

</td><td>

Done

 Ready

 Closed

</td></tr><tr><td>

Deleted

</td><td>

Deleted

</td><td>

Completed

 Deleted

</td><td>

Removed

</td></tr></tbody>
</table>**Note:** When an imported Azure Boards work item type or state is not recognized, the value is set to **Other**.

## Customize Azure Boards state and type mappings

Access the DevOpsAzureDevOpsWorkItemHelper script include in the **System Definition** &gt; **Script Includes** module.

This script example adds new states and types for custom processes MyScrum and CustomBasic. CustomBasic inherits the state and type defined for Basic process.

```
var DevOpsAzureDevOpsWorkItemHelper = Class.create();

DevOpsAzureDevOpsWorkItemHelper.prototype = Object.extendsObject(DevOpsAzureDevOpsWorkItemHelperSNC, {
	
	setDefaultProcess: function (projectProcess){
		
		DevOpsAzureDevOpsWorkItemHelperSNC.prototype.setDefaultProcess.call(this, projectProcess);
		
		//set custom states and types
		var newStates, newWITypes;
		if (projectProcess == 'NPScrum'){
			// no parent process set. So type and states avaibale will be linited to newStates
			// and newWITypes
			newStates = {
				'Delayed': 'planned',
				'Approved': 'wip'
			};
			newWITypes= {
				'Request': 'story',
				'Incident': 'task'
			};
			
		} else  if (projectProcess == 'CustomBasic'){
			//set parent process to Basic to inherit basic states and types
			this.setParentProcess('Basic');
			newStates = {
				'Auto-Approved': 'wip'
			};
			newWITypes= {
				'UserStory': 'story'
			};
		}
		
		this.setStates(newStates);
        this.setWorkItemTypes(newWITypes);
	},
	
	type: 'DevOpsAzureDevOpsWorkItemHelper'
});
```

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

