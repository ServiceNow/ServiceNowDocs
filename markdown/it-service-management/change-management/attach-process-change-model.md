---
title: Attach a process for Change model states
description: You can attach a process with defined conditions to the Change model states to enable state transitions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/attach-process-change-model.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [change model evaluation, automatic state transition, evaluateChangeModel]
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Attach a process for Change model states

You can attach a process with defined conditions to the Change model states to enable state transitions.

A change model defines the states of a change request and the conditions that allow a change request to move between states. The conditions alone don't move a change request. A process, either a flow or a business rule, must evaluate the change model so that any automatic transition whose conditions are met is applied.

Attach a process by using one of the following methods:

-   Workflow Studio flow: Use a flow when you want a low-code process that runs the **Evaluate Change Model** action at defined points. See [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md).
-   Business rule: Use a business rule when the evaluation must run every time the change request record is updated. See [Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_BusinessRules.md).

Change flows for default Change models are available in Workflow Studio. For more information on default Change flows, see [Change flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-flows.md).

## How automatic transitions are evaluated

1.  You define transition conditions for each model state. For more information, see [Create predefined transition condition types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-predefined-transition-condition-type.md).
2.  You attach a flow or business rule that evaluates the change model.
3.  The process runs, for example when the change request is updated or a task is closed.
4.  The system checks the automatic transitions for the current state and moves the change request to the first state whose conditions are met.

For example, the **Change Registration: Auto State Change** business rule on the change\_request table evaluates the change model after each update. The change request moves to the next state as soon as its transition conditions are met.

## Evaluating a Change model

When your flow is completed, you can evaluate the Change model to process any automated transitions. In Workflow Studio, the **Evaluate Change Model** action is used to evaluate the Change model.

When using Business Rules, you can use the script to evaluate the Change model. For example, see the **Change Registration: Auto State Change** business rule on the change\_request table.

You can also evaluate a Change model for a specific Change request using this event:

|Event name|Parameter|Description|
|----------|---------|-----------|
|change\_model.evaluate|Change Request sys\_id|Process that may affect the state of the Change request but doesn't change the Change request record.|

**Parent Topic:**[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md)

**Related topics**  


[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md)

[Configure state model transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ConfigStateModelTransit.md)

