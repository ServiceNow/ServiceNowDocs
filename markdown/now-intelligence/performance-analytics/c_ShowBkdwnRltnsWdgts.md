---
title: Showing breakdown relations on dashboards
description: A breakdown widget can display 1st level breakdown elements that are related to the element selected for the dashboard. The widget must be on a breakdown dashboard, and that dashboard must include the breakdown sources of the related breakdowns.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/performance-analytics/c\_ShowBkdwnRltnsWdgts.html
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using breakdowns on dashboards, Indicator breakdowns, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Showing breakdown relations on dashboards

A breakdown widget can display 1st level breakdown elements that are related to the element selected for the dashboard. The widget must be on a breakdown dashboard, and that dashboard must include the breakdown sources of the related breakdowns.

**Note:** You cannot select more than one element on the dashboard for a widget that shows breakdown relations.

Consider an indicator such as Number of open incidents. This indicator uses the Location breakdown. The Location breakdown has three breakdown relations between its own elements. For an element of Location, these relations are:

-   Parent Locations, whose Sys ID value is in the Parent field of other Location elements.
-   Child Locations, which have the Sys ID value of another Location element in their Parent fields.
-   Sibling Locations, consisting of Location elements who share the same value in the Parent field.

\[Omitted image "breakdown-relations-assignment-group.png"\] Alt text: The three breakdown relations of the Location breakdown

Now consider a widget that displays the Number of open incidents indicator scores grouped by Location. You set the widget to follow an element selected in a breakdown dashboard. Now you must select which of the breakdown relations to follow.

\[Omitted image "bkdown-scorecard-widget-w-bkdown-rel.png"\] Alt text: Form for creating a breakdown widget with an Analytics Hub visualization showing the choice of breakdown relations to follow

**Important:** The **Followed breakdown relation** menu works only when the **Scorecard** visualization is selected. To allow the user to follow breakdown relations with other visualizations, select **Show visualization selector** on the widget form.

You select Child Locations. Now you put the widget in a breakdown dashboard that uses the Locations breakdown source. Locations is the breakdown source of the Location breakdown, so on the dashboard you can select any of the elements of Location. If you select EMEA, the widget shows the locations that have EMEA as a parent.

\[Omitted image "Breakdown\_relations\_widget.png"\] Alt text: A widget on a breakdown dashboard showing the child locations of the EMEA group

You can go down more levels, to "grandchild" and "great-grandchild" elements. For example, here the location of Germany is selected:

\[Omitted image "bkdwn-relation-germany.png"\] Alt text: Breakdown widget with Germany selected, showing its child elements

If you edit the widget to display the Parent Location instead of the Child Locations and select Germany on the dashboard again, you see the parent location of Germany.

\[Omitted image "breakdown-relations-sibling-group.png"\] Alt text: A widget on a breakdown dashboard showing the sibling locations of the EMEA group

**Parent Topic:**[Using breakdowns on dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_SpecialDashboards.md)

**Related topics**  


[Add breakdown sources to a dashboard]()

[Configure widgets for breakdown dashboards]()

[Showing multiple elements separately or aggregated]()

[Same breakdown on widget and dashboard]()

[Navigating breakdown elements with breakdown relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/breakdown-relations.md)

[Create a scorecard visualization for a breakdown widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/create-scorecard-widget.md)

