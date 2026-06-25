---
title: Configure tasks and requests
description: Set up AI preferences to control resource usage and generation modes for task insights and request summaries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/emp-slate-tasks-requests.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-06-04"
reading_time_minutes: 2
keywords: [configure AI preferences, usage limits, insights, summaries]
breadcrumb: [Employee Slate for Now Assist, Configuration flow, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Configure tasks and requests

Set up AI preferences to control resource usage and generation modes for task insights and request summaries.

## Before you begin

Check your entitlements to determine whether you have access to Now Assist or Moveworks licensing.

Role required: admin

## About this task

Configure the following AI preferences to manage smart prioritization for tasks and requests.

-   **AI assist** represents a single background execution of an AI feature that automatically generates insights, card summaries, or smart task sorting across your organization.
-   **Task insight** analyzes the tasks against policy criteria to identify compliance and optimization opportunities.
-   **Request summary** generates a concise summary of request details with useful info and efficiency.

## Procedure

1.  Follow the instructions here to [Configure branding and theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/eslate-config-admin-console.md).

2.  Expand the **Tasks and requests** section and select **Tasks** to view the read-only list with task types, table, conditions, search, and configure tasks.

    \[Omitted image "es-tasks-admin.png"\] Alt text: Tasks list and details

    **Note:** For additional information, select **Configure tasks** to go to tasks full-list or go to a specific task configuration by clicking external link icon. For more information, see [Employee tasks page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/employee-center-to-dos-page-configuration.md).

3.  Expand the **Tasks and requests** section and select **Requests** to view the read-only list with request types, table, conditions, search, and configure requests.

    \[Omitted image "es-requests-admin.png"\] Alt text: Request details

    **Note:** For additional information, select **Configure request** to go to requests full-list or go to a specific request configuration by clicking external link icon. For more information, see [Employee requests page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/employee-center-requests-page-configuration.md).

4.  Expand the **Tasks and requests** section and select **AI preferences** to manage usage limits and insight and summaries.

    \[Omitted image "es-ai-preferences-admin.png"\] Alt text: AI preferences for usage limit, insights, and summaries

    **Note:** When you don't have appropriate licensing, AI preferences aren't visible in the navigation.

    1.  Configure **Usage limit per day** for AI assists by selecting a value between 0 and 100,000.

        -   Use default limit of 3000 assists per day.
        -   Adjust the range from 0 to 100,000 assists per day to suit your needs.
        -   Set the value to 0 to disable the smart prioritization and revert to the due date-based sorting.
    2.  Configure the **Insights and summaries** modes for approval insights and request summaries.

        -   For task insights, select **Auto-generate** to create insights automatically when task detail page loads or select **On-demand** to manually trigger from the **Summarize** button.
        -   For request summaries, select **Auto-generate** to create summaries automatically when request detail page loads or select **On-demand** to manually trigger from the **Summarize** button
    3.  Save the AI preferences configuration.

        Your preferences are to task and request processing.

5.  Select **Mark as configured** for each completed configuration section in the Admin Console.


## What to do next

Monitor AI assists usage and adjust limits as needed based on organizational requirements and performance considerations.

**Related topics**  


[Smart prioritization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/ec-smart-prioritization-content.md)

