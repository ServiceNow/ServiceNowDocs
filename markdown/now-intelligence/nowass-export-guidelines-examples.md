---
title: Export guidelines and examples
description: In your prompts for the dashboard and visualization export skill, you can describe the export you want with a variable amount of detail. You are prompted for any necessary information that is missing. Before the export runs, you are asked to review the request, giving you a chance to change any options.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 2
breadcrumb: [Export dashboards and visualizations, Platform Analytics in the Now Assist panel, Now Assist in Platform Analytics, Platform Analytics]
---

# Export guidelines and examples

In your prompts for the dashboard and visualization export skill, you can describe the export you want with a variable amount of detail. You are prompted for any necessary information that is missing. Before the export runs, you are asked to review the request, giving you a chance to change any options.

![Prompt to review a request to export a dashboard.](../../../administer/now-assist-platform/images/export-request-review.png "Export request review")

Here are some example requests with different levels of detail, to use in different circumstances:

-   **Export this visualization to PowerPoint**

    If you have a dashboard or data visualization open, you do not have to specify the name. Now Assist is aware of the context. For this request, you would be asked for the export method.

-   **Export visualization Asset lifecycle by state to PPT**

    If you do not have the dashboard or visualization open, either specify its name or choose it from the list. Always specify whether you want to export a dashboard or a visualization.

-   **Export and email Usage Overview dashboard**

    As there are several dashboards with Usage Overview in the name, you are asked which one to export.

    ![Prompt to select from several dashboards with names similar to the name in the request.](../../../administer/now-assist-platform/images/export-dboard-same-name.png)

-   **Export to PowerPoint the Reports Usage tab of the Analytics Usage Overview dashboard**

    You can export an entire dashboard or a selected tab to PowerPoint. You can only export entire dashboards to PDF.

-   **Export this dashboard to PowerPoint with applied filters**

    In this case, you export the open dashboard and apply any filters on the dashboard as a whole and on any tabs. If you export a dashboard tab with applied filters, you apply only the top-level dashboard filters and the filters on that tab. You can apply filters only when exporting to PowerPoint.


**Parent Topic:**[Export dashboards and data visualizations from the Now Assist panel](../task/export-db-dv-now-assist-panel.md)

**Related topics**  


[Supported export output types](nowass-supported-export-output.md)

[Export destinations](nowass-export-destinations.md)

[Limitations for exporting dashboards and visualizations](limitations-exporting-db-dv.md)

