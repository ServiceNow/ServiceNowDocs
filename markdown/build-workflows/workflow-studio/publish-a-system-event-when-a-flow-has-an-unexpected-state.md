---
title: Publish a system event for an unexpected state
description: Publish a system event when a flow enters the error, cancelled, or presumed interrupted states. Use the default event name or specify a custom event name.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/publish-a-system-event-when-a-flow-has-an-unexpected-state.html
release: brazil
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
breadcrumb: [Flow administration, Configure flows, Flows, subflows, and actions, Workflow Studio, Build workflows]
---

# Publish a system event for an unexpected state

Publish a system event when a flow enters the error, cancelled, or presumed interrupted states. Use the default event name or specify a custom event name.

## Before you begin

Role required: flow\_designer, flow\_operator, or flow\_admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Administration** &gt; **Settings** &gt; **.**.

2.  Select **New**.

3.  From **Flow/SubFlow/Action**, select Flow.

4.  From **Document**, select the flow that you want to publish a system event for when it enters an unexpected state.

    \[Omitted image "publish-flow-state-events-01.png"\] Alt text: Select a specific flow to configure its settings

5.  Expand the section **Flow Execution State Events**.

6.  Select the flow states where you want to publish a system event.

    \[Omitted image "publish-flow-state-events-02.png"\] Alt text: Options to publish events for error, cancelled, and presumed interrupted

    |Field|Description|
    |-----|-----------|
    |Publish error events|Publish a system event when a flow enters the Error state.|
    |Publish cancellation events|Publish a system event when a flow enter the Cancelled state.|
    |Published presumed interrupted events|Publish a system event when a flow enters the Presumed Interrupted state.|

7.  In **Event name**, enter a custom event name.

    These are the default system event names.

    -   **flow.state.error**
    -   **flow.state.cancelled**
    -   **flow.state.interrupted**
8.  Select **Submit**.


## Result

Workflow Studio publishes the appropriate system event when the flow enters the specified unexpected state of error, cancelled, or presumed interrupted. You can review the **Parm2** field of the system event to see a JSON payload describing the flow context.

```json
{
  "contextId": "abc123...",
  "flowId": "def456...",
  "flowName": "My Automated Flow",
  "previousState": "IN_PROGRESS",
  "currentState": "ERROR",
  "errorMessage": "Connection timeout",
  "cancellationReason": "",
  "runTimeMs": 1542,
  "engineMajorVersion": 2,
  "domainId": "global",
  "createdBy": "admin",
  "callingSource": "flow_trigger"
}
```

## What to do next

Register the system event. For more information about registering a system event, see [Register an event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/system-events/t_RegisterAnEvent.md). After the system event is registered, you can create a script action or a notification to automate the response to the event. For more information about script actions, see [Script actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/system-events/r_ScriptActions.md).

**Parent Topic:**[Flow administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/workflow-studio/flow-administration.md)

