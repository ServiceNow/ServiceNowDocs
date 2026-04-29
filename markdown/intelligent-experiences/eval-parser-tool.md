---
title: Agentic evaluation parser tool
description: Use the outputs of the agentic evaluation parser tool in your scripts for custom metrics to customize the criteria for effective AI agents and agentic workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-08-19"
reading_time_minutes: 3
breadcrumb: [Reference, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Agentic evaluation parser tool

Use the outputs of the agentic evaluation parser tool in your scripts for custom metrics to customize the criteria for effective AI agents and agentic workflows.

## Parser tool overview

The agentic evaluation parser tool extracts structured execution data from the execution logs of an agentic workflow or AI agent. You can use the information gathered by the tool to create custom metrics that use scripts to evaluate agentic workflows.

The parser tool returns structured AI agent or agentic workflow execution data within the **output.payload** object, which contains the following:

-   **executionInputs**: A JSON object that contains initial workflow setup information, such as the names and instructions of agents and tools and the initial user utterance
-   **executionOutputs**: A JSON object with AI agent actions and tool execution results
-   **executionMessages**: A JSON object array of user-facing conversation flow and system responses
-   **executionPlanDetails**: A JSON object of execution metadata, such as status, sys\_ids, and configuration values

```
{
     "output": {
 "payload": {
  "executionInputs": { ... },
  "executionOutputs": { ... },
  "executionMessages": [ ... ],
  "executionPlanDetails": { ... }
 }
}

```

## Accessing the parser tool's output

To view the complete parser tool output for testing and development, perform the following steps.

-   Navigate to the Script Editor view in your custom metric guided setup.
-   Select **Run Test**.
-   Wait for the test to complete.
-   View the complete JSON output in the Tools section of the test results.

Reviewing the parser tool's output before designing your custom metric enables you to inspect the data structure before implementing any specific logic.

## executionInputs data structure

The executionInputs attribute contains a JSON object with the following structure:

```
"executionInputs": {
 "agenticWorkflow": "(name of agentic workflow)",
 "description": "(descriptions for agentic workflow)",
 "instructions": "(list of steps for agentic workflow)", 
 "utterance": "(initial user utterance)", 
 "agents": [ 
  { 
   "name": "(AI agent name)",  
   "instructions": "(list of steps for AI agent)", 
   "tools": [ 
    { 
     "name": "(tool name)", 
     "description": "(tool description)", 
     "executionMode": "(execution mode, either Autonomous or Supervised)", 
     "inputs": { ... } 
    }, 
    { ... }, ... 
   ]
  }, 
  { ... }, ... 
 ]
}
```

## executionOutputs data structure

The executionOutputs attribute contains a JSON object with the following structure:

```
"executionOutputs": {
 "agents": [ 
  { 
   "name": "(AI agent name)", 
   "subTask": { ... }, 
   "tools": [ 
    { 
     "name": "(tool name)", 
     "inputs": { ... }, 
     "output": { ... }
    }
   ]
  }, 
  { ... }, ... 
 ]
}
```

## executionMessages data structure

The executionOutputs attribute contains an array of JSON objects with the following structure:

```
"executionMessages": [ 
 { 
  "role": "(Message sender, either 'agent' or 'user')", 
   "message": "(Content of message)", 
   "order": "(Sequence number indicating order of message in the conversation)"
  }, 
  { ... }, ... 
]
   
```

## executionPlanDetails data structure

The executionPlanDetails attribute contains a JSON object with the following structure:

```
"executionPlanDetails": { 
    "state": "(Current execution status)", 
    "runType": "(Type of execution)", 
    "conversationId": "(sys_id of conversation)", 
    "relatedTask": "(sys_id of the associated task or record)", 
    "relatedTaskTable": "(Table name where the related task is stored)", 
    "context": { ... } (May be null)
    "builtInTools": [ { ... } ]
    }
   
```

This section provides execution metadata for tracking workflow performance, debugging issues, and correlating executions with specific tasks or conversations.

The possibilities for runType include the following:

-   API
-   Chat
-   Evaluation
-   Testing
-   Trigger

## Using parser tool output in metric scripts

The parser tool data is available in your metric script through the **context** parameter. Access the structured data using the following code:

```
// Access the parser tool output from context
var parserToolOutput = context['AgenticExecutionParserTool.output'];
if (typeof parserToolOutput == "string") {
 parserToolOutput = JSON.parse(parserToolOutput);
}
var parserToolPayload = parserToolOutput.payload;
var parserToolStatus = parserToolOutput.status;
    
// Extract individual sections from payload
var inputs = parserToolPayload.executionInputs;
var outputs = parserToolPayload.executionOutputs;
var messages = parserToolPayload.executionMessages;
var planDetails = parserToolPayload.executionPlanDetails;
   
```

