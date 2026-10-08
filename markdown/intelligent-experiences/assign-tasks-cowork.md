---
title: Assign tasks to ServiceNow Cowork
description: Use ServiceNow Cowork to complete multi-step work, such as investigating incidents, creating reports, or coordinating updates across platforms. Combine skills, sub-agents, and connectors in a single request so Cowork can complete the whole piece of work from start to finish.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/assign-tasks-cowork.html
release: australia
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 2
keywords: [complex tasks, multistep tasks, skills, subagents]
breadcrumb: [Use, ServiceNow Cowork, Enable AI experiences]
---

# Assign tasks to ServiceNow Cowork

Use ServiceNow Cowork to complete multi-step work, such as investigating incidents, creating reports, or coordinating updates across platforms. Combine skills, sub-agents, and connectors in a single request so Cowork can complete the whole piece of work from start to finish.

## Before you begin

Role required: sn\_app\_cowork.user

The platforms the task uses, such as ServiceNow instance, Microsoft 365, or GitHub, must be connected. For more information, see [Connectors in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/connectors-in-cowork.md).

## Procedure

1.  In the message box, describe the outcome you want, including the goal, the sources to use, and the format of the result.

    For example: Find my open P1 incidents, check each one for related changes in the last week, summarize the likely cause, and draft an update email to each assignment group.

    Cowork determines the steps automatically, so describe the result, not the steps.

2.  Enter a slash followed by the skill name, such as /plan-my-time, to run a skill as part of the task.

    Cowork also uses skills automatically when your request matches a skill's description.

3.  Name a sub-agent in your request to hand part of the work to a specialist.

    For example: Use the researcher sub-agent to find the API documentation, and then use the build-fixer sub-agent to fix the failing test. Cowork automatically routes work to sub-agents when a task requires focused expertise.

4.  Include when the task should run, such as every Monday at 9 a.m., to run it on a schedule.

5.  Select a model from the model list in the message box to use a different model for this task.

6.  Select the send icon.

7.  Select **Kanban** in the sidebar to follow the task.

8.  If Cowork asks for approval or input, respond in the chat so the task can continue.

    **Example request**: Every Monday, summarize last week's P1 incidents, create a PowerPoint presentation with a slide per incident, and post the summary to my team's Teams channel.

    Cowork processes this request in stages:

    1.  Queries ServiceNow for P1 incidents through the ServiceNow connector.
    2.  Assigns the analysis to the sn-analyst sub-agent.
    3.  Uses the pptx skill to create the presentation.
    4.  Asks for your approval before it posts to Teams through the Microsoft 365 connector.
    5.  Saves the request as a scheduled task that runs every Monday.

## Result

Cowork executes each step of the task, using the required skills, sub-agents, and connectors. When the task is done, it moves to **Completed** on the **Kanban** board, and the results appear in the chat.

## What to do next

For better results with complex tasks:

-   Name specific sources, such as a ServiceNow table, a Microsoft SharePoint folder, or a GitHub repository.
-   State the output format, such as an email draft, a spreadsheet, or a slide per item.
-   For work you repeat, turn it into a custom skill.

**Parent Topic:**[Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/servicenow-cowork-using.md)

