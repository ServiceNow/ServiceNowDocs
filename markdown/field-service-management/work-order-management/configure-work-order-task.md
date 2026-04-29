---
title: Configuring work order tasks
description: Work orders are composed of at least one, but usually multiple, work order tasks. The tasks in a work order can be assigned to one person, a group, or multiple Field Service technicians who operate autonomously. It’s easier to complete a work order when the tasks needed to finish the work are divided into logical parts that can be accomplished independently.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring work order tasks

Work orders are composed of at least one, but usually multiple, work order tasks. The tasks in a work order can be assigned to one person, a group, or multiple Field Service technicians who operate autonomously. It’s easier to complete a work order when the tasks needed to finish the work are divided into logical parts that can be accomplished independently.

## Configuration overview

Optionally, set up one or more work order task configurations.

-   [Create work types for a work order task](../task/create-work-type-fsm.md)

    Create different work types for a task to determine and configure the various requirements of the task, such as if the task needs a crew and preference of an assignment group.

-   [Work order task states](work-order-task-states.md)

    Work order tasks states are sequential and progress from one state to the next. Depending on your configuration, work order tasks may follow this sequence, a unique sequence, or automatically move from state to state when defined requirements are met.

-   [Configure the Scheduled state](../task/configure-scheduled-state.md)

    Allows for the work order task to be soft booked but not confirmed. In this state, the work order task is pending assignment from the dispatcher.

-   [Configuring survey-based work order questionnaires](work-order-questionnaire.md)

    Use the work order questionnaire feature enables admins to create questionnaire records and associate those records with work order tasks. The administrator can also make filling out the questionnaire required before an agent closes a task.

-   [Configuring Time Recording for Field Service](Configuring-time-recording.md)

    Use the time recording feature enables agents to record time worked on tasks from the Work Order Task form and time spent on other activities, such as meetings or training, from the Time Worked form.

-   [Enable PDF summaries at work order task level](../task/enable-pdf-summary.md)

    Signed PDF summaries are generated at the work order task level. You can generate these PDF summaries at the work order task level by enabling the SM Config.


