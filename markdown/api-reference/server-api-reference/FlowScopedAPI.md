---
title: Flow - Scoped \(deprecated\)
description: The Flow API provides methods to run activated Workflow Studio flows.Ignores the trigger and runs an activated flow asynchronously.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Flow- Scoped \(deprecated\)

The Flow API provides methods to run activated Workflow Studio flows.

This API is deprecated and replaced by the [ScriptableFlowRunner - Scoped](../../ScriptableFlowRunnerScoped/concept/ScriptableFlowRunnerScopedAPI.md#) and [ScriptableFlowRunnerResult - Scoped](../../ScriptableFlowRunnerResultScoped/concept/ScriptableFlowRunnerResultScopedAPI.md#)APIs.

The Flow API can only be used in server scripts.

Use the `sn_fd` namespace to access the Flow API.

Before interacting with a flow using the Flow API, you must first create and activate the flow in the Workflow Studio interface. Because the Flow API only interacts with pre-built flows, there is no constructor for the class.

**Note:** To optimize instance performance, avoid calling these methods from an asynchronous business rule script. Instead, create a scheduled job record within the Workflow Studio UI.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Flow - startAsync\(String scopeName.flowName, Map flowInputs\)

Ignores the trigger and runs an activated flow asynchronously.

Asynchronous calls are non-blocking, allowing the client to execute other code in the script without having to wait for the flow to complete.

<table id="table_s1t_yn5_ncb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

scopeName.flowName

</td><td>

String

</td><td>

The application scope for the flow and the internal name of the flow to run. If scopeName is not included, the scope of the user currently logged in is used. Retrieve the internal name of the flow using the **Internal name** column on the Workflow Studio landing page.

</td></tr><tr><td>

flowInputs

</td><td>

Map

</td><td>

Name-value pairs in `<String, Object>` format that define record-based flow inputs.To call a flow with a record-based trigger, use the format:

```
var flowInputs = {};
flowInputs['current'] = glideRecord;
flowInputs['table_name'] = glideRecord.getTableName();
```

 The GlideRecord object must be named 'current'.

 To call a flow with a Service Catalog trigger, use the format:

```
var flowInputs = {};
flowInputs['request_item'] = glideRecord;
flowInputs['table_name'] = glideRecord.getTableName();
```

 The GlideRecord object must be named 'request\_item'.

</td></tr></tbody>
</table><table id="table_t1t_yn5_ncb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

PlanResponse object containing the following properties: -   contextId: sys\_id of the execution details record for the executed flow. Access the execution details by navigating to the Flow Executions tab in Workflow Studio and filtering by sys\_id.

 An exception occurs when the flow:

-   Does not exist within the specified application scope, or the flow or scope name has been misspelled.
-   Is not activated.
-   Exceeds the recursion limit set by the **com.glide.hub.flow\_engine.indirect\_recursion\_limit** system property. The default value is three.

</td></tr></tbody>
</table>```
//Example 1: Run a flow with a record-based trigger
(function startFlowAsync() {

	try {
		// You MUST fetch the GlideRecord that will be passed to the flow
		var glideRecordInput = new GlideRecord('sys_user');
		glideRecordInput.get('62826bf03710200044e0bfc8bcbe5df1');

		var flowInputs = {};
		flowInputs['current'] = glideRecordInput;
		flowInputs['table_name'] = glideRecordInput.getTableName();

		var result = sn_fd.Flow.startAsync('global.recordtriggeredflow', flowInputs);

		//The Sys ID of a flow execution (contextId)
		var contextId = result.contextId;

	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	}

})();

//Example 2: Run a flow with a schedule-based trigger
(function startFlowAsync() {

	try {
		var result = sn_fd.Flow.startAsync('global.scheduletriggeredflow');

		//The Sys ID of a flow execution (contextId)
		var contextId = result.contextId;

	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	}

})();

//Example 3: Run a flow with a Service Catalog trigger
(function startFlowAsync() {

	try {
		// You MUST fetch the GlideRecord that will be passed to the flow
		var glideRecordInput = new GlideRecord('sc_req_item');
		glideRecordInput.get(aeed229047801200e0ef563dbb9a71c2);

		var flowInputs = {};
		flowInputs['request_item'] = glideRecordInput;
		flowInputs['table_name'] = glideRecordInput.getTableName();

		var result = sn_fd.Flow.startAsync('global.catalogtriggeredflow', flowInputs);

		//The Sys ID of a flow execution (contextId)
		var contextId = result.contextId;

	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	}

})();

//Example 4: Run a flow with a MetricBase trigger
(function startMetricBaseFlowAsync() {

	try {

		var oilLevelTriggerRecord = new GlideRecord('oil_levels');
		oilLevelTriggerRecord.get('a4b3622bc72113007b237f48cb97635f');

		var metricTriggerDefinition = new GlideRecord('sys_metric_trigger_definition');
		metricTriggerDefinition.get('21f2eae7c72113007b237f48cb976352');

		var event_time = oilLevelTriggerRecord.getValue('sys_created_on');
		var level = 4;

		var metricBaseFlowInputs = {};
		//The record that triggered the metric event
		metricBaseFlowInputs['current'] = oilLevelTriggerRecord;
		//The MetricBase Trigger Definition record
		metricBaseFlowInputs['metric'] = metricTriggerDefinition;
		//The time that the 'record' reached a specific metric event level and triggered this flow
		metricBaseFlowInputs['event_time'] = event_time;
		//The target event level to reach in order for a metric flow to trigger
		metricBaseFlowInputs['level'] = level;

		var result = sn_fd.Flow.startAsync('global.metricbasedtriggeredflow', metricBaseFlowInputs);

		//The Sys ID of a flow execution (contextId)
		var contextId = result.contextId;

	} catch (ex) {
		var message = ex.getMessage();
		gs.error(message);
	}

})();
```

