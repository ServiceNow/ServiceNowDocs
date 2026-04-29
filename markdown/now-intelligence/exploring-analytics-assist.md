---
title: Explore generating or exporting dashboards and visualizations in the Now Assist panel
description: Generate and export Platform Analytics artifacts from conversational interactions. For example, ask for information about the number of open incidents and get a single-score data visualization. Then export that visualization as a PDF file, all in the Now Assist panel.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Platform Analytics in the Now Assist panel, Now Assist in Platform Analytics, Platform Analytics]
---

# Explore generating or exporting dashboards and visualizations in the Now Assist panel

Generate and export Platform Analytics artifacts from conversational interactions. For example, ask for information about the number of open incidents and get a single-score data visualization. Then export that visualization as a PDF file, all in the Now Assist panel.

## Overview of skills

There are two skills pertaining to working with data visualizations and dashboards conversationally in the Now Assist panel:

-   **Data visualization generation**

    Lets you create relevant visualizations based upon natural language questions and available data, leveraging Platform Analytics and Query Generation. The visualizations can show data from any ServiceNow AI Platform tables. The user can add the visualization to a dashboard. This skill simplifies the process of data visualization generation and configuration, potentially increasing efficiency.

-   **Dashboard and visualization export**

    Lets you export existing Platform Analytics dashboards and data visualizations conversationally, leveraging Query Generation. The available output formats depend on what you are exporting, but typically include PDF and Microsoft PowerPoint.


## Roles

The now\_assist\_panel\_user andeither now\_assist\_analytics\_generation or now.assist.creator.analytics roles are required to use the data visualization generation skill. The user must also have access to the data for which they are requesting a visualization.

The user can add a generated visualization to any dashboard to which they have editing rights.

The now\_assist\_panel\_user role is required to use the dashboard and visualization export skill. To schedule the export, the user also needs par\_scheduler.

## Activation

The data visualization generation and dashboard and visualization export skills are included with Workflow Data Fabric applications from the ServiceNow Store. You have to activate the skills after installation. For more information, see [Configuring Now Assist panel skills for Platform Analytics](configuring-now-ass-skills-pa.md).

## Supported user interfaces

Access the data visualization generation skill by starting a conversation in the Now Assist panel and asking for information available from a Platform Analytics table.

Similarly, access the dashboard and visualization export skill by starting a conversation in the Now Assist panel and asking to export a specific visualization or dashboard.

![Query asking Now Assist to show all indicators that have not been resolved for over 30 days.](../image/nowass-dv-intro.png "Asking Now Assist for a data visualization")

![Result of the query showing a list of indicators.](../image/nowass-dv-list.png "Example of a generated data visualization")

**Parent Topic:**[Generate or export dashboards and data visualizations in the Now Assist panel](../reference/analytics-assist-landing-page.md)

