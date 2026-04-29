---
title: Configuring survey-based work order questionnaires
description: Admin can create survey-based questionnaires and associate them with work order tasks.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Questionnaires, Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring survey-based work order questionnaires

Admin can create survey-based questionnaires and associate them with work order tasks.

The Survey Designer tool is used to create the questionnaires.

When a work order or task has an associated questionnaire, the **Questionnaires** button appears at the top of the form. Selecting this button displays the Questionnaires page, where the agent can complete the questionnaire or check-list.

**Note:** The Survey Designer tool for Field Service Management doesn't support the functionality of retaking a questionnaire.

## Demo questionnaire

The Inspection Questionnaire is a demo questionnaire record that is included with the Field Service - Questionnaire plugin. Whenever a work order task changes to the Work in Progress state, this questionnaire record adds a questionnaire to that task.

The following is a screen shot of the demo questionnaire form. In the Trigger condition section, there’s a condition that the state must have changed to Work in Progress.

When defining trigger conditions, the operator **changes to** means that the state was changed to Work in progress. If you instead use the operation **is**, then the questionnaire is triggered every time that an update is made to the task.

This demo questionnaire works as follows:

1.  The dispatcher assigns a work order task to an agent.
2.  The agent accepts the task and selects **Start Work** on the task form.
3.  The task state changes to Work in Progress.
4.  The **Questionnaires** button appears in the task form header.
5.  The agent selects **Questionnaires** to display one or more available questionnaires for the task.
6.  The agent selects **Start** on the desired questionnaire.
7.  The agent completes the questionnaire and selects **Submit** or **Save**.
8.  The agent returns to the work order task, completes the work, and closes the task.

**Note:** Questionnaires aren’t editable after the associated work order or task is closed.

## Configuration overview

The steps for setting up work order questionnaires are:

1.  [Activate Field Service Questionnaire](../task/Activate-fsm-questionnaire.md)

    Install the Field Service- Questionnaire plugin \(com.snc.wm\_questionnaire\) if you have the admin role.

2.  [Create a questionnaire for a work order or task](../task/create-questionnaire-for-work-order.md)

    Create a questionnaire to be completed before work starts or after a work is done.


**Related topics**  


[Activate Field Service Questionnaire](../task/Activate-fsm-questionnaire.md)

[Create a questionnaire for a work order or task](../task/create-questionnaire-for-work-order.md)

