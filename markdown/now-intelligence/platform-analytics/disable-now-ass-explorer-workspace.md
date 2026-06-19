---
title: Remove data visualization links to AI Data Explorer in a specific workspace
description: If you don't want data visualizations in a specific workspace to have an entry point for AI Data Explorer, add the workspace to the PAAI Canvas Workspace Configs table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/platform-analytics/disable-now-ass-explorer-workspace.html
release: australia
product: Platform Analytics
classification: platform-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, AI Data Explorer, Now Assist in Platform Analytics, Platform Analytics]
---

# Remove data visualization links to AI Data Explorer in a specific workspace

If you don't want data visualizations in a specific workspace to have an entry point for AI Data Explorer, add the workspace to the PAAI Canvas Workspace Configs table.

## Before you begin

Role required: now\_assist\_explorer\_admin or higher

## Procedure

1.  Navigate to **All** and search for paai\_canvas\_workspace\_config\_list.do.

2.  Select **New**.

3.  In the new PAAI Canvas Workspace Config record, select the workspace or experience from the **Experience** list.

    \[Omitted image "nowass-select-restricted-workspace.png"\] Alt text: Expanded list for selecting an experience or workspace for the Experience field.

4.  Turn on **Disabled in workspace**.

    \[Omitted image "nowass-disable-workspace.png"\] Alt text: Disable in Workspace selector in PAAI Canvas Workspace Config record.

5.  Select **Submit**.


**Parent Topic:**[Configure AI Data Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/platform-analytics/configure-now-ass-explorer.md)

