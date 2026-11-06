---
title: Attach a process for Change model states
description: You can attach a process with defined conditions to the change model states to enable state transitions.
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

You can attach a process with defined conditions to the change model states to enable state transitions.

A change model defines the states of a change request and the conditions that allow a change request to move between states. The conditions alone don't move a change request. A process, either a flow or a business rule, must evaluate the change model so that any automatic transition whose conditions are met is applied.

Attach a process by using one of the following methods:

-   Workflow Studio flow: Use a flow for a low-code process that runs the **Evaluate Change Model** action at defined points. See [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md).
-   Business rule: Use a business rule when the evaluation must run every time the change request record is updated. See [Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/c_BusinessRules.md).

Change flows for default change models are available in Workflow Studio. For more information on default change flows, see [Change flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/change-flows.md).

## Automatic transition evaluation

1.  You define transition conditions for each model state. For more information, see [Create predefined transition condition types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-predefined-transition-condition-type.md).
2.  You attach a flow or business rule that evaluates the change model.
3.  The process runs, for example when the change request is updated or a task is closed.
4.  The system checks the automatic transitions for the current state and moves the change request to the first state whose conditions are met.

For example, the **Change Registration: Auto State Change** business rule on the Change Request \[change\_request\] table evaluates the change model after each update. The change request moves to the next state as soon as its transition conditions are met.

## Evaluating a change model

After your flow completes, you can evaluate the change model to process any automatic transitions. In Workflow Studio, use the **Evaluate Change Model** action to evaluate the change model.

When using business rules, you can use a script to evaluate the change model. For example, see the **Change Registration: Auto State Change** business rule on the Change Request \[change\_request\] table.

You can also evaluate a change model for a specific change request by using the event in the following table.

|Event name|Parameter|Description|
|----------|---------|-----------|
|change\_model.evaluate|Change Request sys\_id|Process that may affect the state of the change request but doesn't change the change request record.|

**Parent Topic:**[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md)

**Related topics**  


[Create a Change model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-a-change-model.md)

[Configure state model transitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_ConfigStateModelTransit.md)

