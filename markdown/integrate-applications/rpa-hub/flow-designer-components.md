---
title: Flow Designer components
description: The Flow Designer components let you invoke flows, subflows, and actions from Workflow Studio and use them as part of a workflow. You can also use these components to determine a flow's output or execution status.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ServiceNow, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Flow Designer components

The Flow Designer components let you invoke flows, subflows, and actions from Workflow Studio and use them as part of a workflow. You can also use these components to determine a flow's output or execution status.

-   **[Use the InvokeFlow component](../task/use-rpahub-flowdesigner-invokeflow.md)**  
Invoke or call a flow that is available in Workflow Studio by using the InvokeFlow component of RPA Desktop Design Studio. Generate the context ID of the flow and use the ID in other flow designer components to get the execution status and output.
-   **[Use the GetExecutionStatus component](../task/use-rpahub-flowdesigner-getexecutionstatus.md)**  
Use the GetExecutionStatus component to determine the execution status of a flow or a subflow in Workflow Studio.
-   **[Use the GetOutputs component](../task/use-rpahub-flowdesigner-getoutputs.md)**  
Use the GetOutputs component to get the output of a flow or a subflow in Workflow Studio.
-   **[Use the InvokeSubFlow component](../task/use-rpahub-flowdesigner-invokesubflow.md)**  
The InvokeSubFlow component returns the context ID of a subflow in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of a subflow.
-   **[Use the InvokeAction component](../task/invoke-action-component.md)**  
The InvokeAction component returns the context ID of an action in Workflow Studio so you can use it in other components. For example, you can use the context ID to get the execution status or the output of an action.
-   **[Properties of the Flow Designer components](../reference/properties-flow-designer-components.md)**  
To set the properties of a Flow Designer component, double-click the component and enter the values in the Properties pane.

**Parent Topic:**[ServiceNow](servicenow.md)

