---
title: Configure a custom AI insights skill for a task type
description: Configure a task to use a custom Now Assist skill for AI insights in the Ticket Details widget. The custom skill lets you tailor insights that are relevant to the task types or business requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-04"
reading_time_minutes: 2
keywords: [AI insights skill, Bring Your Own Skill, task configuration, Now Assist skill, Employee Works]
breadcrumb: [Tasks and requests, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure a custom AI insights skill for a task type

Configure a task to use a custom Now Assist skill for AI insights in the Ticket Details widget. The custom skill lets you tailor insights that are relevant to the task types or business requirements.

## Before you begin

Verify that the Generative AI plugin \(sn\_generative\_ai\) and the configured skill are active.

Select and activate a Now Assist skill that works best for the task type.

Role required: sn\_hr\_sp.esc\_admin or admin

## About this task

Configure a skill only for task types that need AI-generated insights. You can configure a custom skill to tailor AI insights on the **Tasks** page. For example, you can configure the following custom skills.

-   A skill that checks policies for Concur approval tasks
-   A skill that shows CLM field-level insights for contract tasks
-   A skill that shows the time-off balance details

**Note:** By default, the **Ticket details** widget does not display AI insights when you don't configure a custom skill for the task type.

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, select an existing to-dos configuration \(for example, **sn\_hr\_sp\_todos\_config**\) for the task category, such as **Approvals**\), and navigate to the **Task Configuration** related list.

2.  In the **Task Configurations** related list, open the task configuration for the required record type, such as **Request**.

    Task configuration page opens.

    **Note:** By default, the AI insights skill field is empty.

    \[Omitted image "es-tasks-config-ai-insight.png"\] Alt text: Task configuration with AI insights skill

3.  Set the **AI insights skill** field to a Now Assist skill from the available list.

    \[Omitted image "es-tasks-ai-skill-field.png"\] Alt text: Task Configuration record for Request Item with the AI insights skill field set

    **Note:** Administrators can select the available skills such as built-in Checklist Generation skill instead of building a custom one. For example, select the built-in **Approval summary checklist generation** skill to show the approval checklist behavior. The checklist appears only while the approval is still actionable.

4.  Confirm that the task configuration is **Active**.

5.  Save the task configuration.

    You can now see the associated skill from the **Task Configuration** tab. The configured skill generates AI insights for every record of that task type.

    \[Omitted image "es-tasks-skill-config.png"\] Alt text: Skill configuration for task AI insights


## Result

Employees who open the task type see a summary and any reference links in the AI response card. The configured skill generates AI insights for every record of that task type.

The skill run fails if the selected skill does not accept **sys\_id** and **table** parameters or if its output does not match the expected format. When a skill run fails, you see an error message instead of insights. To remove the AI insights section for that task type, clear the **AI insights skill** field and reload the page.

Understand the basics of AI insights skill, see [AI insights skill reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-ai-insights-skill-ref.md).

**Related topics**  


[AI insights skill reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-ai-insights-skill-ref.md)

