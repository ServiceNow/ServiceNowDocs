---
title: Client side planning console
description: During calculation of project schedule in the planning console, it is possible to build your project structure quickly on the client side \(browser\) without having to save details in the server for each interaction. It prevents any time lags that occur after you perform any actions in the planning console, and improves the scheduling performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/client-side-planning-console.html
release: australia
product: Project Management
classification: project-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Planning console - Legacy, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Client side planning console

During calculation of project schedule in the planning console, it is possible to build your project structure quickly on the client side \(browser\) without having to save details in the server for each interaction. It prevents any time lags that occur after you perform any actions in the planning console, and improves the scheduling performance.

For example, when a project manager changes dates on a project task in the planning console, re-calculating the dates for the dependent tasks and the project can cause time lag if each interaction is saved to the server. Similarly, when a new task or a dependency is created, there can be a time lag before the new dates are displayed if they are saved on the server side each time.

When client side planning is [enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/enable-client-side-planning.md), the changes such as re-calculation of dates are not posted to the server immediately. All the changes in planning console are kept on client side until the user explicitly saves the changes to be committed to the server.

## Exceptions

There are a few actions for which you must save your changes immediately to the server side before proceeding such as:

-   Create baseline
-   Copy project
-   Copy partial project
-   Add child tasks
-   Add external dependency
-   Edit Assigned to
-   Edit Additional Assignees

In addition, if you enable custom business rules on any of the columns, those columns are also part of exceptions.

-   **[Enable client side planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/enable-client-side-planning.md)**  
Enable client side planning in planning console to enable project scheduling at the client side.

**Parent Topic:**[Using Planning console - Legacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_TheProjectPlanningConsole.md)

**Related topics**  


[Open the project planning console]()

[Planning console tasks]()

[Gantt chart]()

[Create a parent-child relationship on the planning console]()

[Predecessor dependencies in the planning console]()

[Custom columns in the planning console]()

[Create a dependency from the planning console]()

[Using Planning console - Legacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/c_TheProjectPlanningConsole.md)

