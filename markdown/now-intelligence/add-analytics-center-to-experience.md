---
title: Create Platform Analytics pages in UI Builder
description: Add Platform Analytics pages to your own workspace/experience through page templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/add-analytics-center-to-experience.html
release: australia
topic_type: task
last_updated: "2026-11-12"
reading_time_minutes: 3
keywords: [workspace, experience, dashboard, data visualization, KPI Details]
breadcrumb: [Creating Platform Analytics pages, Platform Analytics experience, Platform Analytics]
---

# Create Platform Analytics pages in UI Builder

Add Platform Analytics pages to your own workspace/experience through page templates.

## Before you begin

Role required: ui\_builder\_admin

## About this task

This topic describes pages you can add to your workspace via page templates. It only describes those pages that are specific to Platform Analytics and not pages available from other teams, such as list or record pages. The pages are:

-   Dashboard library
-   Data Visualizations library
-   Dashboard
-   Visualization Designer
-   KPI Details

You can open pages for individual entries from a library page. To do so, add both the library page and the page that shows individual entries, as follows:

|Library page|Individual entry page|Required path for individual entry page|
|------------|---------------------|---------------------------------------|
|Dashboard library|Dashboards|dashboards|
|Data Visualizations library|Visualization Designer|visualization-designer|

Additionally, if you expect to have an Indicator scorecard visualization on this instance, add a KPI Details page. Viewers can then open KPI Details for an indicator by selecting the indicator from the scorecard. The KPI Details page must have the path ac\_kpi\_details.

**Important:** You must use these paths, which are the same paths of the pages in the Platform Analytics experience. The preconfigured event handlers on the pages use these paths. If you do not give your pages these paths, the event handlers will not work.

## Procedure

1.  Open your experience in the UI Builder.

2.  Select the plus \(+\) icon to add a page.

    \[Omitted image "page-add.png"\] Alt text: Add a page.

3.  Scroll to the desired template.

    This procedure shows how to use the Dashboard Library and Dashboards templates.

4.  Hold your cursor over the Dashboard Library template and select **Use template**.

    \[Omitted image "analytics-center-template.png"\] Alt text: The Dashboard Library template selected.

5.  Specify the name Dashboard library and the path `dashboard-library` and press **Continue**.

6.  In the URL parameters page, press **Looks good**.

7.  Specify the variant name, audiences, and conditions.

8.  Press **Create**.

    The page editor opens.

9.  Select **Preview** to preview the variant.

    \[Omitted image "preview-variant.png"\] Alt text: Preview variant button.

10. If all is well, select **Open URL path** to check whether the page opens.

11. Close the preview to return to the editor and then to the experience overview.

    \[Omitted image "preview-to-experience.gif"\] Alt text: Closing the preview and opening the experience page.

12. Select the plus \(+\) icon to add another page.

    \[Omitted image "page-add.png"\] Alt text: Add a page.

13. Hold your cursor over the Dashboards template and select **Use template**.

14. Name the page Dashboards with the path `dashboards` and press **Continue**

15. Repeat Step [6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/add-analytics-center-to-experience.md) to Step [10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/add-analytics-center-to-experience.md).


## Result

You can now open the Dashboard library page, select a dashboard, and open it in the Dashboards page.

## What to do next

Add more pages to the workspace, as desired.

**Parent Topic:**[Creating Platform Analytics pages in your own workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/adding-analytics-center-to-ws.md)

**Related topics**  


[Create a Platform Analytics workspace from App Engine Studio]()

[Add a dashboard to a Dashboards page]()

[Configure custom redirection from a dashboard component]()

[Dashboard URL parameter delegation]()

[Pass global filters to the dashboard page template]()

[Configure dashboard data broker]()

[Add a dashboard to a Dashboards page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/add-dashboard-to-workspace.md)

