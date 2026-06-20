---
title: Suggest agents to assign to a work order task
description: Quickly sort a list of the best agents to assign a work order task based on the criteria that you choose from.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/field-service-management/assignment-assistance.html
release: xanadu
product: Field Service Management
classification: field-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Suggest agents to assign to a work order task

Quickly sort a list of the best agents to assign a work order task based on the criteria that you choose from.

## Before you begin

Assignment assistance 

Role required: wm\_dispatcher

Dynamic Scheduling must be enabled in order to use Assignment assistance. For more information see, [Configuring Dynamic Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/field-service-scheduling/Configure-dynamic-scheduling.md).

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Select **Dispatcher Workspace**.

3.  In the task panel, select the More Actions icon \(\[Omitted image "more\_actions.png"\] Alt text: more actions\).

4.  Select **Assignment assistance**.

5.  Sort the agent list based on the criteria that you want.

    |Sort option|Description|
    |-----------|-----------|
    |Best Match|Best match is the default sorting method. Match percentage is calculated the same way that Dynamic Scheduling calculates agents to assign tasks to. For more information, see [Matching criteria for task filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/field-service-management/field-service-scheduling/task-assignment-matching-criteria.md).|
    |Distance|Sorts agents based on how far each agent is from the work order task.|
    |Skills|Sorts agents based on the number of required skills that each agent has. Agents with more skills are at the top.|
    |Parts|Sorts agents based on how many required parts each agent has. Agents with the most parts to complete the task are at the top.|
    |Earliest start time|Sorts agents based on how quickly they can start the work order task.|
    |Earliest end time|Sorts agents based on how quickly they can complete the work order task.|

6.  Select the agent for which you want to assign the work order task.

7.  Select **Save**.


