---
title: Configure the home page
description: Configure the home page in EmployeeWorks Web App. Set the AI chat entry, the out-of-the-box widget lineup, and the quick links shown to employees.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-configure-home-page.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [home page, homepage configuration, AI chat, announcements widget, quick links, upcoming holiday, Employee Slate]
breadcrumb: [EmployeeWorks home, ServiceNow EmployeeWorks Web App, Unified Employee Experience, Employee Service Management]
---

# Configure the home page

Configure the home page in EmployeeWorks Web App. Set the AI chat entry, the out-of-the-box widget lineup, and the quick links shown to employees.

## Before you begin

Activate Employee Slate \(built for Now Assist\) in the instance.

Role required: admin.

## About this task

The home page is the personalized starting point for an employee. The page aggregates the relevant tasks, requests, and content for the day.

Configure each widget to scope the content for the audience.

## Procedure

1.  Navigate to **Admin Console** &gt; **All** &gt; **Home page**.

    The home page configuration lists the AI chat entry and the out-of-the-box widget lineup.

2.  Set the AI chat and search entry at the top of the page.

    Employees use the chat entry to find a knowledge article, request a catalog item, or ask a quick question without navigating away.

    \[Omitted image "es-home-widget-config.png"\] Alt text: Home widget configuration in the Product Configuration console

3.  [Configure the home page background](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-configure-home-page-background.md).

    Set a solid color, gradient, or image background, and match the logo and text color to the background.

4.  [Configure tasks and requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/emp-slate-tasks-requests.md) widget.

    Set the task types and the source queues that appear in the widget. Employees can take action on a task from the widget or open the detailed Tasks and requests view.

5.  [Create announcements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown).

    Select the announcement source and the carousel order. Employees can select a slide to open the announcement details.

6.  [Configure the Upcoming Holiday widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-configure-upcoming-holiday.md).

    Set the holiday source by work location. Employees view the next holiday based on the location set on the user record.

7.  [Configure quick links from the admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-manage-quick-links-console.md).

    Add knowledge articles, catalog items, or external links. Employees select a link to navigate directly to the destination.

8.  [Configure notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-configure-notifications.md)

9.  Configure the **Popular Content** widget.

    Set the source for knowledge articles and catalog items. The widget shows the most viewed knowledge and the most requested catalog item for the chosen scope.

10. Verify the home page from an employee account such as Abel Tuter.

    Sign in to Employee Slate and confirm that the chat entry, the widgets, and the quick links render as configured.

11. Save the configuration.

    The save commits the AI chat entry and the widget settings. Refresh the home page to confirm the change.


## Result

Employees view the configured chat entry at the top of the page and the five default widgets below. The page presents proactive nudges for tasks and surfaces popular content, the next holiday, and the quick links you configured.

