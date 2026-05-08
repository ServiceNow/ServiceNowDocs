---
title: ScriptableFlowRunner - Scoped
description: Creates a builder object used to define parameters for flow, subflow, and action execution. You can specify a flow to execute in a particular domain. Start the flow, subflow, or action execution directly from the builder and view the results in a ScriptableFlowRunnerResult object.Identifies the scope and name of the action to execute.Adds a single input. If the name passed as an argument already exists as a separate input, the new value replaces the pre-existing value.Runs flow as the user who triggered it, not the system, for quick background executions.Identifies the scope and name of the data stream action to execute.Identifies the scope and name of the flow to execute.Runs the flow, subflow, or action asynchronously. Once the flow object starts running, script execution resumes immediately.Runs the flow, subflow, or action in the specified domain. Checks to ensure the domain exists and is available.Runs the flow, subflow, or action synchronously. Script execution pauses while the flow object is running.Runs a flow, subflow, action, or Data Stream action from a server-side script synchronously or asynchronously without creating execution details or other related records. Improves performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.Runs the flow, subflow, or action with the specified parameters.Identifies the scope and name of the subflow to execute.Sets a timeout for a flow, subflow, or action execution.Throw an error and prevent the ScriptableFlowRunner class from running when any method input has an unexpected value. This method defaults to true for any ScriptableFlowRunner call.Overrides the Connections and Credentials alias associated with the flow, action, or subflow. You can override the default parent alias with any of its child aliases.Adds a collection of inputs. If a name in one of the name-value pairs already exists, the new value replaces the pre-existing value.Runs the flow as the user who triggered the flow or executes the flow with roles that have been added in Workflow Studio.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ScriptableFlowRunner- Scoped

Creates a builder object used to define parameters for flow, subflow, and action execution. You can specify a flow to execute in a particular domain. Start the flow, subflow, or action execution directly from the builder and view the results in a ScriptableFlowRunnerResult object.

Use these methods in your server-side scripts with the `sn_fd` namespace identifier.

## API call order

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

## ScriptableFlowRunner - action\(String scopedActionName\)

Identifies the scope and name of the action to execute.

See also:

-   [ScriptableFlowRunner - flow\(String scopedFlowName\)](ScriptableFlowRunnerScopedAPI.md#)
-   [ScriptableFlowRunner - subflow\(String scopedSubflowName\)](ScriptableFlowRunnerScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|scopedActionName|String|Scope and name of the action to execute. For example, `global.actionName`.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

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

## ScriptableFlowRunner - addInput\(String name, Object value\)

Adds a single input. If the name passed as an argument already exists as a separate input, the new value replaces the pre-existing value.

This method adds a single input. To create an object and add multiple inputs, use the withInputs\(\) method.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the input for the flow, subflow, or action.|
|value|Object|The value of the input for the flow, subflow, or action.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example runs an action that takes a single input called `table_name`.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .action('global.test_action')
      .addInput('table_name', 'incident')
      .inForeground()
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
Flow Designer: TableName
*** Script: FlowRunnerResult
Flow Object Name: global.test_action
Flow Object Type: action
Domain: null
Result Time: 2020-06-09 00:10:57
ContextId: null
Output count: 1
```

## ScriptableFlowRunner - asUser\(\)

Runs flow as the user who triggered it, not the system, for quick background executions.

When a flow is triggered using quick\(\) along with the asUser\(\) method, user who triggered the flow is retrieved and is used for the flow execution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner - Scoped](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to create a ScriptableFlowRunner builder object and uses it to execute an approval action on a specific record using asUser\(\) and quick\(\) methods. A ScriptableFlowRunnerResult object captures the execution arguments and action outputs.

```
(function() {
    try {

        var outputs = sn_fd.FlowAPI.getRunner() // Create a ScriptableFlowRunner builder object.
        .flow('global.stry53225960_flow_asuser_test')
        .inForeground()
        .quick() //Run the flow from a server-side script.
        .asUser() //Run flow with the roles specified in the flow.
        .run(); // Run the action and return a FlowRunnerResult object.

    } catch (ex) {
        var message = ex.getMessage();
        gs.error(message);
    }  

})();
```

### Errors

These errors may occur while using the asUser\(\) method:

-   Script returns an error when asUser\(\) not used along with quick\(\).
-   Script returns an error when asUser\(\) is called in a flow that has roles defined.
-   Script returns an error when withRoles\(\) and asUser\(\) methods are called at the same time.

## ScriptableFlowRunner - datastream\(String scopedDatastreamName\)

Identifies the scope and name of the data stream action to execute.

To learn more about data stream actions, see Data Stream actions and pagination.

|Name|Type|Description|
|----|----|-----------|
|scopedDatastreamName|String|Scope and name of the Data Stream action to execute. For example, `global.dataStreamActionName`.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to run a Data Stream action.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .datastream('global.test_dsa')
      .inForeground()
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
Flow Object Name: global.test_dsa
Flow Object Type: datastream
Domain: null
Result Time: 2020-06-08 16:41:13
ContextId: null
Output count: 0
```

## ScriptableFlowRunner - flow\(String scopedFlowName\)

Identifies the scope and name of the flow to execute.

See also:

-   [ScriptableFlowRunner - action\(String scopedActionName\)](ScriptableFlowRunnerScopedAPI.md#)
-   [ScriptableFlowRunner - subflow\(String scopedSubflowName\)](ScriptableFlowRunnerScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|scopedFlowName|String|Scope and name of the flow to execute. For example, `global.flowName`.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to run a flow that logs a message.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
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
Result Time: 2020-06-08 16:41:13
ContextId: null
Output count: 0
```

## ScriptableFlowRunner - inBackground\(\)

Runs the flow, subflow, or action asynchronously. Once the flow object starts running, script execution resumes immediately.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

**Note:** As of the Xanadu release, running an action, flow, or subflow in the background using the quick\(\) method returns an execution ID as the ContextId value. The execution ID is not an actual context record as no records are inserted into the Flow Context \[sys\_flow\_context\] table. Rather the execution ID is used to track the asynchronous call.

This example shows how to run a flow in the background asynchronously.

```
(function() {
    try {
  
      var result = sn_fd.FlowAPI.getRunner()
        .flow('global.change__unauthorized__review')
        .inBackground()
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

[0:00:01.015] Script completed in scope global: script
––––––––––––––––––––––––––––––––––––––––––––––––––––--
Script execution history and recovery available here
Operation       Table                               Row Count
insert          sys_flow_context_inputs_chunk       1
insert          sys_flow_context                    1
––––––––––––––––––––––––––––––––––––––––––––––––––––--
Complex type redefined: FlowDesigner:FDCollection
Queued flow.fire event in NowMQ for sys_flow_context.sys_id: e0cd6e30b8b602104a8752ad4a9167c8,
sysevent.sys_id: 34cd6e30dbb60210497c1a48139619c9, with priority 5
*** Script: FlowRunnerResult
Flow Object Name: global.change__unauthorized__review
Flow Object Type: flow
Domain: null
Result Time: 2024-06-12 17:54:58
ContextId: e0cd6e30b8b602104a8752ad4a9167c8
Output count: 0
```

## ScriptableFlowRunner - inDomain\(String domainId\)

Runs the flow, subflow, or action in the specified domain. Checks to ensure the domain exists and is available.

|Name|Type|Description|
|----|----|-----------|
|domainId|String|The sys\_id or name for the domain of execution for the flow.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

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

## ScriptableFlowRunner - inForeground\(\)

Runs the flow, subflow, or action synchronously. Script execution pauses while the flow object is running.

**Note:** This method does not support pausing the action to wait for conditions. Steps that pause for wait conditions such as Ask for Approval or Wait for Condition are not supported.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

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

## ScriptableFlowRunner - quick\(\)

Runs a flow, subflow, action, or Data Stream action from a server-side script synchronously or asynchronously without creating execution details or other related records. Improves performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Wait condition support**

    This method does not support pausing an action or flow to wait for conditions. Actions, flow logic, and steps that pause for wait conditions such as Ask for Approval, Wait for Condition, or Wait for a duration are not supported.

-   **MID Server support**

    This method does not support pausing an action or flow to run from a MID Server. This restriction includes data stream action preprocessing scripts that pause an action to run from a MID Server.

-   **Data stream action support**

    This method does not support pausing a data stream action to run a preprocessing script from a MID Server.

-   **Flow priority support**

    This method supports flow priority settings. The flow runs at the specified flow priority.


|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

**Note:** As of the Xanadu release, running an action, flow, or subflow in the background using the quick\(\) method returns an execution ID as the ContextId value. The execution ID is not an actual context record as no records are inserted into the Flow Context \[sys\_flow\_context\] table. Rather the execution ID is used to track the asynchronous call.

This example shows how to run a flow without creating any related records.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.change__unauthorized__review')
      .inBackground()
      .quick()
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

Complex type redefined: FlowDesigner:FDCollection
Queued flow.run.quick event in NowMQ for sys_flow_context.sys_id: d81781ec57801110403e8f90ac94f90e,
sysevent.sys_id: 48abe270dbf20210497c1a4813961908, with priority 5
*** Script: FlowRunnerResult
Flow Object Name: global.change__unauthorized__review
Flow Object Type: flow
Domain: null
Result Time: 2024-06-12 17:45:37
ContextId: 08abe2706cf202107b7d3b283f7ee108
Output count: 0
```

## ScriptableFlowRunner - run\(\)

Runs the flow, subflow, or action with the specified parameters.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ScriptableFlowRunnerResultsScoped|Object containing the execution details of a Workflow Studio action, flow, or subflow.|

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

## ScriptableFlowRunner - subflow\(String scopedSubflowName\)

Identifies the scope and name of the subflow to execute.

See also:

-   [ScriptableFlowRunner - action\(String scopedActionName\)](ScriptableFlowRunnerScopedAPI.md#)
-   [ScriptableFlowRunner - flow\(String scopedFlowName\)](ScriptableFlowRunnerScopedAPI.md#)

|Name|Type|Description|
|----|----|-----------|
|scopedSubflowName|String|Scope and name of the subflow to execute. For example, `global.subflowName`.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to run a subflow that logs a message.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .subflow('global.output_test')
      .inForeground()
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
record-watcher asynchronous tracking complete - time: 1 ms. Executed responders: 1 
record-watcher asynchronous tracking complete - time: 1 ms. Executed responders: 1 
*** Script: FlowRunnerResult
Flow Object Name: global.output_test
Flow Object Type: subflow
Domain: null
Result Time: 2024-08-02 22:52:08
ContextId: b2dxx659bebf01101d72200x503x19pr
Output count: 2
```

## ScriptableFlowRunner - timeout\(Number timeout\)

Sets a timeout for a flow, subflow, or action execution.

|Name|Type|Description|
|----|----|-----------|
|timeout|Number|Timeout in milliseconds.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to run a flow and sets a timeout for two minutes.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .timeout(120000)
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
Flow Designer: Cloning a new session to run as as user id: [user_name] from original user session: [user_name]
Flow Designer: Reverting cloned session to original user session: [user_name]
*** Script: FlowRunnerResult
Flow Object Name: global.test_flow
Flow Object Type: flow
Domain: null
Result Time: 2020-06-08 18:22:35
ContextId: null
Output count: 0
```

## ScriptableFlowRunner - validateInputs\(Boolean validateInputs\)

Throw an error and prevent the ScriptableFlowRunner class from running when any method input has an unexpected value. This method defaults to true for any ScriptableFlowRunner call.

<table id="table_vmh_2yp_rwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

validateInputs

</td><td>

Boolean

</td><td>

Flag that indicates whether to validate ScriptableFlowRunner method inputs.There are two valid values.

-   true: Throw an error when inputs have unexpected values and stop running the script.
-   false: Allow the script to run with unexpected values.

Default: True

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to run a flow without validating the method input values.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .inForeground()
      .validateInputs(false)
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
Result Time: 2020-06-08 16:41:13
ContextId: null
Output count: 0
```

## ScriptableFlowRunner - withConnectionAliasOverride\(String aliasName, String overrideName\)

Overrides the Connections and Credentials alias associated with the flow, action, or subflow. You can override the default parent alias with any of its child aliases.

To learn more about overriding a Connections and Credentials alias, see Supporting multiple connections.

|Name|Type|Description|
|----|----|-----------|
|parentAliasSysID|String|The sys\_id of the parent alias, the alias you want to override.|
|overrideAliasSysID|String|The sys\_id of the child alias, the alias you want to use when running the flow, subflow, or action.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to run a flow using a different alias than the default associated with the flow.

```
(function() {
  try {

    var result = sn_fd.FlowAPI.getRunner()
      .flow('global.test_flow')
      .withConnectionAliasOverride('sn_original_alias.spoke', 'x_new_alias.spoke')
      .inForeground()
      .run();

    gs.info(result.debug());

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

## ScriptableFlowRunner - withInputs\(Map inputs\)

Adds a collection of inputs. If a name in one of the name-value pairs already exists, the new value replaces the pre-existing value.

|Name|Type|Description|
|----|----|-----------|
|inputs|Object|Map object containing the name-value pairs that define inputs for the flow, subflow, or action.|

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

Creates an input object and passes the value to the withInputs\(\) method.

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

## ScriptableFlowRunner - withRoles\(\)

Runs the flow as the user who triggered the flow or executes the flow with roles that have been added in Workflow Studio.

When a flow is triggered using quick\(\) along with the withRoles\(\) method, roles defined in the flow properties are retrieved, passed during the flow execution, and the flow is run with the roles.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner - Scoped](ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example shows how to create a ScriptableFlowRunner builder object and uses it to execute an approval action on a specific record using withRoles\(\) and quick\(\) methods. A ScriptableFlowRunnerResult object captures the execution arguments and action outputs.

```
(function() {
    try {

        var outputs = sn_fd.FlowAPI.getRunner() // Create a ScriptableFlowRunner builder object.
        .flow('global.stry53225960_flow')
        .inForeground()
        .quick() //Run the flow from a server-side script.
        .withRoles() //Run the flow as the user who triggered the flow.
        .run(); // Run the action and return a FlowRunnerResult object.

    } catch (ex) {
        var message = ex.getMessage();
        gs.error(message);

    }  

})();
```

### Errors

These errors may occur while using the withRoles\(\) method:

-   withRoles\(\) performs no operation if it is not used along with quick\(\).
-   Script returns an error when withRoles\(\) is called in a flow that doesn't have any roles.
-   Script returns an error when withRoles\(\) and asUser\(\) methods are called at the same time.

