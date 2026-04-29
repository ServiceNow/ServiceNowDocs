---
title: Use multiple timer activities in one workflow
description: Workflow timer activities store data independently of each other in an activity-specific scratchpad.
locale: en-US
release: australia
product: Workflow Activities
classification: workflow-activities
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow activities, Classic Workflow, Build workflows]
---

# Use multiple timer activities in one workflow

Workflow timer activities store data independently of each other in an activity-specific scratchpad.

Previously, all timer activities in a workflow accessed a single, shared scratchpad, which could lead to conflicts when adding multiple timer activities to one workflow.

Timer scratchpads entries hold these values:

-   workflow.scratchpad.endTime
-   workflow.scratchpad.realStartTime
-   workflow.scratchpad.retroactiveSecsLeft

**Related topics**  


[Timer workflow activities](https://www.servicenow.com/docs/access?context=c_TimerActivities&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

