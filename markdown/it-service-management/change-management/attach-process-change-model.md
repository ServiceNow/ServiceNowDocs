---
title: Attach a process for Change model states
description: You can attach a process with defined conditions to the Change model states to enable state transitions.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a Change model, Configure, Change Management, IT Service Management]
---

# Attach a process for Change model states

You can attach a process with defined conditions to the Change model states to enable state transitions.

This process can be done by using one of the following methods:

-   ServiceNow® Workflow Studio: See [Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md)
-   Business Rules: See [Business rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/business-rules-classic/c_BusinessRules.md)

Change flows for default Change models are available in Workflow Studio. For more information on default Change flows, see [Change flows](change-flows.md).

## Evaluating a Change model

When your flow is completed, you can evaluate the Change model to process any automated transitions. In Workflow Studio, the **Evaluate Change Model** action is used to evaluate the Change model.

When using Business Rules, you can use the script to evaluate the Change model. For example, see the **Change Registration: Auto State Change** business rule on the change\_request table.

You can also evaluate a Change model for a specific Change request using this event:

|Event name|Parameter|Description|
|----------|---------|-----------|
|change\_model.evaluate|Change Request sys\_id|Process that may affect the state of the Change request but doesn't change the Change request record.|

**Parent Topic:**[Create a Change model](../task/create-a-change-model.md)

