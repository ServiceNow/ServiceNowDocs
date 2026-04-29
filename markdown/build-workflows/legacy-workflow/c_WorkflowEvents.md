---
title: Workflow events
description: The system employs two types of events: registered platform events and workflow events.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workflow management, Classic Workflow, Build workflows]
---

# Workflow events

The system employs two types of events: registered platform events and workflow events.

## Registered platform events

Registered events are created in business rules and are used for such tasks as sending email notifications when records are inserted into the database. Workflow events are registered within workflows only and are not used anywhere else in the platform. Registered platform events can be triggered by a workflow for external use, but cannot be used within a workflow.

## Workflow events

Workflow events follow different rules than platform events that are registered using the event registry. Platform events are entered into the Event Registration \[sysevent\_register\] table and are available for platform processes to use. Workflow events are triggered exclusively for the workflow engine and are used only to direct the work of executing workflow contexts. When an event is registered in a workflow, it is attached to a currently executing activity in the **registered\_events** column of the Workflow Executing Activity \[wf\_executing\] table.

Workflow events also can be broadcast to a workflow from any scripting source that has access to the workflow context, such as a script include or a **Run Script** activity. In this case, the event, such as **cancel**, is passed to all records in the Workflow Executing \[wf\_executing\] table for a specific context.

Whether by registry or by broadcast, an event is handled by the activity definition associated with the currently executing activity. Each activity definition comes with a set of handlers. For example, most activities come with onExecute, onCancel, and onUpdate event handlers. As an example of a more specific event, the **Approval - User** activity also comes with onDetermineApprovalState, which is specific to the work of the approval activity.

## Multiple parallel events

A single workflow can have multiple event threads running concurrently, such as when a workflow has timers that overlap on separate workflow branches. If any additional thread completes before the first thread, the system stores event information from the additional thread on the Workflow Queued Commands \[wf\_command\] table. After the first thread completes, the system retrieves the information stored by the additional thread and proceeds through the workflow with the event information from each thread.

-   **[Workflow events in the base system](../reference/r_WorkflowEventsInTheBaseSystem.md)**  
Several workflow events are available in the base system.

**Parent Topic:**[Workflow management](managing-workflows.md)

