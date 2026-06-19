---
title: Using Dashboard Summary
description: Enable users of Platform Analytics experience dashboards to generate summaries of a dashboard's content using AI.Use AI to generate a summary of an inline dashboard. When information on the dashboard changes, you can regenerate the summary for updated information and details about what has changed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/platform-analytics/use-now-assist-cm.html
release: australia
product: Platform Analytics
classification: platform-analytics
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Dashboard Summary, Now Assist in Platform Analytics, Platform Analytics]
---

# Using Dashboard Summary

Enable users of Platform Analytics experience dashboards to generate summaries of a dashboard's content using AI.

**Note:** The following dashboard elements aren't supported in the Dashboard Summary:

-   Process Mining - Map
-   Usage Insights Funnel
-   iFrame

## Summarize a dashboard

Use AI to generate a summary of an inline dashboard. When information on the dashboard changes, you can regenerate the summary for updated information and details about what has changed.

### Before you begin

Role required: By default, any authenticated user can access the Dashboard Summary on a dashboard. Note that admins may restrict the availability of the tool to specified roles.

Select the **Generate Summary** button in the Dashboard Summary component to request a summary of the dashboard's contents.

\[Omitted image "nowass-summarize-gen-sum.png"\] Alt text: The Generate Summary button in Now Assist context menu element

AI generates a summary and places it in the component. The dashboard summary component supports analysis across all supported dashboard visualization types and sources, including tables, Workflow Data Fabric tables, Indicators \(both classic and data snapshots\), and Usage Insights.The **Generate Summary** button is replaced with a Refresh button \[Omitted image "icon-refresh-nextexp.png"\].\[Omitted image "explore-nacm.png"\] Alt text: A Now Assist Dashboard Summary

Select the **Copy** button \[Omitted image "icon-copy.png"\] to copy the generated summary to the clipboard.

To regenerate the summary, select the **Refresh** button \[Omitted image "icon-refresh-nextexp.png"\] button in the summary header.

**Note:** Cached summaries are stored for 24 hours. If the summary is refreshed in that period, it doesn't change. Cached summaries consume no assists.

Select **Refine** to shorten, elaborate, or change the tone of a generated summary.

\[Omitted image "nowass-summary-refine.png"\] Alt text: Options in the Refine menu: Change Tone &gt; Casual \| Formal \| Sympathetic, Elaborate, Shorten

Select the Thumbs up/Thumbs down icons \[Omitted image "icon-thumbs.png"\]to provide feedback on the summary.

