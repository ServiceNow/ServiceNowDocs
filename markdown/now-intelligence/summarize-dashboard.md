---
title: Summarize a dashboard
description: Use AI to generate a personalized summary of any inline dashboard or workspace with output adapted to your user context including role, title, and department. When information changes, you can regenerate the summary for updated information and details about what has changed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/summarize-dashboard.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, Dashboard Summary, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Summarize a dashboard

Use AI to generate a personalized summary of any inline dashboard or workspace with output adapted to your user context including role, title, and department. When information changes, you can regenerate the summary for updated information and details about what has changed.

## Before you begin

Role required: By default, any authenticated user can access the Dashboard Summary on a dashboard. Note that admins may restrict the availability of the tool to specified roles.

Select the **Generate Summary** button in the Dashboard Summary component to request a summary of the dashboard's contents.

\[Omitted image "nowass-summarize-gen-sum.png"\] Alt text: The Generate Summary button in ServiceNow Otto context menu element

AI generates a summary and places it in the component. The dashboard summary component supports analysis across all supported dashboard visualization types and sources, including tables, Workflow Data Fabric tables, Indicators \(both classic and data snapshots\), and Usage Insights. The **Generate Summary** button is replaced with a Refresh button \[Omitted image "icon-refresh-nextexp.png"\].

The primary subjects such as widgets, segments, and features are shown in bold text. Key quantitative values that show what has changed and by how much are also in bold text.

\[Omitted image "explore-nacm.png"\] Alt text: A Now Assist Dashboard Summary

Select the **Copy** button \[Omitted image "icon-copy.png"\] to copy the generated summary to the clipboard.

To regenerate the summary, select the **Refresh** button \[Omitted image "icon-refresh-nextexp.png"\] button in the summary header.

**Note:** Cached summaries are stored for 24 hours. If the summary is refreshed in that period, it doesn't change. Cached summaries consume no assists.

Select **Refine** to shorten, elaborate, or change the tone of a generated summary.

\[Omitted image "nowass-summary-refine.png"\] Alt text: Options in the Refine menu: Change Tone &gt; Casual \| Formal \| Sympathetic, Elaborate, Shorten

Select the Thumbs up/Thumbs down icons \[Omitted image "icon-thumbs.png"\]to provide feedback on the summary.

