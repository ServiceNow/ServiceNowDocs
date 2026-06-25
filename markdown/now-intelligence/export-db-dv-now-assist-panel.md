---
title: Export dashboards and data visualizations from the Now Assist panel
description: Export or schedule the export of dashboards and data visualizations conversationally through AI instead of going through the Platform Analytics user interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/export-db-dv-now-assist-panel.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [export, schedule, schedule export, Now Assist, Now Assist Panel, Platform Analytics AI]
breadcrumb: [Platform Analytics in the Now Assist panel, Now Assist in Platform Analytics, Platform Analytics]
---

# Export dashboards and data visualizations from the Now Assist panel

Export or schedule the export of dashboards and data visualizations conversationally through AI instead of going through the Platform Analytics user interface.

## Before you begin

Role required: now\_assist\_panel\_user. To schedule an export, you also need par\_scheduler. You need access to the dashboard or the data in the visualization.

## Procedure

1.  Open the Now Assist panel.

    \[Omitted image "nowass-open-nowass-panel.png"\] Alt text: Control for opening the Now Assist panel.

2.  From the options, select **Dashboard and visualization export**.

    \[Omitted image "dash-viz-export.png"\] Alt text: Now Assist panel showing Dashboard and visualization export.

3.  Engage in an iterative conversation until Now Assist produces the export you want.

    -   If you want an immediate export, specify the word "Export" in your prompt. If you want to schedule an export, specify "Schedule."
    -   Specify the name of the data visualization or dashboard.
    -   Specify the word "visualization" or "dashboard" depending on what you want to export. Specify the word multiple times for best results.
    -   Specify the desired output type.
    -   Specify whether you want to download the export or have it emailed.
    -   You can only export dashboards or data visualizations that have been saved to the library.
    -   Although you can directly export only visualizations that are in the library, if you export a dashboard, you export all visualizations on that dashboard, including those that were not saved to the library.
    For more information, see the topics linked after this procedure.


## What to do next

**Tip:** After an export request is complete, reset the conversation before beginning a new request. Otherwise, some option selections might carry over to the new request. If this happens anyway, consider clearing your browser cache.

-   **[Supported export output types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/nowass-supported-export-output.md)**  
The dashboard and visualization output skill supports the same outputs for the same data visualizations as Platform Analytics generally.
-   **[Export destinations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/nowass-export-destinations.md)**  
When you export a dashboard or data visualization in the Now Assist panel, you have to specify the destination.
-   **[Limitations for exporting dashboards and visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/limitations-exporting-db-dv.md)**  
The dashboard and visualization export skill supports only some dashboards for export. Requests for export are not always recognized or understood correctly.
-   **[Export guidelines and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/nowass-export-guidelines-examples.md)**  
In your prompts for the dashboard and visualization export skill, you can describe the export you want with a variable amount of detail. You are prompted for any necessary information that is missing. Before the export runs, you are asked to review the request, giving you a chance to change any options.

**Parent Topic:**[Generate or export dashboards and data visualizations in the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-assist-landing-page.md)

**Related topics**  


[Export a data visualization from the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/export-visualization-vd.md)

[Export a Platform Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/export-pae-dashboard-ppt.md)

[Schedule the export of data visualizations or dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/schedule-visn-export-vd.md)

