---
title: AI insights skill reference
description: Build a custom Now Assist skill that generates AI insights for the task details widget. Use this reference for the input, output, and error contract your skill must follow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/empworks-ai-insights-skill-ref.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-01-27"
reading_time_minutes: 3
keywords: [AI insights skill, Bring Your Own Skill, skill contract, task configuration, ServiceNow Otto skill, task details widget, Employee Works]
breadcrumb: [Configure a custom AI insights skill, Task configuration, Tasks and requests, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# AI insights skill reference

Build a custom Now Assist skill that generates AI insights for the task details widget. Use this reference for the input, output, and error contract your skill must follow.

## AI insights skill overview

Build your skill to match the input and output format in this topic. Administrators select your skill in the **AI insights skill** field \(`aix_ai_insights_skill`\) on the **AI insights** tab of the `sn_ex_sp_task_configuration` table.

To set a skill for a task type, see [Configure a custom AI insights skill for a task type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.md).

-   When a task page loads, the task details widget runs your skill through `ActivityHubUtilSNC.generateAiInsights`. The widget then displays the results in the AI response card.
-   When a skill is not selected, the AI insights section doesn't appear.
-   Administrators can select the available skills such as the out-of-the-box Checklist Generation skill instead of building a custom one. For example, when you select the **Approval summary checklist generation** skill to show the approval checklist behavior, the checklist appears only while the approval \(sysapproval\_approver\) is still actionable.

    **Note:** Approval checklist generation skill does not support other types of approvals.


## Example use cases

Build a skill that helps you get the contextual insights and details relevant to the task type:

-   A policy-check skill for Concur approval tasks.
-   A skill that surfaces CLM field-level insights for contract tasks.
-   A skill that shows the time-off balance details.

## Skill input specification

Your skill receives the following payload.

|Field|Type|Description|
|-----|----|-----------|
|`sys_id`|String|The sys\_id of the record on the task page.|
|`table`|String|The table name of the record on the task page.|

## Custom skill requirements

When you build custom skills, follow these guidelines

-   **Task context**

    Design your skill for the specific task type and the data available on that task.

-   **Performance**

    Make your skill execute efficiently so it does not slow the task page.

-   **Error handling**

    Handle failures using the format in error handling for your skill.


## Skill output specification

Return the following JSON structure from your skill, as a string or object:

|Field|Type|Required|Description|
|-----|----|--------|-----------|
|`summary`|String|Yes|The insight text shown in the AI response card. Supports HTML formatting.|
|`references`|Array|No|List of reference links. Each entry includes `number`, `title`, and `url` fields.|

Structure each object in your `references` array as explained in the following table:

|Field|Type|Required|Description|
|-----|----|--------|-----------|
|`number`\(Optional\)|String|Yes|Reference identifier displayed in the card.|
|`title`|String|Yes|Link text displayed to users.|
|`url`|String|Yes|Target URL for the reference link.|

## Error handling

If your skill fails, return the following error structure:

/b

|Field|Type|Required|Description|
|-----|----|--------|-----------|
|`status`|String|Yes|Must be set to `error`.|
|`message`|String|Yes|Error message displayed to users in the AI response card.|

**Note:** If your skill returns an empty or unreadable response, the AI response card shows a generic error message instead.

## Configuration options

Administrators control when your skill runs using this property:

|Property|Value|Behavior|
|--------|-----|--------|
|`sn_ex_ai_portal.task_insights_gen_mode`|`auto`|Insights are generated automatically when the task page loads.|
|`sn_ex_ai_portal.task_insights_gen_mode`|`on_demand`|Insights are generated when you select **Summarize this task** to generate insights.|

**Related topics**  


[Configure a custom AI insights skill for a task type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.md)

