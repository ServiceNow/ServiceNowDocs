---
title: Launch AI Data Explorer
description: You can launch AI Data Explorer from either unified navigation or a data visualization or list . If you have the right role, you can create an exploration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/platform-analytics/launch-now-assist-explorer.html
release: zurich
product: Platform Analytics
classification: platform-analytics
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Launch AI Data Explorer

You can launch AI Data Explorer from either unified navigation or a data visualization or list . If you have the right role, you can create an exploration.

## Before you begin

Role required: now\_assist\_explorer\_user to create or edit explorations, any role to view explorations that have been shared with you.

## Procedure

1.  Perform one of the following actions:

    -   To launch AI Data Explorer from Unified Navigation, navigate to **All** &gt; **AI Data Explorer** &gt; **AI Data Explorer**.
    -   To launch AI Data Explorer from a data visualization or list, select the Explore with AI button \[Omitted image "analyze-ai-icon.png"\] Alt text: Explore with AI button.

        \[Omitted image "explore-icon-dv-tile.png"\] Alt text: Data visualization tile with Explore with AI button highlighted.

        **Note:** If the data visualization shows data from a protected scope that is not supported in Query Generation and AI Data Explorer, there is no Explore with AI icon. For more information, see [Enabling access to protected scope applications for AI Data Explorer and Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/enable-aide-secure-scope-apps.md).

2.  If you launch AI Data Explorer from a data visualization or list, choose from the following options:

    \[Omitted image "explore-options-dv.png"\] Alt text: Explore options dialog from data visualization.

    -   Ask a specific question about your data.
    -   Choose a suggested question about the data visualization, such as **Analyze trend** or **Breakdown/distribution analysis**.
    -   Add the visualization or list to a new exploration or one that is open in another tab. For more information about adding visualizations to existing explorations, see [Add an existing visualization to an exploration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/import-data-viz-list-exploration.md).
    **Important:**

    -   The data visualization or list must display table data.
    -   Supported table data sources include database views and Workflow Data Fabric tables.
    -   The table or database view must be included in the Query Generation semantic layer. For more information, see [Add a table to the semantic data layer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/add-table-semantic-layer.md).
    -   If the data is from an application with a protected scope, access to that scope must be configured. Otherwise, the Explore with AI icon does not appear.For more information, see [Enabling access to protected scope applications for AI Data Explorer and Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/enable-aide-secure-scope-apps.md).
    The results are shown in a new exploration. If you have an exploration open in another tab, you have the option to display the results there instead.

    The exploration opens in a floating panel. You can expand the dialog to a full screen or move the exploration to a new tab.

    \[Omitted image "nowass-expl-float-dialog.png"\] Alt text: Floating panel containing exploration.


**Parent Topic:**[Using AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/platform-analytics/use-now-assist-explorer.md)

