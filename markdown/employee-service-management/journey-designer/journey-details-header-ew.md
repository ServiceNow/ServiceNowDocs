---
title: Journey Details page header inEmployeeWorks Web App Base
description: The Journey Details page header shows the journey or lifecycle event's status, progress, and participant information, and can be expanded or collapsed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/journey-designer/journey-details-header-ew.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [Journey Details header, progress bar, Employee Works]
breadcrumb: [Journeys in EmployeeWorks Web App, AI in Journey designer, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Journey Details page header inEmployeeWorks Web App Base

The Journey Details page header shows the journey or lifecycle event's status, progress, and participant information, and can be expanded or collapsed.

## Journey details page overview

The Journey Details page header displays the record name the configured journey title for a journey, or `HR Service Name - Subject Person` for a standalone lifecycle event case along with a status pill. You can expand or collapse the header.

## Progress bar

An overall progress bar appears in the header, using the same component and visual treatment for journeys and standalone lifecycle event cases. The completion percentage displays next to the progress bar \(for example, `73% complete`\), and the bar updates when journey or lifecycle event task progress changes. The progress bar is the same for both the employee and manager views.

## Employee view

For employees, the header shows a status derived from the employee's own assigned tasks:

-   **Overdue** – one or more active tasks assigned to the employee are overdue \(shown as, for example, `X tasks overdue`\).
-   **On Track** – no active tasks assigned to the employee are overdue, including when the employee has completed all currently available tasks and the journey is still in progress.
-   **Completed** – the journey status is Completed.

The header also shows the employee's remaining task count. A progress indicator is displayed for the employee's tasks, along with **Your Manager** \(or **Journey Owner**, when the journey owner isn't the employee's manager\) and, when a mentor is assigned, **Your Mentor**. Selecting a manager or mentor opens their HR profile.

## Manager view

For managers, the header shows both the manager's own task progress and the overall journey progress: a persona-based status and progress indicator for the manager's own assigned tasks, and the overall journey status and completion percentage. The header shows **Team Member** \(or **Journey For**, depending on whether the employee's manager is the journey owner\) and, when assigned, journey mentors. A mentor can also view the Journey Details page, with the same header fields as the manager view.

## Subject person and opened-for precedence

If a user is both the subject person and the opened-for user on a record, the employee/subject-person view takes precedence.

