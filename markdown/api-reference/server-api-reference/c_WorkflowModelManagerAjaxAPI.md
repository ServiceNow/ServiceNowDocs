---
title: WorkflowModelManagerAjax - Global
description: The WorkflowModelManagerAjax script include provides an AjaxProcessor wrapper for the WorkflowModelManager script include. This class derives from AbstractAjaxProcessor.Puts the execution history into the return parameter based on the query string.DMB This seems to be missing some information. Fix.Returns the final execution activity list based on a query string.Puts the rollback activity list into the return parameter based on the query string.needs help
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# WorkflowModelManagerAjax- Global

The WorkflowModelManagerAjax script include provides an AjaxProcessor wrapper for the WorkflowModelManager script include. This class derives from AbstractAjaxProcessor.

Use this class in the Workflow Debug context menus.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## WorkflowModelManagerAjax - getExecutedHistory\( \)

Puts the execution history into the return parameter based on the query string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## WorkflowModelManagerAjax - getFinalExecutedActivityIdList\( \)

Returns the final execution activity list based on a query string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

This example shows how to obtain the sys\_ids of an executed activity list.

```
var model = new WorkflowModelManagerAjax(); // Initiate the class

  model.getParameter = function(paramName) {
    return {
       sysparm_key_id: "0213a4a607e0011094b4fe4f7c1ed0e2", // sys_id of workflow context
       sysparm_key_table: 'wf_context'
    }[paramName];
  } // Override the parameters while calling from server side

  model.getExecutedHistory();
  var finals = model.getFinalExecutedActivityIdList(); // Get the list of IDs
  finals = JSON.parse(finals);
  var finalarrofID = finals.ids;
    for ( var x = 0; x < finalarrofID .length; x++ ) {
      gs.print(JSON.stringify(finalarrofID[x]) ); // Print the sys_ids of workflow history records
    }
```

Output:

```
WorkflowModelManagerAjax: creating new WorkflowModelManager for context=0213a4a607e0011094b4fe4f7c1ed0e2
WorkflowModelManagerAjax: returning 4 ActivityHistoryRecords
WorkflowModelManagerAjax: returning 4 activities  in execution path for 0213a4a607e0011094b4fe4f7c1ed0e2
*** Script: "0a13a4a607e0011094b4fe4f7c1ed0e3"
*** Script: "d61368a607e0011094b4fe4f7c1ed027"
*** Script: "de1368a607e0011094b4fe4f7c1ed02b"
*** Script: "961368a607e0011094b4fe4f7c1ed02f"

```

## WorkflowModelManagerAjax - getRolledBackActivityIdList\( \)

Puts the rollback activity list into the return parameter based on the query string.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

