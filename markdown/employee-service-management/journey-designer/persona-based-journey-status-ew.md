---
title: Persona-based journey status and progress in Employee Works
description: In Employee Works, a journey's status and progress are calculated separately for each participant, based only on the tasks assigned to that participant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/journey-designer/persona-based-journey-status-ew.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [journey status, journey progress, persona-based, Employee Works]
breadcrumb: [Journeys in EmployeeWorks Web App, AI in Journey designer, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Persona-based journey status and progress in Employee Works

In Employee Works, a journey's status and progress are calculated separately for each participant, based only on the tasks assigned to that participant.

## Journey status

Status is derived dynamically from the signed-in user's own assigned tasks:

-   **Overdue** – one or more active tasks assigned to the signed-in user are overdue.
-   **On Track** – none of the active tasks assigned to the signed-in user are overdue.

Because status is calculated per participant, the same journey can show a different status to different people depending on their own assigned tasks. Status updates whenever a task assignment or task state changes.

## Journey progress

Progress metrics are also derived from the signed-in user's own assigned tasks:

-   **Remaining task count** – the number of active, incomplete tasks assigned to the signed-in user.
-   **Journey completion percentage** – the percentage of the signed-in user's assigned tasks that are complete.

Tasks assigned to other journey participants are excluded from these calculations, so the same journey can show different remaining task counts and completion percentages to different participants. Progress metrics update whenever a task assignment or completion status changes.

## Where persona-based status and progress appear

Persona-based status and progress are supported on the Journey Home Page widget and the Journey List page, for both the employee's My Journeys view and the manager's Team Journeys view.

