---
title: Overview of reporting and analytics for developers
description: Most applications that you create have some level of reporting requirements. Reports should be actionable to drive change.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create design elements, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Overview of reporting and analytics for developers

Most applications that you create have some level of reporting requirements. Reports should be actionable to drive change.

"Reporting" generally refers to showing the data inside facts tables like Incident \[incident\]. You can also create key performance indicators \(KPIs\) to track changes in this data over time, through the Performance Analytics application.

Currently the ServiceNow AI Platform® is in transition between two user interfaces for showing this information:

-   The older Core UI technology. This UI includes the Reporting application, which only shows data directly from tables, and PA Widgets, which show data from Performance Analytics indicators. Both reports and PA widgets can be placed on Core UI responsive dashboards. For more information, see Reporting, dashboards, and Performance Analytics in the Core UI.
-   The newer Platform Analytics technology. This UI includes Data Visualizations, which let you report on data from any source. These visualizations can be placed on Platform Analytics dashboards, along with Platform Analytics filters. For more information, see Platform Analytics experience.

    All Platform Analytics objects are rooted in the Next Experience UI Framework and are available to developers. However, a non-developer can still build their own objects through the Platform Analytics experience, without using UI Builder. For more information, see Platform Analytics experience.


**Note:** Although "reporting" is a general term, this documentation usually uses "report" and "reporting" to refer to the Core UI Reporting application and "visualization" or "visualize" to refer to Platform Analytics data visualizations, for disambiguation.

Follow these guidelines when building reports or data visualizations:

-   Creating reports or visualizations on large tables can negatively impact performance. Be sure to filter by a date range or other limiting criteria rather than showing all records on the table.
-   Grouping by fields that contain many possible values can negatively impact performance.
-   If loading a report or visualization gives a Long running transaction timer message, consider adding more data filters to reduce the load time.
-   If you need to export a report, data visualization, or dashboard on a regular basis, schedule the export and email.

In Platform Analytics, you have several possibilities for showing multiple data visualizations on one page:

-   Create the data visualizations and the dashboards entirely inside the Platform Analytics experience. This approach does not require a developer role or special technical knowledge, and probably should be explored before you try a more complex solution.
-   Create data visualization components in a generic UI Builder page, along with filters and other components. This approach gives you the most freedom as a developer, but also requires the most configuration.
-   Create the data visualizations and the dashboards inside the Platform Analytics experience, but then place the dashboards inside UI Builder pages using the Dashboard page template. This approach lets you use the convenience and special features of the Platform Analytics experience to create dashboards, data visualizations, and filters in your own experiences/workspaces. This approach also gives you the freedom to customize the page configuration partially. For more information, see Creating Platform Analytics pages in your own workspace.
-   Create a technical dashboard and populate it inside UI Builder. This approach is almost the same as creating your own UI Builder page from scratch, but the dashboard is available in the dashboard library, has dashboard details, and can be shared like other dashboards. For more information, see Technical dashboards.

**Parent Topic:**[Create design elements](create-design-elements.md)

