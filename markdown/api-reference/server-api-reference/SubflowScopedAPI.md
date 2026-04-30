---
title: Subflow - Scoped \(deprecated\)
description: The Subflow API provides methods to run published Workflow Studio subflows.Runs a published subflow asynchronously.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Subflow- Scoped \(deprecated\)

The Subflow API provides methods to run published Workflow Studio subflows.

This API is deprecated and replaced by the [FlowAPI - Scoped, Global](../../ScriptableFlowAPI/concept/ScriptableFlowAPI.md#).

The Subflow API can only be used in server scripts.

Use the `sn_fd` namespace to access the Subflow API.

Before interacting with a subflow using the Subflow API, you must first create and publish the subflow in the Workflow Studio interface. Because the Subflow API only interacts with pre-built subflows, there is no constructor for the class.

**Note:** To optimize instance performance, avoid calling these methods from an asynchronous business rule script. Instead, create a scheduled job record within the Workflow Studio UI.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Subflow - startAsync\(String scopeName.subflowName, Map inputs\)

Runs a published subflow asynchronously.

Asynchronous calls are non-blocking, allowing the client to execute other code in the script without having to wait for the subflow to complete.

|Name|Type|Description|
|----|----|-----------|
|scopeName.subflowName|String|The application scope for the subflow and the internal name of the subflow to run. If scopeName is not included, the scope of the user currently logged in is used. Retrieve the internal name of the subflow using the **Internal name** column on the Workflow Studio landing page.|
|inputs|Map|Name-value pairs that define subflow inputs. If a subflow includes mandatory inputs, they must be included. For inputs of Reference or Document ID field types, use a GlideRecord object as the value.|

<table id="table_tlq_v1v_ncb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

PlanResponse object containing the following properties: -   contextId: Sys\_id of the execution details record for the executed subflow. Access the execution details by navigating to the Flow Executions tab in Workflow Studio and filtering by sys\_id.

 An exception occurs when the subflow:

-   Does not exist within the specified application scope, or the subflow or scope name has been misspelled.
-   Is not published.
-   Is passed an input object that does not match the subflow inputs.
-   Exceeds the recursion limit set by the **com.glide.hub.flow\_engine.indirect\_recursion\_limit** system property. The default value is three.

</td></tr></tbody>
</table>```
//Run a subflow that takes two inputs: user, a sys_user record, and laptop_welcome_message, a string.
(function startSubflowAsync() {

  try {
    var userToProvisionFor = new GlideRecord('sys_user');
    userToProvisionFor.get('62826bf03710200044e0bfc8bcbe5df1');

    var inputs = {};
    inputs['user'] = userToProvisionFor;
    inputs['laptop_welcome_message'] = 'Welcome Onboard!!';

    var result = sn_fd.Subflow.startAsync('sn_devstudio.provisionlaptop', inputs);

    //The Sys ID of a flow execution (contextId)
    var contextId = result.contextId;

  } catch (ex) {
    var message = ex.getMessage();
    gs.error(message);
  }

})();
```

