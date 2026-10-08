---
title: Find and filter journeys on the Journey List page
description: Search, filter, and page through your journeys and lifecycle event cases, and your team's journeys if you're a manager, on the Journey List page in Employee Works.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/journey-designer/use-journey-list-page-ew.html
release: australia
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2026-09-18"
reading_time_minutes: 1
keywords: [Journey List page, journey filter, journey search, Employee Works]
breadcrumb: [Journeys in EmployeeWorks Web App, AI in Journey designer, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Find and filter journeys on the Journey List page

Search, filter, and page through your journeys and lifecycle event cases, and your team's journeys if you're a manager, on the Journey List page in Employee Works.

## Before you begin

Role required: sn\_jny.manager

## About this task

The Journey List page shows active journeys and standalone lifecycle event cases where you're the journey employee/subject person. For managers, it shows journeys you own or journeys opened by you.

## Procedure

1.  Navigate to EmployeeWorks Web App Base and open the Journey List page.

    Each journey card shows the journey or lifecycle event type, journey title, your persona-based status, your progress indicator, and your remaining active task count.

<table id="table_sfq_tnv_qkc"><thead><tr><th>

Find journey using

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Search

</td><td>

Enter a keyword in the search bar to find a specific journey or lifecycle event.Search for matches against the journey title or lifecycle event case title, the employee or subject person name, and the journey number or lifecycle event case number. Matching supports partial, case-insensitive keywords. Optionally clear the search keyword to return to the full journey list, with any applied filters still in effect.

</td></tr><tr><td>

Type

</td><td>

Select the **Journey Type** filter option and choose one or more journey typees from the drop-down.The filter shows a unified list of journey types and lifecycle event types across active records, with a count beside each. Applied filters display as chips below the filter bar; remove one by selecting the **x** on its chip or by deselecting it in the drop-down.

</td></tr><tr><td>

State

</td><td>

To filter by state, select the **State** multi-select dropdown and select one or more states.For employees, the available states are Overdue, On Track, and Completed. For managers, team journeys are available in Draft state. Applied state filters are displayed below the filter bar, the same as Journey Type filters, and can be removed the same way. When a selected state has no matching records, an empty state displays.

</td></tr><tr><td>

Pagination controls

</td><td>

Use the pagination controls to move between pages of results.By default, results are sorted by journey published date \(earliest first\). When Attention First sorting is enabled, journeys are instead ordered by the due date of the next active task for your own journeys, the next task assigned to you.

For team journeys, the next task assigned to any participant with overdue tasks shown first \(longest overdue first\), then tasks due today, then future tasks by nearest due date.

</td></tr></tbody>
</table>
