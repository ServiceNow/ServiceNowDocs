---
title: Work notes in state flows
description: Work notes are an important part of the state flow process and are used to communicate information about state transitions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [State flow customization, Service management states, Service Management]
---

# Work notes in state flows

Work notes are an important part of the state flow process and are used to communicate information about state transitions.

The state flow adds work notes into the **Work notes** field of any task making this transition. For example, you might include the note, "Task rejected by agent" in the **Reject** state flow, which occurs when the task moves from **Assigned** to **Pending Dispatch**. If an agent rejects the task and fails to enter a work note, this note tells the dispatcher why the task reappeared in the dispatch queue. Work notes added by an agent rejecting the task are appended to the work notes that are inherited from the state flow.

These rules apply to state flow work notes:

-   For a state flow with no **Starting state**, the work note is added every time the task transitions to the **Ending state**.
-   For a state flow with a **Starting state** and an **Ending state**, the work note is added only when the task transitions from that starting state to that ending state.
-   If two state flows with work notes have the same **Ending state**, but only one has a **Starting state**, the system adds the work notes from the state flow with the starting state. This better matches the state flow work note to the more important transition between specific starting and ending states. In the example here, the work note information is more pertinent to a task moving from **Assigned** to **Pending Dispatch** than to a task that reaches the Pending Dispatch state from an undetermined beginning state.

**Parent Topic:**[State flow customization](c_StateFlowCustomization.md)

**Related topics**  


[State flow customization](c_StateFlowCustomization.md)

[Request states](../../planning-and-policy/reference/r_SMRequestStates.md)

[Request task states](../../planning-and-policy/reference/r_SMRequestTaskStates.md)

