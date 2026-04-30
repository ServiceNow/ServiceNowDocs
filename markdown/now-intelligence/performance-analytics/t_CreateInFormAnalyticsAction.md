---
title: Add in-form analytics to a form
description: Create a UI action that enables users to view relevant analytics while completing a form. The UI action associates the table that uses the form, a breakdown used with that table, and a breakdown dashboard.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [In-form analytics, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add in-form analytics to a form

Create a UI action that enables users to view relevant analytics while completing a form. The UI action associates the table that uses the form, a breakdown used with that table, and a breakdown dashboard.

## Before you begin

Role required: pa\_power\_user, pa\_admin, or admin. In addition to the Performance Analytics roles, you must be able to create records on the UI Actions \[sys\_ui\_action\] table.

Before adding in-form analytics for a specific table and breakdown, create a breakdown dashboard that uses that table and the breakdown source of that breakdown. Design the dashboard so that it prominently displays the most useful information to the users who create records on that table. For more information about breakdown dashboards, see [Using breakdowns on dashboards](../concept/c_SpecialDashboards.md).

Performance Analytics must be active to create in-form analytics.

## About this task

## Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **In-Form Analytics** and create a new record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Name|A descriptive name for the UI action.|
    |Table|The table to display analytics for. The in-page icon appears on forms for this table.|
    |Breakdown|The breakdown for analyzing the table. The UI action icon appears next to the field that corresponds to this breakdown, if the field is included in the form view.|
    |Dashboard|The breakdown dashboard to display. The dashboard must use the selected **Table** and the breakdown source of the **Breakdown**.|
    |Icon|The icon to display next to the breakdown-related field on the form.|
    |Icon color|The color of the form icon.|
    |Create in-form link|Display a related link on the form in addition to the icon when this check box is selected. The related link directs to the same dashboard as the icon.|


## Incident Assignment Group in-form analytics

Consider the case where you want support engineers who create incidents to be able to see the expected time to close the incident based on the assignment group. You have designed a widget that shows the expected time to close an incident. You have added this widget to the In-form Analytics breakdown dashboard, which uses the Groups breakdown source. 'Groups' is the source for the Assignment Group breakdown.

![Breakdown dashboard with the Groups breakdown source and a widget showing the expected time to close an incident](../image/in-form-analytics-dashboard.png "Breakdown dashboard")

Now you create in-form analytics for the Incident \[incident\] table, the Assignment Group breakdown, and the In-form Analytics - Incidents dashboard. You select the icon for the UI Action. This icon will appear next to the Assignment Group field. You also decide to create a Related Link to the dashboard.

![Creating in-form analytics for showing the dashboard with resolution time by assignment group for incidents](../image/in-form-analytics-create.png "Creating in-form analytics")

Clicking the dial icon opens the pop-up view of the dashboard. Note that instead of the dashboard name, the pop-up window is titled "Analysis of \[Breakdown name\]".

![The dashboard open from the icon next to the Assignment Group field.](../image/in-form-analytics-open-view.png "Opening dashboard view from incident form")

The Self-Service view does not show the Assignment Group field by default. In this case, you can still view the analytics from the Related Links.

![The dashboard pop-up opened from the Related Links](../image/in-form-analytics-related-link.png "Related link to analytics")

**Parent Topic:**[In-form analytics](../concept/in-form-analytics.md)

