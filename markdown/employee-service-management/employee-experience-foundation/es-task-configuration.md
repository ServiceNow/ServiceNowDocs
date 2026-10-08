---
title: Task configuration enhancements
description: Task configurations control how tasks appear and behave in Employee Center and EmployeeWorks Web App, including widget mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/employee-experience-foundation/es-task-configuration.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-08-03"
reading_time_minutes: 3
keywords: [task configuration, Employee Center, Employee Slate, Applies to, action group, AIX widget, AI insights skill, custom script]
breadcrumb: [Tasks and requests, Working with EmployeeWorks capabilities, ServiceNow EmployeeWorks Web App, Unified Employee Experience, Employee Service Management]
---

# Task configuration enhancements

Task configurations control how tasks appear and behave in Employee Center and EmployeeWorks Web App, including widget mappings.

Task configurations define how to-do items display and function across employee experiences. You can configure task-specific widgets for different task types without breaking existing widget mappings.

## HR task types in Employee Slate

The task types are re-platformed for improved AI integration on the Employee Slate platform.

Plugin requirements: To use these task types, you must have:

-   EmployeeWorks Web App licensing \(obtained either by EmployeeWorks Web App for Now Assist or EmployeeWorks Web App for Moveworks\)
-   Case and Knowledge Management for EmployeeWorks plugin

Supported task types:

-   **Approval:** An approval task where HR agents or managers review and approve or reject a request with comments. The approval decision is written back to the workflow and advances the case.
-   **Checklist:** A multi-item task where employees track and mark off individual items. The task only closes when all required items are checked, and the case advances upon closure.
-   **E-signature:** The E-signature enables secure document signing within HR task workflows. When employees encounter an E-signature task, they can capture their digital signature on screen. The signed PDF is archived to the employee record with a full audit trail.
-   **Schedule a meeting:** A task that allows employees to schedule meetings with HR agents or managers. The task integrates with calendar systems to coordinate availability and send meeting invitations.
-   **Mark When Complete:** A simple one-click task for employees to acknowledge completion. The task closes when the employee selects the **Mark as Complete** button, and the HR case advances to the next step.
-   **Upload documents:** A task that enables employees to attach required documents to their HR case. Uploaded files are stored with the case record and can be reviewed by HR agents.
-   **URL:** A task that directs employees to an external web page or resource. The task can open the URL in a new tab or embedded frame, and employees mark the task complete after reviewing the content.
-   **View video:** A task that presents video content to employees within the workflow. The task tracks video completion and advances the case when the employee finishes viewing the required content.

## Configure task scope and actions

You can customize task configurations in two ways:

-   **Scope configurations by experience**: Use the **Applies to** field to control which experience uses a task configuration. You can scope configurations to Employee Center, EmployeeWorks Web App, or both. When set to **All**, you configure both Angular and AIX widgets for each platform. When scoped to a single platform, only the relevant widget fields appear.

    **Note:** The default task configurations are supported for only EmployeeWorks or EmployeeSlate.

-   **Build custom action widgets**: Use the **Action** tab to configure custom LIT-based action widgets for task types. Custom action widget provides an alternative to the default action group. The **AIX action widget** field accepts LIT-based widgets that embed custom Angular widgets for task-specific actions.

For more information, see [Configure task scope and action widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/employee-experience-foundation/empworks-configure-action-widget.md).

## E-signature configuration

The E-signature enables secure document signing within HR task workflows. When employees encounter an E-signature task, they can capture their digital signature on screen, and the signed PDF is archived to the employee record with a full audit trail.

**Plugin requirements:**

-   E-signature plugin installed and active
-   Case and Knowledge Management for EmployeeWorks plugin
-   EmployeeWorks Web App licensing \(obtained either by EmployeeWorks Web App for Now Assist or EmployeeWorks Web App for Moveworks\)

**Related topics**  


[Enable task configuration for approvals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/employee-experience-foundation/approval-hub-to-dos-page-filters.md)

