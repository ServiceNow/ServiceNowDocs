---
title: FlowAPI - Scoped, Global
description: The FlowAPI provides methods to execute actions, flows, or subflows in server-side scripts using either blocking or non-blocking methods.Cancels a paused or running flow, subflow, or action.Runs an action from a server-side script synchronously.Run an action from a server-side script synchronously from the current user session without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.Runs a Data Stream action synchronously from a server-side script and returns a ScriptableDataStream object.Runs a flow from a server-side script synchronously.Runs a flow, subflow, action, or Data Stream action from a server-side script synchronously or asynchronously without creating execution details or other related records. Improves performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.Runs an subflow from a server-side script synchronously.Run a subflow from a server-side script synchronously from the current user session without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.Returns the error messages produced by a flow, subflow, or action. This method cannot return messages from flows, subflows, or actions run with the quick\(\) API.Return a JSON string containing the list of flow stages.Returns the outputs of a completed action or subflow.Returns a ScriptableFlowRunner builder object for a flow or action that you want to run.Returns the status of a flow, subflow, or action.Checks if a flow within a give scope contains any Ask for Approval actions.Restarts a flow, subflow, or action that was run in the background. You can provide new inputs or omit them to reuse the previously provided inputs.Schedule a system event in the Flow Engine Queue to cancel a flow that is in the in progress, presumed interrupted, or waiting state after a delay.Send a specific message and payload response to a flow that is paused and waiting for a message.Builds password2 values inside a script step.Runs an action from a server-side script asynchronously.Runs an action from a server-side script asynchronously without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.Runs a flow from a server-side script.Runs a flow from a server-side script asynchronously without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.Runs a subflow from a server-side script.Runs a subflow from a server-side script asynchronously without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 45
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# FlowAPI - Scoped, Global

The FlowAPI provides methods to execute actions, flows, or subflows in server-side scripts using either blocking or non-blocking methods.

Access FlowAPI methods in global and scoped scripts using the `sn_fd` namespace. Create calls to your flows using the **Code Snippet** action in Workflow Studio or use the methods detailed here to update scripts manually.

**Note:** In domain separated instances, flows, subflows, and actions triggered by this API run in the domain of the user who started the script. For example, if a user in the Acme domain starts a script that triggers a flow, the flow runs in the Acme domain and can only access Acme data, even if the flow runs as the System User.

**Note:** To optimize instance performance, avoid calling these methods from an asynchronous business rule script. Instead, create a scheduled job record within the Workflow Studio UI.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## FlowAPI - cancel\(String contextId, String reason\)

Cancels a paused or running flow, subflow, or action.

<table id="table_twb_vmn_p3b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contextId

</td><td>

String

</td><td>

Sys\_id of the execution details record for the flow, subflow, or action. Access the execution details by navigating to the Flow Executions tab in Workflow Studio, or pass the sys\_id of the context record returned by the startFlow\(\), startSubflow\(\), or startAction\(\) methods.**Note:** There might be a small delay in cancellation if the target context is running on a different node of the instance. Contexts running on the same node are cancelled immediately. Contexts running on another node must first wait for the cancellation to be forwarded to the appropriate node.

</td></tr><tr><td>

reason

</td><td>

String

</td><td>

Optional. Reason for canceling the flow, subflow, or action. Appears in the **Message** field of the Flow engine log entries \[sys\_flow\_log\] table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This example uses the return value of the startFlow\(\) method to cancel any long-running flows.

```
(function() { 

var now_GR = new GlideRecord('incident'); 
now_GR.addQuery('number', 'INC0000050'); 
now_GR.query(); 
now_GR.next(); 

      try { 
          var inputs = {}; 
          inputs['current'] = now_GR; // GlideRecord of table: 
          inputs['table_name'] = 'incident'; 

          // Starts the flow asynchronously.
          var result = sn_fd.FlowAPI.getRunner()
          .flow('global.myFlow')
          .inBackground()
          .withInputs(inputs)
          .run();

          var contextId = result.getContextId();
          var dateRun = result.getDate();
          var domainUsed = result.getDomainId();
          var flowName = result.getFlowObjectName();
          var flowObjectType = result.getFlowObjectType(); 

      } catch (ex) { 
          var message = ex.getMessage(); 
          gs.error(message); 
      } 
})();

 
// Call the cancel() method using the context Id returned from the startFlow() method
sn_fd.FlowAPI.cancel(contextId, 'Flow took too long to execute.');
```

This example cancels any flows named Test Flow.

```
var now_GR = new GlideRecord("sys_flow_context");
now_GR.addQuery("name", "Test Flow");
now_GR.query();

while (now_GR.next()) {
sn_fd.FlowAPI.cancel(now_GR.getUniqueValue(), 'Canceling Test Flows');
} 
```

## FlowAPI - executeAction\(String name, Map inputs, Number timeout\)

Runs an action from a server-side script synchronously.

Execute an action from within a business rule, script include, or any other server-side script. Actions run using this method run synchronously, so the method has access to outputs created by the action. Use **startAction** to run an action asynchronously.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** This method runs the action as the user who initiates the session.

|Name|Type|Description|
|----|----|-----------|
|name|String|The scope and name of the action to be executed, for example `global.action_name`.|
|inputs|Map|Name-value pairs that define action inputs. Use the input name, not the input label.|
|timeout|Number|Optional. Timeout in milliseconds. This value overrides the 30 second default timeout specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property. After the timeout expires, an exception is thrown.|

|Type|Description|
|----|-----------|
|Object|The action outputs.|

In this example, the script uses sn\_fd.FlowAPI.executeAction to execute an action called actionforpassword2test in the global scope. A variable called inputs contains the inputs for the action. In this case, a name and password. The outputs for the action are stored in the outputs variable, which in this case, is an encrypted password object. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {
	
  try {
    var inputs = {};
    inputs['name'] = ; // String 
    inputs['password2'] = ; // Password (2 Way Encrypted) 
		
    // Execute Synchronously: Run in foreground. Code snippet has access to outputs.
    // var timeout = ; //timeout in ms
    //sn_fd.FlowAPI.executeAction('global.actionforpassword2test', inputs, timeout)
    var outputs = sn_fd.FlowAPI.executeAction('global.actionforpassword2test', inputs);

    // Get Outputs:
    // Note: outputs can only be retrieved when executing synchronously.
    var output = outputs['output']; // Password (2 Way Encrypted)
		
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();
```

## FlowAPI - executeActionQuick\(String name, Map inputs, Number timeout\)

Run an action from a server-side script synchronously from the current user session without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Wait support**

    This method does not support pausing the action to wait for conditions. Steps that pause for wait conditions such as Ask for Approval or Wait for Condition are not supported.

-   **MID Server support**

    This method does not support pausing an action to run from a MID Server.


**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

<table id="table_gx5_kcf_1hb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

Scope and internal name of the action to execute. For example, `global.action_name`. Locate the **Internal name** field in the list of Workflow Studio actions.

</td></tr><tr><td>

inputs

</td><td>

Map

</td><td>

Name-value pairs that define action inputs. You can find the available action inputs and required data types under Inputs in the action outline. Use the input name, not the input label. For example, `{'table':'incident','sys_id':'a39d8e3cf0212300964feeefe80ff0ed'}`.

</td></tr><tr><td>

timeout

</td><td>

Number

</td><td>

Optional. Timeout in milliseconds. This value overrides the 30 second default timeout specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property. After the timeout expires, an exception is thrown.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|Object containing outputs defined by the action. You can find the outputs for the action under **Outputs** in the action outline.|

```
(function() {
  try {

    var grIncident = new GlideRecord('incident');
    grIncident.get('57af7aec73d423002728660c4cf6a71c');

    var inputs = {};
    inputs['variable'] = grIncident;

    var outputs = sn_fd.FlowAPI.executeActionQuick('global.update_record_test', inputs);

    // Get Outputs:
    // Note: outputs can only be retrieved when executing synchronously.
    var output1 = outputs['output1']; 

  } catch (ex) { 
    var message = ex.getMessage();
    gs.error(message);
    }
	
})();
```

## FlowAPI - executeDataStreamAction\(String name, Map inputs, Number timeout\)

Runs a Data Stream action synchronously from a server-side script and returns a ScriptableDataStream object.

For more information about Data Stream actions, see [Data Stream actions and pagination](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/data-stream-actions.md).

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** Always wrap data stream logic in a `try/catch` block to catch errors. Always include a `finally` statement that ends with the close\(\) method from the ScriptableDataStream class to close the data stream and prevent performance issues.

<table id="table_oz4_hd3_z3b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

The scope and name of the Data Stream action to execute. For example, `global.data_stream_action_name`.

</td></tr><tr><td>

inputs

</td><td>

Map

</td><td>

Name-value pairs that define action inputs. Use the input name, not the input label. If the action does not have any inputs, do not include this parameter.

</td></tr><tr><td>

timeout

</td><td>

Number

</td><td>

Optional. Amount of time before the action times out. After the timeout expires, an exception is thrown. The timeout only applies to the executeDataStreamAction method, not to methods in the ScriptableDataStream class.Default: 30000, specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property

 Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|ScriptableDataStream|An object used to iterate through items in the data stream. Use the methods in the ScriptableDataStream class to interact with this object. See [ScriptableDataStream API](../../ScriptableDataStream/concept/ScriptableDataStreamAPI.md#).|

This example creates an incident record for each item returned in the data stream.

```
(function() {
	
  try {

    // Execute Data Stream Action. 
    var stream = sn_fd.FlowAPI.executeDataStreamAction('x_my_scope.data_stream_name');

    // Process each item in the data stream
    while (stream.hasNext()) {

      // Get a single item from the data stream.
      var item = stream.next();

      // Use the item. 
      var now_GR = new GlideRecord('incident');
      now_GR.setValue('number',item.id);
      now_GR.setValue('short_description',item.name);
      now_GR.insert();
		
      // By default, this code snippet will terminate after 10 items.
      // Remove or modify this limit after testing your code.
      if (stream.getItemIndex() >= 9) {
        break;
      }
    }
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  } finally {
    stream.close();
  }
	
})();
```

## FlowAPI - executeFlow\(String name, Map inputs, Number timeout\)

Runs a flow from a server-side script synchronously.

Execute a flow from within a business rule, script include, or any other server-side script. Flows run using this method run synchronously. Use **startFlow** to run a flow asynchronously.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** This method runs the flow as the user specified in flow properties.

|Name|Type|Description|
|----|----|-----------|
|name|String|The scope and name of the flow to be executed, for example `global.flow_name`.|
|inputs|Map|Name-value pairs that define trigger inputs. Use the input name, not the input label.|
|timeout|Number|Optional. Timeout in milliseconds. This value overrides the 30 second default timeout specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property. After the timeout expires, an exception is thrown.|

|Type|Description|
|----|-----------|
|None|Normal operation produces no return value.|
|Exception|The API throws an exception when a flow called synchronously pauses. `The current execution is in the waiting state`. In most cases, the exception is removed when the flow resumes. However, the API cannot resume a flow that has been sent to a MID Server.|

This example uses sn\_fd.FlowAPI.executeFlow to execute a global flow called test\_flow. This flow is normally triggered when a record on the incident table is updated. Because you are activating the flow from a script, you must provide this information. The code creates an inputs variable that contains the current record, and the table for the record. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {
  try {
    var inputs = {};
    inputs['current'] = ; // GlideRecord of table:  
    inputs['table_name'] = 'incident';

    // Execute Synchronously: Run in foreground.
    // var timeout = ; //timeout in ms
    //sn_fd.FlowAPI.executeFlow('global.test_flow', inputs, timeout)
    sn_fd.FlowAPI.executeFlow('global.test_flow', inputs);
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();
```

## FlowAPI - executeFlowQuick\(String name, Map inputs, Number timeout\)

Runs a flow, subflow, action, or Data Stream action from a server-side script synchronously or asynchronously without creating execution details or other related records. Improves performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Run as user**

    This method runs the flow as the user who initiates the session. Setting the flow to run as the system user, or impersonating a user, is not supported.

-   **Wait support**

    This method does not support pausing the flow to wait for conditions. Actions or flow logic that pause for wait conditions such as Ask for Approval, Wait for Condition, or Wait for a duration are not supported.

-   **MID Server support**

    This method does not support pausing a flow to run from a MID Server.


**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

|Name|Type|Description|
|----|----|-----------|
|name|String|Scope and internal name of the flow to execute. For example, `global.flow_name`. Locate the **Internal name** field in the list of Workflow Studio flows.|
|inputs|Map|Name-value pairs that define trigger inputs. You can find the available trigger inputs and required data types in the Trigger section of the flow. Use the input name, not the input label. For example, `{'table':'incident','sys_id':'a39d8e3cf0212300964feeefe80ff0ed'}`.|
|timeout|Number|Optional. Timeout in milliseconds. This value overrides the 30 second default timeout specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property. After the timeout expires, an exception is thrown.|

|Type|Description|
|----|-----------|
|void| |

```
(function() {
	
  try {
    var grIncident = new GlideRecord('incident');
    grIncident.get('ed92e8d173d023002728660c4cf6a7bc');

    var inputs = {};
    inputs['current'] = grIncident;
    inputs['table_name'] = 'incident';
		
    sn_fd.FlowAPI.executeFlowQuick('global.test_quick_flow', inputs);
		
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
	}
	
})();
```

## FlowAPI - executeSubflow\(String name, Map inputs, Number timeout\)

Runs an subflow from a server-side script synchronously.

Execute a subflow from within a business rule, script include, or any other server-side script. Subflows run using this method run synchronously. Use **startSubflow** to run an subflow asynchronously.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** This method runs the flow as the user specified in flow properties.

|Name|Type|Description|
|----|----|-----------|
|name|String|The scope and name of the subflow to be executed, for example `global.subflow_name`.|
|inputs|Map|Name-value pairs that define subflow inputs. Use the input name, not the input label.|
|timeout|Number|Optional. Timeout in milliseconds. This value overrides the 30 second default timeout specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property. After the timeout expires, an exception is thrown.|

|Type|Description|
|----|-----------|
|Object|Object containing the subflow outputs.|
|Exception|The API throws an exception when a flow called synchronously pauses. `The current execution is in the waiting state`. In most cases, the exception is removed when the flow resumes. However, the API cannot resume a flow that has been sent to a MID Server.|

In this example, the script uses sn\_fd.FlowAPI.executeSubflow to execute an subflow called subflowTest in the global scope. A variable called inputs contains the inputs for the subflow. In this case, a name and password. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```

(function() {
	
	try {
		var inputs = {};
		inputs['name'] = ; // String 
		inputs['password2'] = ; // Password (2 Way Encrypted) 
		
		// Execute Synchronously: Run in foreground.
		// var timeout = ; //timeout in ms
              //sn_fd.FlowAPI.executeSubflow('global.subflowTest', inputs, timeout)
              var outputs = sn_fd.FlowAPI.executeSubflow('global.subflowTest', inputs);
		
	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	}	
})();
```

## FlowAPI - executeSubflowQuick\(String name, Map inputs, Number timeout\)

Run a subflow from a server-side script synchronously from the current user session without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Run as user**

    This method runs the flow as the user who initiates the session. Setting the flow to run as the system user, or impersonating a user, is not supported.

-   **Wait support**

    This method does not support pausing the flow to wait for conditions. Actions or flow logic that pause for wait conditions such as Ask for Approval, Wait for Condition, or Wait for a duration are not supported.

-   **MID Server support**

    This method does not support pausing a flow to run from a MID Server.


**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

|Name|Type|Description|
|----|----|-----------|
|name|String|Scope and internal name of the subflow to execute. For example, `global.subflow_name`. Locate the **Internal name** field in the list of Workflow Studio subflows.|
|inputs|Map|Name-value pairs that define subflow inputs. You can find the available subflow inputs and required data types under Inputs in the subflow. Use the input name, not the input label. For example, `{'table':'incident','sys_id':'a39d8e3cf0212300964feeefe80ff0ed'}`.|
|timeout|Number|Optional. Timeout in milliseconds. This value overrides the 30 second default timeout specified by the **com.glide.hub.flow\_api.default\_execution\_time** system property. After the timeout expires, an exception is thrown.|

|Type|Description|
|----|-----------|
|Object|Object containing outputs defined by the subflow. You can find the outputs for the subflow under **Subflow Inputs &amp; Outputs** in the subflow outline.|

```
(function() {

  try {
    var grIncident = new GlideRecord('incident');
    grIncident.get('57af7aec73d423002728660c4cf6a71c');

    var inputs = {};
    inputs['variable'] = grIncident;

    var outputs = sn_fd.FlowAPI.executeSubflowQuick('global.test_quick_run_subflow', inputs);

    // Get Outputs:
    // Note: outputs can only be retrieved when executing synchronously.
    var output1 = outputs['output1']; 
		
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
    }
	
})();
```

## FlowAPI - getErrorMessage\(String contextId\)

Returns the error messages produced by a flow, subflow, or action. This method cannot return messages from flows, subflows, or actions run with the quick\(\) API.

|Name|Type|Description|
|----|----|-----------|
|contextId|String|The sys\_id of the flow, subflow, or action whose error messages you want to get.|

|Type|Description|
|----|-----------|
|String|The last operation run and the error message it produced.|

This example starts a global subflow called test\_error\_subflow and returns any error messages it produces. Normally, a single script does not both run a flow and then get its error messages. Typically, either another script or Workflow Studio would have already run the flow. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {

  try {
    // Gather inputs to call flow
    var inputs = {};
    inputs['ah_task'] = myTaskRecord; // GlideRecord of table: task
    inputs['ah_comment'] ='Test Comment' ; // String

    // Call flow with known errors
    var contextId = sn_fd.FlowAPI.startSubflow('global.test_error_subflow', inputs);

    // Get flow error message
    var errormsg = sn_fd.FlowAPI.getErrorMessage(contextId);
    return errormsg;

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();

```

Output:

```
Operation (test_error_flow.574033f6db6811102166e2291396199f.274073f6db6811102166e22913961908.0be0d916c31332002841b63b12d3ae13) failed with error: com.snc.process_flow.exception.OpException: Value of field record is not a GlideRecord
at com.snc.process_flow.operation.FieldValue.getGlideRecord(FieldValue.java:145)
at com.snc.process_flow.operation.CRUDOperation.getInputValidGlideRecord(CRUDOperation.java:54)
at com.snc.process_flow.operation.RecordDeleteOperation.run(RecordDeleteOperation.java:26)
at com.snc.process_flow.engine.Operation.execute(Operation.java:212)
at com.snc.process_flow.engine.restricted_caller_access.ExecuteWithCallerAccessTracking.executeWithMetaStack(ExecuteWithCallerAccessTracking.java:31)
at com.snc.process_flow.engine.ProcessEngine.executeOps(ProcessEngine.java:570)
at com.snc.process_flow.engine.ProcessEngine.runInternal(ProcessEngine.java:476)
at com.snc.process_flow.engine.ProcessEngine.run(ProcessEngine.java:462)
at com.snc.process_flow.engine.ProcessAutomation.run(ProcessAutomation.java:86)
at com.snc.process_flow.engine.GlideProcessAutomation.runSync(GlideProcessAutomation.java:155)
at com.snc.process_flow.engine.GlideProcessAutomation.runWithDomain(GlideProcessAutomation.java:270)
at com.snc.process_flow.engine.GlideProcessAutomation.lambda$runAsUserSync$1(GlideProcessAutomation.java:237)
at com.snc.process_flow.engine.PFSessionClone.run(PFSessionClone.java:70)
at com.snc.process_flow.engine.GlidePFSession.runPlanAsUserSession(GlidePFSession.java:42)
at com.snc.process_flow.engine.GlideProcessAutomation.runAsUserSync(GlideProcessAutomation.java:235)
at com.snc.process_flow.engine.GlideProcessAutomation.messageFlow(GlideProcessAutomation.java:330)
at com.snc.process_flow.engine.GlideProcessAutomation.messageFlow(GlideProcessAutomation.java:309)
at com.snc.process_flow.engine.ProcessHubEventHandler.doSendMessage(ProcessHubEventHandler.java:475)
at com.snc.process_flow.engine.ProcessHubEventHandler.process(ProcessHubEventHandler.java:119)
at com.snc.process_flow.engine.ProcessHubEventHandler.process(ProcessHubEventHandler.java:91)
at com.snc.process_flow.engine.FlowEventManager.processEvents(FlowEventManager.java:122)
at com.glide.job.EventHandlerJob.execute(EventHandlerJob.java:38)
at com.glide.schedule.JobExecutor.lambda$executeJob$0(JobExecutor.java:129)
at com.snc.db.data_replicate.replicator.DataReplicationAdvisors.runInOriginatorContext(DataReplicationAdvisors.java:73)
at com.glide.schedule.JobExecutor.lambda$inDataReplicationContext$2(JobExecutor.java:159)
at com.glide.schedule.JobExecutor.executeJob(JobExecutor.java:132)
at com.glide.schedule.JobExecutor.execute(JobExecutor.java:116)
at com.glide.schedule_v2.SchedulerWorkerThread.executeJob(SchedulerWorkerThread.java:338)
at com.glide.schedule_v2.SchedulerWorkerThread.lambda$process$0(SchedulerWorkerThread.java:220)
at com.glide.worker.TransactionalWorkerThread.executeInTransaction(TransactionalWorkerThread.java:35)
at com.glide.schedule_v2.SchedulerWorkerThread.process(SchedulerWorkerThread.java:220)
at com.glide.schedule_v2.SchedulerWorkerThread.run(SchedulerWorkerThread.java:101)
```

## FlowAPI - getFlowStages\(String scopedFlowName\)

Return a JSON string containing the list of flow stages.

|Name|Type|Description|
|----|----|-----------|
|scopedFlowName|String|The application scope and name of the flow whose stages you want to get.|

|Type|Description|
|----|-----------|
|String|JSON formatted string that lists the stages of the flow by their stage record values.|

This example shows getting the stages for the Service Catalog Item Request flow.

```
(function() {

  try {
    // Name of flow with stages
    var flowName = "service_catalog_item_request";

    // Get flow stages
    var flowStages = sn_fd.FlowAPI.getFlowStages(flowName);
    //Print JSON as info message  
    gs.info(flowStages);
    return flowStages;

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();

```

Output:

The JSON string contains name-value pairs for a stage field. See for more information.

```
[
  {
    "label": "Manager Approval",
    "value": "manager_approval",
    "type": "standard",
    "duration": "1970-01-03 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 0
  },
  {
    "label": "Set current stage state to:  [Error]",
    "value": "Set current stage state to:  [Error]",
    "type": "error",
    "duration": "1970-01-01 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": false,
    "order": 0
  },
  {
    "label": "Dept. Head Approval",
    "value": "Dept. Head Approval",
    "type": "standard",
    "duration": "1970-01-03 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 1
  },
  {
    "label": "CIO Approval",
    "value": "CIO Approval",
    "type": "standard",
    "duration": "1970-01-03 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 2
  },
  {
    "label": "Order Fulfillment",
    "value": "Order Fulfillment",
    "type": "standard",
    "duration": "1970-01-05 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 3
  },
  {
    "label": "Backordered",
    "value": "Backordered",
    "type": "standard",
    "duration": "1970-01-15 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 4
  },
  {
    "label": "Deployment",
    "value": "Deployment",
    "type": "standard",
    "duration": "1970-01-02 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 5
  },
  {
    "label": "Request Cancelled",
    "value": "Request Cancelled",
    "type": "standard",
    "duration": "1970-01-01 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 6
  },
  {
    "label": "Completed",
    "value": "complete",
    "type": "standard",
    "duration": "1970-01-01 00:00:00",
    "states": {
      "pending": "Pending - has not started",
      "inprogress": "In progress",
      "skipped": "Skipped",
      "complete": "Completed",
      "error": "Error"
    },
    "flow": "30f3d26187e92300e0ef0cf888cb0b91",
    "alwaysShow": true,
    "order": 7
  }
]
```

## FlowAPI - getOutputs\(String contextId\)

Returns the outputs of a completed action or subflow.

You can use the return values from either the startAction\(\) orstartSubflow\(\) methods as the contextId parameter.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

|Name|Type|Description|
|----|----|-----------|
|contextId|String|The sys\_id of the action or subflow whose outputs you want to get.|

|Type|Description|
|----|-----------|
|Object|Object containing the action or subflow outputs.|

This example starts a global subflow called test\_subflow, waits for the flow to finish, and then gets its output values. Normally, a single script does not both run a flow and then get its output values. Since a flow may not complete before the getOutputs\(\) call, this example uses a wait time. Typically, either another script or Workflow Studio would have already run the flow. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {

  try {
    // Gather inputs to call flow
    var inputs = {};
    inputs['ah_task'] = myTaskRecord; // GlideRecord of table: task
    inputs['ah_comment'] ='Test Comment' ; // String

    // Call flow
    var contextId = sn_fd.FlowAPI.startSubflow('global.test_subflow', inputs);

    // Wait for the flow to finish running

    // Get flow outputs
    var outputs = sn_fd.FlowAPI.getOutputs(contextId);
    var output1 = outputs['output1'];
    return output1;

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();

```

## FlowAPI - getRunner\(\)

Returns a ScriptableFlowRunner builder object for a flow or action that you want to run.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[ScriptableFlowRunner](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#)|Builder object used to run a Workflow Studio action, flow, or subflow.|

This example runs a flow synchronously.

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

## FlowAPI - getStatus\(String contextId\)

Returns the status of a flow, subflow, or action.

|Name|Type|Description|
|----|----|-----------|
|contextId|String|The sys\_id of the flow, subflow, or action whose status you want to get.|

<table id="table_jsj_glz_dbc" class="returns"><thead><tr><th>

Parameter

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;

</td><td>

Object

</td><td>

Object containing the current state of the flow, subflow, or action as name-value pairs. ```
{
    "hasLookupError": Boolean,
    "errorMessage": "String",
    "contextStatus": {Object}
  }
```

</td></tr><tr><td>

&lt;Object&gt;.hasLookupError

</td><td>

Boolean

</td><td>

Flag that indicates whether there was an issue looking up the context status of the flow, subflow, or action.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {Object}
  }
```

</td></tr><tr><td>

&lt;Object&gt;.errorMessage

</td><td>

String

</td><td>

Error message returned by context lookup operation. This parameter is void when **hasLookupError** is false.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {Object}
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus

</td><td>

Object

</td><td>

Object containing state details about the queried flow, subflow, or action.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "COMPLETE",
      "errorState": "NONE"
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.state

</td><td>

String

</td><td>

State of the flow, subflow, or action context. Some state values provide additional information in related parameters.-   COMPLETE provides additional information in the **errorState** parameter
-   ERROR provides additional information in the **message** parameter
-   CANCELLED provides additional information in the **canceledReason** parameter
-   IN\_PROGRESS provides additional information in the **isRunOnMid** parameter
-   WAITING provides additional information in the **waitingOn** parameter

```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "COMPLETE",
      "errorState": "NONE"
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.errorState

</td><td>

String

</td><td>

Flow complete state produced by flow error handling. The API only generates this parameter when the flow, subflow, or action is in the COMPLETE state.-   ERROR\_CAUGHT
-   ERROR\_SKIPPED

```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "COMPLETE",
      "errorState": "ERROR_CAUGHT"
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.message

</td><td>

String

</td><td>

Error message returned by the flow, subflow, or action. The API only generates this parameter when the flow, subflow, or action is in the ERROR state.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "ERROR",
      "message": "Error:  Error Message! (Process Automation.LOG; line 1)"
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.canceledReason

</td><td>

String

</td><td>

Cancel message returned by the flow, subflow, or action. The API only generates this parameter when the flow, subflow, or action is in the CANCELLED state.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "CANCELLED",
      "canceledReason": "User has requested to stop executing the flow"
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.isRunOnMid

</td><td>

Boolean

</td><td>

Flag that indicates whether the flow, subflow, or action is run on a MID Server environment. The API only generates this parameter when the flow, subflow, or action is in the IN\_PROGRESS state.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "IN_PROGRESS",
      "isRunOnMid": true
    }
  }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn

</td><td>

Array

</td><td>

List of items that the current flow, subflow, or action is waiting on. The API only generates this parameter when the flow, subflow, or action is in the WAITING state.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "WAITING",
      "waitingOn": [
        {
          "order":"1",
          "stepType": "TIMER",
          "endTime": 1713627497643
        },
        {
          "order":"5",
          "stepType": "WAIT_FOR_CONDITION_WITH_TIMEOUT",
          "table": "incident",
          "condition": "sys_id=10e8b43243200210338774d6ebb8f22d^short_description=112",
          "endTime": 1713645497800
        }
      ]
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.order

</td><td>

String

</td><td>

Flow step number of the item that is causing the flow to wait. If the waiting action is a custom action within a flow, the order also includes a period and the action step number of custom action on which the flow is waiting.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "WAITING",
      "waitingOn": [
        {
          "order":"1",
          "stepType": "TIMER",
          "endTime": 1713627497643
        },
        {
          "order":"5",
          "stepType": "WAIT_FOR_CONDITION_WITH_TIMEOUT",
          "table": "incident",
          "condition": "sys_id=10e8b43243200210338774d6ebb8f22d^short_description=112",
          "endTime": 1713645497800
        }
      ]
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.stepType

</td><td>

String

</td><td>

Type of action or flow step that is causing the flow, subflow, or action to wait. The API only generates this parameter when the flow, subflow, or action is in the WAITING state. Here are some common examples.-   WAIT\_FOR\_CONDITION
-   WAIT\_FOR\_CONDITION\_WITH\_TIMEOUT
-   ASK\_FOR\_APPROVAL
-   CREATE\_TASK\_WITH\_WAIT
-   TIMER
-   SLA\_TIMER
-   SUBFLOW

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.table

</td><td>

String

</td><td>

Table name containing the record that the flow, subflow, or action is waiting on. The API only generates this parameter when the flow, subflow, or action is in the WAITING state and the stepType is WAIT\_FOR\_CONDITION, WAIT\_FOR\_CONDITION\_WITH\_TIMEOUT, ASK\_FOR\_APPROVAL, or CREATE\_TASK\_WITH\_WAIT.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "WAITING",
      "waitingOn": [
          {
          "order":"1",
          "stepType": "WAIT_FOR_CONDITION",
          "table": "incident",
          "condition": "sys_id=1347723243200210338774d6ebb8f285^short_description=1238"
          }
        ]
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.condition

</td><td>

String

</td><td>

Query condition of the record that the flow, subflow, or action is waiting on. The API only generates this parameter when the flow, subflow, or action is in the WAITING state and there is a condition that must be met to continue running.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "WAITING",
      "waitingOn": [
          {
          "order":"1",
          "stepType": "WAIT_FOR_CONDITION",
          "table": "incident",
          "condition": "sys_id=1347723243200210338774d6ebb8f285^short_description=1238"
          }
        ]
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.endTime

</td><td>

Integer

</td><td>

End time that the flow, subflow, or action is waiting on. The API only generates this parameter when the flow, subflow, or action is in the WAITING state and the stepType is WAIT\_FOR\_CONDITION\_WITH\_TIMEOUT, TIMER, or SLA\_TIMER.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
    "state": "WAITING",
    "waitingOn": [
        {
          "order":"3",
          "stepType": "SLA_TIMER",
          "endTime": 1713574610000
        }
    ]
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.approvalRule

</td><td>

String

</td><td>

Approval rule that the flow, subflow, or action is waiting on. The API only generates this parameter when the flow, subflow, or action is in the WAITING state and the stepType is ASK\_FOR\_APPROVAL.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "WAITING",
      "waitingOn": [
        {
          "order":"3",
          "stepType": "ASK_FOR_APPROVAL",
          "table": "incident",
          "condition": "sys_id=3bd89703372002103387963174924b20^approvalINapproved,rejected,cancelled",
          "approvalRule": "ApprovesAnyU[a8f98bb0eb32010045e1a5115206fe3a,71826bf03710200044e0bfc8bcbe5d3b]"
        }
      ]
    }
  }
```

</td></tr><tr><td>

&lt;Object&gt;.contextStatus.waitingOn.contextId

</td><td>

String

</td><td>

The sys\_id of the subflow that the flow or subflow is waiting on. The API only generates this parameter when the flow, or subflow is in the WAITING state and the stepType is SUBFLOW.```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
    "state": "WAITING",
    "waitingOn": [
        {
          "order":"1",
          "stepType": "SUBFLOW",
          "contextId": "0f724aabd921021020291a665e07e44a"
        }
      ]
    }
  }
```

</td></tr></tbody>
</table>This example runs a flow containing Do the following in parallel flow logic. Normally, a single script does not both run a flow and then get its error messages. Typically, either another script or Workflow Studio would have already run the flow.

```
(function() {
  try {
    var result = sn_fd.FlowAPI.getRunner()  // Create a ScriptableFlowRunner builder object.
      .flow('global.test_do_in_parallel')   // Run the global scope flow named do_in_parallel.
      .run();                               // Run the flow and return a FlowRunnerResult object.

    var contextId = result.getContextId();  // Retrieve the context ID from the result

    var flowStatus = sn_fd.FlowAPI
      .getStatus(contextId);                // Retrieve any outputs from the flow execution.

    JSON.stringfy(flowStatus);              // Convert object to string
    return flowStatus;
		
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
	
})();
```

Output:

```
{
    "hasLookupError": false,
    "errorMessage": "",
    "contextStatus": {
      "state": "WAITING",
      "waitingOn": [
        {
          "order":"1",
          "stepType": "TIMER",
          "endTime": 1713627497643
        },
        {
          "order":"5",
          "stepType": "WAIT_FOR_CONDITION_WITH_TIMEOUT",
          "table": "incident",
          "condition": "sys_id=10e8b43243200210338774d6ebb8f22d^short_description=112",
          "endTime": 1713645497800
        }
      ]
    }
  }
```

## FlowAPI - hasApprovals\(String scopedFlowName\)

Checks if a flow within a give scope contains any Ask for Approval actions.

The hasApprovals\(\) method determines if a flow within a given scope contains any Ask for Approval actions. This method also checks if any Ask for Approval actions within the flow are nested under If flow logic blocks. For more information, see [Ask for Approval actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/ask-approval-flow-designer.md).

|Name|Type|Description|
|----|----|-----------|
|scopedFlowName|String|Scope and internal name of the flow to execute. For example, `global.flow_name`. Locate the **Internal name** field in the list of Workflow Studio flows.|

<table id="table_x1d_dz2_vlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Returns one of the following string values:-   ALWAYS: The flow contains an Ask for Approval action that isn't nested within a conditional `If` flow logic block.
-   CONDITIONALLY: The flow contains an Ask for Approval action that is nested within a conditional `If` flow logic block.
-   NO: The flow doesn't contain any Ask for Approval actions.
-   UNKNOWN: There was a compiler error, and the system can't determine whether the flow contains any Ask for Approval actions.

</td></tr></tbody>
</table>The following example checks if the example\_flow flow within the global scope contains any Ask for Approval actions and logs the result.

```
(function() {
	
  try {
    var result = sn_fd.FlowAPI.hasApprovals('global.example_flow');
    gs.log('Result: ' + result);
  }

  catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();
```

## FlowAPI - restartFlowFromContext\(String ContextId, Map providedInputs\)

Restarts a flow, subflow, or action that was run in the background. You can provide new inputs or omit them to reuse the previously provided inputs.

|Name|Type|Description|
|----|----|-----------|
|contextId|String|The sys\_id of the flow, subflow, or action you want to restart. This flow, subflow, or action must have run in background and have an associated sysevent record.|
|providedInputs|Object|Optional. Map object containing the name-value pairs that define replacement inputs for the flow, subflow, or action. If you omit or provide a null value for this parameter, the flow, subflow, or action runs using the previously provided inputs.|

|Type|Description|
|----|-----------|
|ScriptableFlowRunnerResultsScoped|Object containing the execution details of a Workflow Studio action, flow, or subflow.|

Restarts a sample flow that has a record-based trigger on the Incident table. The original flow used sample incident INC0008112 as an input. When the flow restarts it instead uses sample incident INC0008111 as an input.

```
(function() {
  try {

    var flowContextID = '4216396ffd7d11107edcf07204c30fd5';     // sys_id of sys_flow_context record
    var oldIncidentRecord = '552c48888c033300964f4932b03eb092'; // sys_id of INC0008112
    var newIncidentRecord = 'a83820b58f723300e7e16c7827bdeed2'; // sys_id of INC0008111
    var inputs = {};
    var gr = new GlideRecord('incident'); // Create new incident object

    gr.get(newIncidentRecord);            // Get GlideRecord object for INC0008111

    inputs['current'] = gr;               // Set new Incident record as input
    inputs['table_name'] = 'incident';    // Set table name to Incident

    var result = sn_fd.FlowAPI.getRunner()            // Create a ScriptableFlowRunner builder object.
      .restartFlowFromContext(flowContextID, inputs); // Restart flow with new inputs.

    var contextId = result.getContextId();  // Retrieve the context ID from the result
    var dateRun = result.getDate();

    gs.info(contextId + ' ' + dateRun);

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();

```

## FlowAPI - scheduleCancel\(String contextId, String reason, Integer delaySeconds\)

Schedule a system event in the Flow Engine Queue to cancel a flow that is in the in progress, presumed interrupted, or waiting state after a delay.

<table id="table_mrg_gpn_v5b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contextId

</td><td>

String

</td><td>

Sys\_id of the execution details record for the flow, subflow, or action. The target flow, subflow, or action must be in the in progress, presumed interrupted, or waiting state. Access the execution details by navigating to the Flow Executions tab in Workflow Studio, or pass the sys\_id of the context record returned by the method.**Note:** There might be a small delay in cancellation if the target context is running on a different node of the instance. Contexts running on the same node are cancelled immediately. Contexts running on another node must first wait for the cancellation to be forwarded to the appropriate node.

</td></tr><tr><td>

reason

</td><td>

String

</td><td>

Reason for canceling the flow, subflow, or action. Appears in the **Message** field of the Flow engine log entries \[sys\_flow\_log\] table.

</td></tr><tr><td>

delaySeconds

</td><td>

Integer

</td><td>

Optional. Number of seconds to wait before processing a cancellation event in the Flow Engine Queue. If you omit this parameter, the method uses the default value of 1 second.You can use this parameter to avoid the performance impact of scheduling the cancellation of thousands of flow contexts at the same time. Rather than run all cancellations simultaneously, schedule a batch of flow cancellations with a delay. Alternatively, you could use the delay as a time out value for an asynchronous flow.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example uses the return value of the startFlow\(\) method to schedule the cancellation of any long-running flows.

```
(function() { 

var now_GR = new GlideRecord('incident'); 
now_GR.addQuery('number', 'INC0000050'); 
now_GR.query(); 
now_GR.next(); 

      try { 
          var inputs = {}; 
          inputs['current'] = now_GR; // GlideRecord of table: 
          inputs['table_name'] = 'incident'; 

          // Starts the flow asynchronously.
          var contextId = sn_fd.FlowAPI.startFlow('global.myFlow', inputs); 

      } catch (ex) { 
          var message = ex.getMessage(); 
          gs.error(message); 
      } 
})();

 
// Call the scheduleCancel() method using the context Id returned from the startFlow() method
sn_fd.FlowAPI.scheduleCancel(contextId, 'Flow took too long to execute.', 60);
```

This example schedules the cancellation of any flows named Test Flow.

```
var now_GR = new GlideRecord("sys_flow_context");
now_GR.addQuery("name", "Test Flow");
now_GR.query();

while (now_GR.next()) {
sn_fd.FlowAPI.scheduleCancel(now_GR.getUniqueValue(), 'Canceling Test Flows', 60);
} 
```

This example uses the delaySeconds parameter to run flow cancellation jobs in batches. Use batches to cancel thousands of flow contexts.

```
var delaySeconds = 1;

for (var i; i < sys_flow_context.length; ++i) {
  if (i % 100 === 0) {
    delaySeconds = delaySeconds + 60;
  }
  var contextId = sys_flow_context[i];
  var reason = "Example reason";
  sn_fd.FlowAPI.scheduleCancel(contextId, reason, delaySeconds);
}
```

## FlowAPI - sendMessage\(String contextSysID, String message, String payload\)

Send a specific message and payload response to a flow that is paused and waiting for a message.

|Name|Type|Description|
|----|----|-----------|
|contextSysID|String|The sys\_id value of the flow or subflow that is paused and waiting for a specific message to resume. The flow or subflow must include a Wait for Message action. See [Wait For Message action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/wait-for-message-action.md).|
|message|String|The text string to send to the waiting flow or subflow. If this message value matches the message value listed in the Wait for Message action, then the flow or subflow resumes running. See [Wait For Message action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/wait-for-message-action.md).|
|payload|String|The text string output value to send to the waiting flow. The flow or subflow can use the payload as an input when it resumes running. For example, you could specify a reason why a record was reopened or that a new approval was required.|

|Type|Description|
|----|-----------|
|None| |

This example sends the message `Resume Flow` to restart a paused flow. The paused flow can then use the payload value as data elsewhere in the flow.

```
(function() {
    try {
      // var change = '154a6320db9b12102166e229139619fc';    // Example sys_id of change record
      var pausedFlowId = '6e9bab60949b1210dda11cd237cd955d'; // Example sys_id of a paused flow
      var resumeMessage = 'Resume Flow';                     // Message that paused flow is waiting for
      var payload = 'Resubmitted for approval';              // Data to send back to flow
      var result = sn_fd.FlowAPI
      .sendMessage(pausedFlowId, resumeMessage, payload);    // Send a message to the paused flow
    } catch (ex) {
      var message = ex.getMessage();
      gs.error(message);
    }
  })();  
  
```

Output:

This script doesn't produce any output of its own. When you run it from the **Scripts-Background** module, the system lists the operations and tables modified by the script. You can also see the results of the script output in the flow execution details of a Wait for Message action.

```
[0:00:00.074] Script completed in scope global: script
Script execution history and recovery available here
Operation	Table	                       Row Count
delete	   sys_flow_runtime_state_chunk	1
insert	   sys_flow_runtime_state_chunk	1
update	   sys_flow_context	            1
record-watcher asynchronous tracking complete - time: 3 ms. Executed responders: 1 
record-watcher asynchronous tracking complete - time: 3 ms. Executed responders: 1 
record-watcher asynchronous tracking complete - time: 3 ms. Executed responders: 1 

```

## FlowAPI - setEncryptedOutput\(String password\)

Builds password2 values inside a script step.

Identify an encrypted password2 value returned from a GlideRecord, enabling the system to display the value as a masked password rather than an encrypted string.

|Name|Type|Description|
|----|----|-----------|
|password|String|Encrypted password2 value.|

|Type|Description|
|----|-----------|
|String|Encrypted password2 value, recognised by the engine as a password value.|

This example returns value of a password2 field from a user record and stores in in a variable. This variable is passed into the setEncryptedOutput method, which is called using sn\_fd.GlideActionUtil.setEncryptedOutput. The instance recognises the returned value as a password.

```
(function execute(inputs, outputs) {
  // ...code...
  var now_GR = new GlideRecord('sys_user');
  now_GR.addQuery('first_name' , 'Abel');
  now_GR.query();
  now_GR.next();
  var pwVal = now_GR.getValue('pw2');
  outputs['usedSetEncrypted'] = sn_fd.GlideActionUtil.setEncryptedOutput(pwVal);
  outputs['justSetDirectly'] = pwVal;
})(inputs, outputs);
```

## FlowAPI - startAction\(String name, Map inputs\)

Runs an action from a server-side script asynchronously.

Execute an action from within a business rule, script include, or any other server-side script. Actions run using this method run asynchronously, so scripts using this method do not have access to any outputs created by the action. Use **executeAction** to run an action synchronously and access the outputs it generates.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** This method runs the action as the user who initiates the session.

|Name|Type|Description|
|----|----|-----------|
|name|String|The scope and name of the action to be executed, for example `global.action_name`.|
|inputs|Map|Name-value pairs that define action inputs. Use the input name, not the input label.|

|Type|Description|
|----|-----------|
|String|Sys Id of the context record for the action. Access the context record by navigating to the Flow Executions tab in Workflow Studio, selecting a flow execution, and clicking **Open Context Record**.|

This example uses sn\_fd.FlowAPI.startAction to execute an action called add\_comment in the sn\_itsm\_spoke scope. The inputs object contains a target record and a comment to add to that record. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {
  try {
    var inputs = {};
    inputs['ah_task'] = myTaskRecord; // GlideRecord of table: task 
    inputs['ah_comment'] ='Test Comment' ; // String 

    var contextId = sn_fd.FlowAPI.startAction('sn_itsm_spoke.add_comment', inputs);	
			
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
})();
```

## FlowAPI - startActionQuick\(String name, Map inputs\)

Runs an action from a server-side script asynchronously without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Wait support**

    This method does not support pausing the action to wait for conditions. Steps that pause for wait conditions such as Ask for Approval or Wait for Condition are not supported.

-   **MID Server support**

    This method does not support pausing an action to run from a MID Server.


**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

|Name|Type|Description|
|----|----|-----------|
|name|String|Scope and internal name of the action to execute. For example, `global.action_name`. Locate the **Internal name** field in the list of Workflow Studio actions.|
|inputs|Map|Name-value pairs that define action inputs. You can find the available action inputs and required data types under Inputs in the action outline. Use the input name, not the input label. For example, `{'table':'incident','sys_id':'a39d8e3cf0212300964feeefe80ff0ed'}`.|

|Type|Description|
|----|-----------|
|void| |

```
(function() {
	
  try {
    var grIncident = new GlideRecord('incident');
    grIncident.get('57af7aec73d423002728660c4cf6a71c');

    var inputs = {};
    inputs['variable'] = grIncident;

    sn_fd.FlowAPI.startActionQuick('global.update_record_test', inputs);

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
    }
	
})();
```

## FlowAPI - startFlow\(String name, Map inputs\)

Runs a flow from a server-side script.

Execute a flow from within a business rule, script include, or any other server-side script. Flows executed with this method run asynchronously.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** This method runs the flow as the user specified in flow properties.

|Name|Type|Description|
|----|----|-----------|
|name|String|The scope and name of the flow to be executed, for example `global.flow_name`.|
|inputs|Map|Name-value pairs that define trigger inputs. Use the input name, not the input label.|

|Type|Description|
|----|-----------|
|String|Sys Id of the context record for the flow. Access the context record by navigating to the Flow Executions tab in Workflow Studio, selecting a flow execution, and clicking **Open Context Record**.|

This example uses sn\_fd.FlowAPI.startFlow to execute a global flow called test\_flow. The code creates an inputs variable that contains inputs required by the flow. In this case, the current record and the table for the record. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {
 
  var now_GR = new GlideRecord('incident'); 
  now_GR.addQuery('number', 'INC0009009'); 
  now_GR.query(); 
  now_GR.next();

  try {
    var inputs = {};
    inputs['current'] = now_GR; // GlideRecord of table: Incident
    inputs['table_name'] = 'incident';

    var contextId = sn_fd.FlowAPI.startFlow('global.test_flow', inputs);	
	
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);  
  }
})();
```

## FlowAPI - startFlowQuick\(String name, Map inputs\)

Runs a flow from a server-side script asynchronously without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Run as System user**

    This method runs the flow as the System user. Setting the flow to run as the user who initiates the session, or impersonating a user, is not supported.

-   **Wait support**

    This method does not support pausing the flow to wait for conditions. Actions or flow logic that pause for wait conditions such as Ask for Approval, Wait for Condition, or Wait for a duration are not supported.

-   **MID Server support**

    This method does not support pausing a flow to run from a MID Server.


**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

|Name|Type|Description|
|----|----|-----------|
|name|String|Scope and internal name of the flow to execute. For example, `global.flow_name`. Locate the **Internal name** field in the list of Workflow Studio flows.|
|inputs|Map|Name-value pairs that define trigger inputs. You can find the available trigger inputs and required data types in the Trigger section of the flow. Use the input name, not the input label. For example, `{'table':'incident','sys_id':'a39d8e3cf0212300964feeefe80ff0ed'}`.|

|Type|Description|
|----|-----------|
|void| |

```
(function() {
	
  try {
    var grIncident = new GlideRecord('incident');
    grIncident.get('ed92e8d173d023002728660c4cf6a7bc');

    var inputs = {};
    inputs['current'] = grIncident;
    inputs['table_name'] = 'incident';
		
    sn_fd.FlowAPI.startFlowQuick('global.test_quick_flow', inputs);
		
  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
	}
	
})();
```

## FlowAPI - startSubflow\(String name, Map input\)

Runs a subflow from a server-side script.

Execute a subflow from within a business rule, script include, or any other server-side script. Subflows run using this method run asynchronously Scripts that include this method do not have access to outputs created by the flow. Use **executeSubflow** to run a subflow synchronously and access the outputs it generates.

**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

**Note:** This method runs the flow as the user specified in flow properties.

|Name|Type|Description|
|----|----|-----------|
|name|String|The scope and name of the subflow to be executed, for example `global.subflow_name`.|
|inputs|Map|Name-value pairs that define subflow inputs. Use the input name, not the input label.|

|Type|Description|
|----|-----------|
|String|Sys Id of the context record for the subflow. Access the context record by navigating to the Flow Executions tab in Workflow Studio, selecting a flow execution, and clicking **Open Context Record**.|

This example uses sn\_fd.FlowAPI.startSubflow to execute a global flow called test\_subflow. The code is wrapped in a try/catch statement to capture any errors that might occur when the flow executes.

```
(function() {
  try {
    var inputs = {};
    inputs['ah_task'] = myTaskRecord; // GlideRecord of table: task 
    inputs['ah_comment'] ='Test Comment' ; // String 

    var contextId = sn_fd.FlowAPI.startSubflow('global.test_subflow', inputs);

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }
	
})();
```

## FlowAPI - startSubflowQuick\(String name, Map inputs\)

Runs a subflow from a server-side script asynchronously without creating execution details or other related records. Improve performance by eliminating record-keeping overhead. Use this API to increase the speed of high-volume processing, for example multiple executions per second, in a production environment.

-   **Reporting &amp; records generated**

    This method does not create execution details and context records, regardless of Workflow Studio settings.

-   **Run as System user**

    This method runs the flow as the System user. Setting the flow to run as the user who initiates the session, or impersonating a user, is not supported.

-   **Wait support**

    This method does not support pausing the flow to wait for conditions. Actions or flow logic that pause for wait conditions such as Ask for Approval, Wait for Condition, or Wait for a duration are not supported.

-   **MID Server support**

    This method does not support pausing a flow to run from a MID Server.


**Note:** This API is replaced by [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#), which deprecates the existing methods used to build objects and execute Workflow Studio flows and actions. Use the getRunner\(\) method in the FlowAPI class to return a ScriptableFlowRunner object and use the associated methods. Use the ScriptableFlowRunner methods if you need to support domain separation.

|Name|Type|Description|
|----|----|-----------|
|name|String|Scope and internal name of the subflow to execute. For example, `global.subflow_name`. Locate the **Internal name** field in the list of Workflow Studio subflows.|
|inputs|Map|Name-value pairs that define subflow inputs. You can find the available subflow inputs and required data types under Inputs in the subflow. Use the input name, not the input label. For example, `{'table':'incident','sys_id':'a39d8e3cf0212300964feeefe80ff0ed'}`.|

|Type|Description|
|----|-----------|
|void| |

```
(function() {

  try {
    var grIncident = new GlideRecord('incident');
    grIncident.get('57af7aec73d423002728660c4cf6a71c');

    var inputs = {};
    inputs['variable'] = grIncident;

    sn_fd.FlowAPI.startSubflowQuick('global.test_quick_run_subflow', inputs);

  } catch (ex) {
    var message = ex.getMessage();  
    gs.error(message);
    }
	
})();
```

