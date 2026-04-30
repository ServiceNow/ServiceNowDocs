---
title: Agent work and schedule status
description: View an agent's work status and schedule status as they complete their tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Agent work and schedule status

View an agent's work status and schedule status as they complete their tasks.

## Work status

To evaluate the agent's work status, the system checks the action that the agent takes when updating a task and interprets it as a status.

An agent's work status can be one of the following:

-   On route
-   On site
-   Off shift

For example, when the agent starts travel to a task, the system considers the agent's status as **On route**. When the agent starts to work on a task, the agent's status is updated to **On site**. When an agent closes or cancels a task, the agent's status is updated to **None** in preparation for travel to the next task.

Off shift agent status indicates that the Field Service agent doesn't have any assigned tasks scheduled for the day.

You can view an agent's work status in the contextual side panel that opens when you click the agent's pin in the dispatch map or in an agent's user record. To display agent work status in the user record, navigate to **User Administration** &gt; **Users** and configure the User form to show the **Work agent status** field. This action puts the status field on all user records.

## Schedule status

When you click an agent pin in the dispatch map, the agent profile appears. If a location shows more than one agent, you can select an agent to display their profile. You can view the status of the agent's schedule, which could be any of the following:

-   Ahead of schedule
-   On time
-   Behind schedule, less than 30 minutes
-   Behind schedule, between 30 to 60 minutes
-   Behind schedule, more that an hour

To display the agent schedule status in the user lists and records, navigate to **User Administration** &gt; **Users** and configure the User list and form to show the **On schedule** field. This action puts the schedule status field on all user records.

A Field Service Agent’s schedule status is determined when the agent selects start travel on the Mobile Agent Application. The Field Service Agent’s schedule status table below shows what the agent status will be based on when they select start travel.

|Agent status|When start travel was selected|
|------------|------------------------------|
|Ahead of schedule|20 minutes before the scheduled start travel time|
|On time|Within 3 minutes of the scheduled start travel time|
|Behind schedule, less than 30 minutes|20 minutes after the scheduled start travel time|
|Behind schedule, between 30 to 60 minutes|40 minutes after the scheduled start travel time|
|Behind schedule, more that an hour|70 minutes after the scheduled start travel time|

