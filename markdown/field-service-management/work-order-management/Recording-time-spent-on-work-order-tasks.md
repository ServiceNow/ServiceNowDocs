---
title: Recording the time worked on a work order task
description: Manage and record time worked on work order tasks and activities. Time recorded entries automatically generate time cards and time sheets for approval by managers. Agents record time for themselves, and managers can also record time for the technicians they manage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/Recording-time-spent-on-work-order-tasks.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Updating task status, Completing work orders on the web interface, Use, Field Service Management]
---

# Recording the time worked on a work order task

Manage and record time worked on work order tasks and activities. Time recorded entries automatically generate time cards and time sheets for approval by managers. Agents record time for themselves, and managers can also record time for the technicians they manage.

Time worked on a work order task can be recorded manually by a user or created automatically by the system.

## Record time manually

An agent can record time worked directly from a work order task by selecting Record Time on the Work Order Task form. See [Record time worked for a task or activity manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/field-service-agent-record-time.md).

Managers and dispatchers can also record time on behalf of a technician. See [Record time spent on a task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/manage-work-order-tasks-dw.md).

## Record time automatically

An administrator can enable the system to create time worked records as agents work on tasks by turning on these system properties:

-   **work.management.allow.auto.timecard**: Time worked records are created automatically. The Actual work duration field on the task captures the cumulative time worked on the task.
-   **work.management.allow.travel.task.timecard**: Enables recording the time an agent spends executing a work order task. The time card is generated when the agent selects Start work.

If both properties are enabled, time cards are created automatically. These time cards capture the duration of the agent's work on the task, including the task's travel time.

For more information about these properties, see [Properties installed with Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/r_PropInstallWFieldServMgmnt.md).

