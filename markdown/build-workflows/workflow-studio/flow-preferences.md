---
title: User preferences for flows
description: Enable or disable user preferences for flow to change options available to Workflow Studio.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# User preferences for flows

Enable or disable user preferences for flow to change options available to Workflow Studio.

|Flow preference|Description|
|---------------|-----------|
|Show triggered flows|Option to show flows with a trigger from the subflow picker. By default, this option is disabled, and the subflow picker hides triggered flows from the subflow picker.|
|Show store spokes|Option to show Workflow Studio content from the ServiceNow Store from the action picker. By default, this option is enabled, which displays Workflow Studio content from ServiceNow Store spokes you have already installed.|
|Show inline script toggle.|Option to add or edit inline scripts when configuring an action input. By default this options is enabled, and you can add or edit inline scripts.|
|Show advanced connection options|Option to show advanced connection properties for actions that use connection aliases or inline connections. By default, this option is disabled.|
|Show flows as diagrams|Option to show all flows in the flow diagramming view. By default this option is disabled, and all flows open in the descriptive text view.|
|Auto Refresh Tests|Option to create an Asynchronous Message Bus \(AMB\) channel for test runs of flows and actions. The AMB channel listens for state changes of execution details that are in a waiting state. When the execution details are done, the AMB channel closes and sets the state to complete. By default, this option is disabled, and you must manually update execution details.|
|Show recommendations|Option to show flow recommendations to build a flow. The system generates recommendations based on the current position in the flow and the flow component names listed before. By default, this option is enabled. For more information about flow recommendations, see .|

**Parent Topic:**[Flows, subflows, and actions reference](flow-designer-reference.md)

**Related topics**  


[Set flow user preferences](../task/set-flow-user-preferences.md)

