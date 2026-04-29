---
title: Define the agent criteria for Universal Task
description: Define the criteria for an agent so that the agent can access the parent table for Universal Task. The default criteria is that agents must have write access to the parent table.
locale: en-US
release: australia
product: Universal Task
classification: universal-task
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring your service, Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Define the agent criteria for Universal Task

Define the criteria for an agent so that the agent can access the parent table for Universal Task. The default criteria is that agents must have write access to the parent table.

## Before you begin

Role required: admin

## About this task

By using an extension point, you can add more conditions for agents to qualify as Universal Task agents. If this extension point is not implemented, agents with write access to the parent table are treated as UT agents for the parent table by default.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the API name column, search for sn\_uni\_task.UniversalTaskParentAccess.

3.  To create an extension point script that defines the agent criteria for your service, click **Create Implementations** in the related link.

    To know more about extension points, see .

4.  Specify the criteria for an agent to have access to the parent table.

    For example, you might want to ensure that the agent belongs to a specific assignment group in addition to having write access for the parent table.


**Parent Topic:**[Configuring your service for Universal Task](../concept/config-service-for-ut.md)

**Previous topic:**[Add a Task tab on the Standard Ticket page](config-stdtktpage-for-ut.md)

**Next topic:**[Configure Universal Task for your service](config-ut-for-service.md)

