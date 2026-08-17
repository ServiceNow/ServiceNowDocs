---
title: Configure a custom AI insights skill for a task type
description: Configure a task to use a custom Now Assist skill for AI insights in the Task details widget. Optionally add a custom script to pre-process input or post-process the skill response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 4
keywords: [AI insights skill, Bring Your Own Skill, task configuration, ServiceNow Otto skill, Employee Works, custom script, Applies to, Employee Center]
breadcrumb: [Task configuration, Tasks and requests, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure a custom AI insights skill for a task type

Configure a task to use a custom Now Assist skill for AI insights in the Task details widget. Optionally add a custom script to pre-process input or post-process the skill response.

## Before you begin

Verify that the Generative AI plugin \(sn\_generative\_ai\) and the configured skill are active.

Select and activate a Now Assist skill that works best for the task type.

Role required: sn\_hr\_sp.esc\_admin or admin

## About this task

AI insights help employees understand task details and make informed decisions. Configure a skill for each task type that requires AI-generated insights in the **Task details** widget. Learn about task scope and action widget configuration from [Configure task scope and action widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-configure-action-widget.md)

You can configure custom skills to provide task-specific insights. Examples include:

-   Policy compliance checks for Concur approval tasks
-   Field-level insights for CLM contract tasks
-   Time-off balance details for leave requests

**Note:** The widget displays AI insights only when you configure a skill for the task type.

## Procedure

1.  Go to **All** &gt; **Employee Center** &gt; **Administration** &gt; **To-dos Configurations**, select an existing to-dos configuration \(for example, **sn\_hr\_sp\_todos\_config**\) for the task category, such as **Approvals**\), and navigate to the **Task Configuration** related list.

2.  In the **Task Configurations** related list, open the task configuration for the required record type, such as **Request**.

    Task configuration page and its related list open.

    \[Omitted image "es-tasks-config-ai-insight.png"\] Alt text: Task configuration with AI insights skill

3.  Go to the **AI insights** tab and select the **AI insights skill** field to a Now Assist skill from the available list.

    \[Omitted image "es-tasks-ai-skill-field.png"\] Alt text: Task Configuration record for Request Item with the AI insights skill field set

    You can select one of the two

    -   Existing AI Insight Skills: Select from the existing pre-configured AI Insight skills provided by ServiceNow.
    -   Custom AI Insight Skills: Enable custom skill processing by checking the custom skill option and providing your JSON format configuration.
    **Note:** By default, the AI insights skill field is empty. Administrators can select the available skills such as built-in Checklist Generation skill instead of building a custom one. For example, select the built-in **Approval summary checklist generation** skill to show the approval checklist behavior. The checklist appears only while the approval is still actionable.

4.  Select the **Use custom script** check box to customize how the skill processes data,

    Write a script in the **Skill execution script** field that performs the following actions:

    -   Pre-processes the input data
    -   Calls the AI insights skill
    -   Post-processes the skill output
    -   Returns a response that matches the skill output contract
    \[Omitted image "es-tasks-skill-config.png"\] Alt text: Custom script skill configuration for task AI insights

    Use a custom script to fetch external data before the skill runs. For example, fetch leave balances from Workday before a leave-approval task runs. You can also retrieve prior expense reports from Concur before an expense-approval task runs. Your script can use the following variables to build internal record or knowledge article URLs:

    -   **__hostname__**

        The virtual host of the instance, for example **now**.

    -   **__experience__**

        The current experience suffix, for example **employee** or **aiux-portal**.

    **Note:** To use ES12 syntax in your script, select **Turn on ECMAScript 2021 \(ES12\) mode** in the script editor toolbar. For the required response format, see [AI insights skill reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-ai-insights-skill-ref.md).

    The **Skill execution script** field opens.

5.  Confirm that the task configuration is **Active**.

6.  Save the task configuration.

    You can now see the associated skill from the **Task Configuration** tab. The configured skill or your custom script generates AI insights for every record of that task type in the experience set by **Applies to**.


## Result

Employees who open the task type see a summary and any reference links in the AI response card. The configured skill generates AI insights for every record of that task type.

The skill run fails if the selected skill does not accept **sys\_id** and **table** parameters or if its output does not match the expected format. When a skill run fails, you see an error message instead of insights. To remove the AI insights section for that task type, clear the **AI insights skill** field and reload the page.

The skill execution script fails if it does not return a response that matches the skill output contract. When the script fails, you see a generic error message instead of insights.

Understand the basics of AI insights skill, see [AI insights skill reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-ai-insights-skill-ref.md).

**Related topics**  


[AI insights skill reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-ai-insights-skill-ref.md)

[Configure task scope and action widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-configure-action-widget.md)

