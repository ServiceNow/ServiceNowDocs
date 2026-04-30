---
title: DevOpsOrchestrationToolIntegrationHandler - Scoped
description: The DevOpsOrchestrationToolIntegrationHandler API enables processing of payloads from custom DevOps tools.Returns the value of the orchestrationTaskName parameter from the payload for the POST /devops/tool/\{capability\} endpoint.Checks if this handler is valid for the specified tool.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DevOpsOrchestrationToolIntegrationHandler- Scoped

The DevOpsOrchestrationToolIntegrationHandler API enables processing of payloads from custom DevOps tools.

A custom DevOps tool is any tool that doesn't have an integration with DevOps. For a list of tools that have DevOps integrations, see [DevOps Change Velocity integrations](https://www.servicenow.com/docs/access?context=dev-ops-overview&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

This API enables the processing of payloads that are used by the REST endpoint [DevOps - POST /devops/tool/\{capability\}](../../../../../integrate/inbound-rest/concept/devops-api.md#). You must implement the methods of this API in a script include before calling the POST /devops/tool/\{capability\} endpoint.

This API executes in the `sn_devops` namespace. For more information about DevOps, see [DevOps Config](https://www.servicenow.com/docs/access?context=devops-config-landing-page&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DevOpsOrchestrationToolIntegrationHandler - getNativeIdForOrchestrationTask\(Object payload\)

Returns the value of the **orchestrationTaskName** parameter from the payload for the POST /devops/tool/\{capability\} endpoint.

You must implement this method in a script include before calling the REST endpoint [DevOps - POST /devops/tool/\{capability\}](../../../../../integrate/inbound-rest/concept/devops-api.md#).

|Name|Type|Description|
|----|----|-----------|
|payload|Object|Payload containing data from the custom tool which is accepted by the REST endpoint POST /devops/tool/\{capability\}, where **capability** is `orchestration`.|

|Type|Description|
|----|-----------|
|String|Value of the **orchestrationTaskName** parameter from the payload.|

In this example, a script include named `DevOpsOrchestrationCustomToolIntegrationHandler` implements the methods handleTool and getNativeIdForOrchestrationTask. The getNativeIdForOrchestrationTask method is implemented to return the value of the **orchestrationTaskName** parameter from the payload for POST /devops/tool/\{capability\}.

```
var DevOpsOrchestrationCustomToolIntegrationHandler = Class.create(); 

DevOpsOrchestrationCustomToolIntegrationHandler.prototype = {     

    handleTool: function(toolName) { 
        if (!gs.nil(toolName) && toolName == 'sn_devops_custom_tool') 
            return true; 
        return false; 
    }, 

    getNativeIdForOrchestrationTask: function(payload) { 
        return payload.orchestrationTaskName; 
    }, 

    type: 'DevOpsOrchestrationCustomToolIntegrationHandler' 

}; 
```

## DevOpsOrchestrationToolIntegrationHandler - handleTool\(String toolName\)

Checks if this handler is valid for the specified tool.

You must implement this method in a script include before calling [DevOps - POST /devops/tool/\{capability\}](../../../../../integrate/inbound-rest/concept/devops-api.md#).

<table id="table_gtf_1vm_ctb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

toolName

</td><td>

String

</td><td>

Name of the tool.Table: *Tool Name* field of the DevOps Tool Integration \[sn\_devops\_tool\_integration\] table

</td></tr></tbody>
</table><table id="table_htf_1vm_ctb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether this handler is valid for the specified tool.Possible values:

-   true: This handler can be used for the specified tool.
-   false: This handler can't be used for the specified tool.

</td></tr></tbody>
</table>In this example, a script include named `DevOpsOrchestrationCustomToolIntegrationHandler` implements the methods handleTool and getNativeIdForOrchestrationTask. The handleTool method is implemented to check that the passed in name is for the correct tool. Replace `'sn_devops_custom_tool'` with the name of the tool that you're using.

```
var DevOpsOrchestrationCustomToolIntegrationHandler = Class.create(); 

DevOpsOrchestrationCustomToolIntegrationHandler.prototype = {     

  handleTool: function(toolName) { 
    if (!gs.nil(toolName) && toolName == 'sn_devops_custom_tool') 
      return true; 
    return false; 
  }, 

  getNativeIdForOrchestrationTask: function(payload) { 
    return payload.orchestrationTaskName; 
  }, 

  type: 'DevOpsOrchestrationCustomToolIntegrationHandler' 

};
```

