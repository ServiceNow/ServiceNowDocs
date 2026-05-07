---
title: Employee Org chart
description: The organizational chart provides an interactive visualization of company structure, reporting relationships, and team hierarchies with search and navigation capabilities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-01-27"
reading_time_minutes: 2
breadcrumb: [Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Employee Org chart

The organizational chart provides an interactive visualization of company structure, reporting relationships, and team hierarchies with search and navigation capabilities.

Employee Slate brings org chart and employee profile functionality together in a single experience. Employees explore the organizational structure and view colleague information without switching between HR systems or directory tools.

![Employee org chart and team structure](../images/es-org-chart.png "Org chart")

## Org chart

The org chart surfaces reporting structures and team hierarchies with rich contextual information available upfront. Employees navigate the org chart to understand how the organization is structured and to identify colleagues in specific roles or teams.

With Now Assist Chat, the org chart adds the following AI-driven interactions:

-   Chat-driven profile discovery: Employees ask about any colleague using natural language, and the assistant returns an interactive profile card with key details.
-   Split view exploration: The org chart opens alongside the conversation panel in the interactive split view. Employees explore the hierarchy while asking questions about specific people or teams.

## Admin configuration

Administrators configure org chart and profile content through two records in the Employee Center application:

-   Use the organization chart configuration to define eligible users and to select the fields that appear on org chart cards.
-   Use the overview UI configuration to select the fields that appear in the **About**, **Work details**, **Personal details**, and **Team** sections.

Employee Slate uses the same org chart configuration as Employee Center. You don't need to set up the org chart separately when you deploy Employee Slate alongside an existing Employee Center instance.

**Note:** The scheduled job fetches the count of direct reports. During an org restructure, the badge count and the actual number may not match. To resolve the count issue, run the org chart schedule job.

## What you can do with org chart

The org chart provides the following capabilities:

-   Multi-level navigation: Displays the employee hierarchy one level at a time with a **Show more** option to expand additional levels.
-   Search functionality: Finds specific employees by name using the search field on the org chart page.
-   Profile information: Selecting an employee card opens the corresponding profile page.
-   Contextual positioning: Navigate to any employee position in the org chart from their profile page using the **View Org Chart** button.
-   Team structure indicators: Visual representation of reporting structures.

## AI chat interactions

With Now Assist Chat, employees find and open profiles conversationally:

-   Ask about a colleague by name to open a people-finder response that links to the profile.
-   Ask to see the organization for a colleague to open the org chart centered on that person.
-   Use the context. When an employee is visible on the current page, asking about that employee updates the same view.

The chart updates automatically to reflect organizational changes, new hires, role changes, and departures. Visual indicators show direct reports and temporary assignments.

