---
title: Personalized canvas
description: Build a personal canvas that brings together AI-generated widgets, role-specific content, and curated tools in a single layout. Administrators govern the canvas through configurations and a widget library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-personalized-canvas.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-04-24"
reading_time_minutes: 2
keywords: [personalized canvas, widgets, widget library, layout]
breadcrumb: [Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Personalized canvas

Build a personal canvas that brings together AI-generated widgets, role-specific content, and curated tools in a single layout. Administrators govern the canvas through configurations and a widget library.

Each employee has a personal canvas. Employees configure the canvas within the bounds of the widget library and the canvas defaults that the administrator sets. Administrators shape the default experience and control what employees access. Employees personalize their own canvas within those limits.

\[Omitted image "es-canvas.png"\] Alt text: Canvas module showing Inbox widget with to-do items, Featured apps section, Kudos and recognition widget, and Smart mood check-in widget

## Canvas types

Employee Slate supports personal and role-based canvases that adapt to individual employee needs and organizational roles.

-   **Role-based canvas**

    Canvas populates based on the organizational role of the employee. Employees with a specific role configure the role canvas to reflect the tools and data most relevant to that role. AI agents can also populate role-based canvases with widgets, data, and actions for role-specific workflows.

-   **Personal canvas**

    Employees customize their personal canvas by adding widgets from the library, resizing and repositioning them, and pinning widgets that the AI assistant generates during conversations.


## Canvas configurations

Administrators manage the canvas experience through three configuration layers:

-   **Curated default**

    The default canvas layout that employees see when they first access their canvas. The curated default includes the widgets that the administrator determines are most relevant for the employee population.

-   **Widget library**

    The set of approved widgets that employees add to their canvas.

-   **Employee personalization**

    Within the bounds of the widget library, you personalize your canvas. You drag widgets into place, resize them, and pin them from chat.


## Administrator controls

Administrators have controls over the canvas environment at the organizational level:

-   Define mandatory widgets that appear on all employee canvases and that employees can't remove. Use mandatory widgets for compliance requirements, critical announcements, or high-priority organizational initiatives.
-   Define priority widgets that Employee Slate prepopulates on employee canvases but that employees can remove or reposition. Use priority widgets for targeted campaigns or role-specific tooling.

## Widget ecosystem

Employee Slate includes a library of predefined widgets that address common employee productivity use cases. These widgets are available for employees to add to their personal canvas and for administrators to configure as mandatory or priority widgets. Administrators extend the library with custom widgets built through the [AI-powered Widget Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-ai-widget-builder.md).

