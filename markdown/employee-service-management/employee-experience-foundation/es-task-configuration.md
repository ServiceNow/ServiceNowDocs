---
title: Task configuration enhancements
description: Task configurations control how tasks appear and behave in Employee Center and Employee Slate, including widget mappings, action groups, and AI insights.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/es-task-configuration.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 2
keywords: [task configuration, Employee Center, Employee Slate, Applies to, action group, AIX widget, AI insights skill, custom script]
breadcrumb: [Tasks and requests, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Task configuration enhancements

Task configurations control how tasks appear and behave in Employee Center and Employee Slate, including widget mappings, action groups, and AI insights.

Task configurations define how to-do items display and function across employee experiences. You can configure task-specific widgets, action groups, and AI insights for different task types without breaking existing widget mappings.

## Configure task scope and actions

You can customize task configurations in two ways:

-   **Scope configurations by experience**: Use the **Applies to** field to control which experience uses a task configuration. You can scope configurations to Employee Center, Employee Slate, or both. When set to **All**, you configure both Angular and AIX widgets for each platform. When scoped to a single platform, only the relevant widget fields appear.
-   **Build custom action widgets**: Use the **Action** tab to configure custom LIT-based action widgets for task types. Custom action widget provides an alternative to the out-of-the-box action group. The **AIX action widget** field accepts LIT-based widgets that embed custom Angular widgets for task-specific actions.

For more information, see [Configure task scope and action widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-configure-action-widget.md).

## Configure custom AI insight skills

Use custom Now Assist skills to provide task-specific AI insights in the Ticket Details widget. You can configure skills in two ways:

-   **Select a preconfigured skill**: Configure different skills for each task type to deliver contextual insights such as policy compliance checks, field-level analysis, or balance summaries.
-   **Use custom scripts**: Add custom scripts to preprocess data before skill invocation. You can fetch additional context, enrich records, and format output before AI insights generate. Custom scripts enable integration with external systems such as Workday or Concur to retrieve relevant data for approval tasks.

For more information, see [Configure a custom AI insights skill for a task type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/empworks-configure-ai-insights-skill.md).

**Related topics**  


[Enable task configuration for approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/approval-hub-to-dos-page-filters.md)

