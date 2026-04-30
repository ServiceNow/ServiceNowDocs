---
title: Work notes
description: Work notes are an important part of the state flow process and are used to communicate information about state transitions.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use state flows, State flows, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Work notes

Work notes are an important part of the state flow process and are used to communicate information about state transitions.

The state flow adds these work notes to the Work notes field of any task making this transition.

These rules apply to state flow work notes:

-   For a state flow with no Starting state, the work note is added every time the task transitions to the Ending state.
-   For a state flow with a Starting state and an Ending state, the work note is added only when the task transitions from that starting state to that ending state.
-   If two state flows with work notes have the same Ending state, but only one has a Starting state, the system adds the work notes from the state flow with the starting state. This better matches the state flow work note to the more important transition between specific starting and ending states.

**Parent Topic:**[Use state flows](c_UseStateFlows.md)

**Related topics**  


[Use state flows](c_UseStateFlows.md)

[Create a state flow](../task/t_CreateAStateFlow.md)

