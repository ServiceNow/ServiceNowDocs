---
title: ScriptableFlowRunnerResult - Scoped
description: Captures the result of using ScriptableFlowRunner to execute a flow, subflow, or action. Includes data such as the context ID, domain, and any outputs from the flow execution.Returns information about the executed flow, subflow, or action, including the context ID, domain ID, and execution outputs.Returns the context ID of the flow, subflow, or action.Returns the date and time when a Workflow Studio action, flow, or subflow ran as a GlideDateTime object.Returns the stream of data from a data stream action.Returns the sys\_id of the domain that the Workflow Studio action, flow, or subflow ran in.Returns the type of Workflow Studio object run.Returns the scope and internal name of the Workflow Studio action, flow, or subflow run.Returns the outputs of a completed Workflow Studio action, flow, or subflow.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ScriptableFlowRunnerResult- Scoped

Captures the result of using ScriptableFlowRunner to execute a flow, subflow, or action. Includes data such as the context ID, domain, and any outputs from the flow execution.

Use these methods in your server-side scripts with the `sn_fd` namespace identifier.

## API call Order

Build and execute flows, subflows, and actions using these APIs in the following order:

-   **1. FlowAPI: Creates a builder object**

    Use getRunner\(\) to instantiate the ScriptableFlowRunner builder object.

-   **2. ScriptableFlowRunner: Specify Workflow Studio content to run**

    Use these methods in the following order to create the builder pattern:

    1.  Use one of the methods action\(\), datastream\(\), flow\(\), or subflow\(\) to specify what type of Workflow Studio object to build.
    2.  Use one or more methods such as addInput\(\), inDomain\(\), or quick\(\) to specify execution parameters.
    3.  Use the run\(\) method to run the action, flow, or subflow with the provided parameters and return a ScriptableFlowRunnerResult object.
-   **3. ScriptableFlowRunnerResult: Retrieve Workflow Studio execution details**

    Use one or more methods such as getContextId\(\), getOutputs\(\), and getDomainId\(\) to view execution details.


## Example

This example shows how to create a ScriptableFlowRunner builder object and uses it to execute an approval action on a specific record. A ScriptableFlowRunnerResult object captures the execution arguments and action outputs.

```

(function() {
  try {

    var inputs = {}; 

    inputs['sys_id'] = '57af7aec73d423002728660c4cf6a71c';  // Pass the record's sys_id in as input.  

    var result = sn_fd.FlowAPI.getRunner()  // Create a ScriptableFlowRunner builder object.
      .action('global.markapproved')        // Run the global scope action named markapproved.
      .inForeground()
      .inDomain('TOP/ACME')                 // Run the action from the TOP/ACME domain.                               
      .withInputs(inputs)
      .run();                               // Run the action and return a FlowRunnerResult object.

    var contextId = result.getContextId();  // Retrieve the context ID from the result
    var dateRun = result.getDate();
    var domainUsed = result.getDomainId();  // Retrieve the Domain ID from the result.
    var flowName = result.getFlowObjectName();
    var flowObjectType = result.getFlowObjectType();

    var outputs = result.getOutputs();            // Retrieve any outputs from the action execution.
    var newApprovalStatus = outputs['approval'];  // Echo back the approval status for verification.
		
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
	
})();
   
```

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ScriptableFlowRunnerResult - debug\(\)

Returns information about the executed flow, subflow, or action, including the context ID, domain ID, and execution outputs.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_iys_1v5_rlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Execution details about the Workflow Studio action, flow, or subflow run.-   flow object name: Name of the flow, subflow, or action.
-   flow object type: Flow, subflow, action, or datastream action.
-   domain ID: ID of the domain that the flow, subflow, or action ran in.
-   result time: Amount of time it took to run.
-   context ID: Sys\_id of the Workflow Studio execution details record for the action, flow, or subflow.
-   output count: Number of action or subflow outputs.

</td></tr></tbody>
</table>This example shows how to retrieve information about the executed flow, subflow, or action from the ScriptableFlowRunnerResult object.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .timeout(12000)
      .run();

    gs.info(result.debug());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

Output:

```
*** Script: FlowRunnerResult
Flow Object Name: global.test_flow
Flow Object Type: flow
Domain: null
Result Time: 2020-06-08 18:28:41
ContextId: null
Output count: 0

```

## ScriptableFlowRunnerResult - getContextId\(\)

Returns the context ID of the flow, subflow, or action.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the Workflow Studio execution details record for the action, flow, or subflow.|

This example shows how to retrieve a context ID from a ScriptableFlowRunnerResult object.

```
var contextId = result.getContextId();
```

Output:

```
4ecead85c4da1110598d0c7d6bf73554
```

## ScriptableFlowRunnerResult - getDate\(\)

Returns the date and time when a Workflow Studio action, flow, or subflow ran as a GlideDateTime object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideDateTime|The execution date and time for the flow, subflow, or action.|

This example shows how to retrieve the date and time of a flow execution from a ScriptableFlowRunnerResult object.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .timeout(12000)
      .run();

    gs.info(result.getDate());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

Output:

```
2020-05-22 18:45:42
```

## ScriptableFlowRunnerResult - getDataStream\(\)

Returns the stream of data from a data stream action.

If the datastream\(\) method was used in the ScriptableFlowRunner builder class, this returns the stream of data as a ScriptableDataStream object. Use the ScriptableDataStream class to iterate over items in the stream. See [ScriptableDataStream](../../ScriptableDataStream/concept/ScriptableDataStreamAPI.md#).

For more information about data stream actions, see [Data Stream actions and pagination](https://www.servicenow.com/docs/access?context=data-stream-actions&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ScriptableDataStream|A ScriptableDataStream object you can use to iterate through items in a data stream. Use the methods in the ScriptableDataStream class to interact with this object. See [ScriptableDataStream](../../ScriptableDataStream/concept/ScriptableDataStreamAPI.md#).|

This example shows how to retrieve a data stream from a ScriptableFlowRunnerResult object.

```
var datastream = result.getDataStream();
```

## ScriptableFlowRunnerResult - getDomainId\(\)

Returns the sys\_id of the domain that the Workflow Studio action, flow, or subflow ran in.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The sys\_id of the domain that the Workflow Studio action, flow, or subflow ran in.|

This example shows how to retrieve a domain ID from a ScriptableFlowRunnerResult object.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .inDomain('TOP/ACME')
      .timeout(12000)
      .run();

    gs.info(result.getDomainId());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

Output:

```
4ecead85a4da1110598d0c7d6bf75554
```

## ScriptableFlowRunnerResult - getFlowObjectType\(\)

Returns the type of Workflow Studio object run.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|FlowObjectType|The type of Workflow Studio object run, which is either action, flow, or subflow.|

This example shows how to retrieve the flow object type from the ScriptableFlowRunnerResult API.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .timeout(12000)
      .run();

    gs.info(result.getFlowObjectType());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

Output:

```
flow
```

## ScriptableFlowRunnerResult - getFlowObjectName\(\)

Returns the scope and internal name of the Workflow Studio action, flow, or subflow run.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The scope and internal name of the Workflow Studio action, flow, or subflow run. For example, `global.emailflow`.|

This example shows how to retrieve the name of the flow, subflow, or action name from a ScriptableFlowRunnerResult object.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .timeout(12000)
      .run();

    gs.info(result.getFlowObjectName());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

Output:

```
global.test_flow
```

## ScriptableFlowRunnerResult - getOutputs\(\)

Returns the outputs of a completed Workflow Studio action, flow, or subflow.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object containing the output of a completed Workflow Studio action, flow, or subflow.|

This example shows how to retrieve the outputs from a Workflow Studio action, flow, or subflow run with the ScriptableFlowRunner API.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .action('global.test_action')
      .inForeground()
      .timeout(12000)
      .run();

    gs.info(result.getOutputs());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

Output:

```
Flow Designer: Warning. This is an important log message. 
```

