---
title: Export dashboards and data visualizations from the ServiceNow Otto panel
description: Export or schedule the export of dashboards and data visualizations conversationally through AI instead of going through the Platform Analytics user interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/export-db-dv-now-assist-panel.html
release: zurich
topic_type: task
last_updated: "2025-08-07"
reading_time_minutes: 2
keywords: [export, schedule, schedule export, Now Assist, Now Assist Panel, Platform Analytics AI]
breadcrumb: [Platform Analytics in the ServiceNow Otto panel, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Export dashboards and data visualizations from the ServiceNow Otto panel

Export or schedule the export of dashboards and data visualizations conversationally through AI instead of going through the Platform Analytics user interface.

## Before you begin

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

Role required: now\_assist\_panel\_user. To schedule an export, you also need par\_scheduler. You need access to the dashboard or the data in the visualization.

## Procedure

1.  Open the ServiceNow Otto panel.

    \[Omitted image "nowass-open-nowass-panel.png"\] Alt text: Control for opening the Now Assist panel.

    \[Omitted image "otto-panel-landing.png"\] Alt text: Initial ServiceNow Otto panel.

2.  Select **View all** then search for `Export`.

3.  Select **Dashboard and data visualization export**.

    \[Omitted image "dash-viz-export.png"\] Alt text: ServiceNow Otto panel showing the Dashboard and visualization export skill.

4.  Engage in an iterative conversation until ServiceNow Otto produces the export you want.

    -   Choose whether you want to download the export, send it by email, or schedule a regular export by email.
    -   Choose whether you want to export a dashboard or a data visualization.
    -   Specify the name of the data visualization or dashboard to export.
    -   Specify the desired output type.
    **Important:** You can only export dashboards or data visualizations that have been saved to the library. However, if you export a dashboard, you export all visualizations on that dashboard, including those that were not saved to the library.

    For more information, see the topics linked after this procedure.


## What to do next

**Tip:** After an export request is complete, reset the conversation before beginning a new request. Otherwise, some option selections might carry over to the new request. If this happens anyway, consider clearing your browser cache.

-   **[Supported export output types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/nowass-supported-export-output.md)**  
The dashboard and visualization output skill supports the same outputs for the same data visualizations as Platform Analytics generally.
-   **[Export destinations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/nowass-export-destinations.md)**  
When you export a dashboard or data visualization in the ServiceNow Otto panel, you have to specify the destination.
-   **[Limitations for exporting dashboards and visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/limitations-exporting-db-dv.md)**  
The dashboard and visualization export skill supports only some dashboards for export. Requests for export are not always recognized or understood correctly.
-   **[Export guidelines and examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/nowass-export-guidelines-examples.md)**  
In your prompts for the dashboard and visualization export skill, you can describe the export you want with a variable amount of detail. You are prompted for any necessary information that is missing. Before the export runs, you are asked to review the request, giving you a chance to change any options.

**Parent Topic:**[Dashboards and data visualizations in the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/analytics-assist-landing-page.md)

**Related topics**  


[Export a data visualization from the Visualization Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/export-visualization-vd.md)

[Export a Platform Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/export-pae-dashboard-ppt.md)

[Schedule the export of data visualizations or dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/schedule-visn-export-vd.md)

