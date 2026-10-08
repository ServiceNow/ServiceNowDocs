---
title: Track a store plan on the workspace
description: Enable plan creators to track published plan execution end-to-end, overall completion status, parent \(HQ\) cases, HQ tasks, store cases, and store tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/track-hq-case.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Track and monitor store plans, Retail]
---

# Track a store plan on the workspace

Enable plan creators to track published plan execution end-to-end, overall completion status, parent \(HQ\) cases, HQ tasks, store cases, and store tasks.

## Before you begin

Role required: HQ communications: sn\_rtl\_hq\_ops.agent\_manager or sn\_rtl\_hq\_ops.location\_manager. Store audit plans: sn\_rtl\_store\_audit.plan\_author with sn\_rtl\_store\_audit.audit\_manager or sn\_rtl\_store\_audit.location\_audit\_manager.

## About this task

Enable operations teams to view, filter, and close cases, and to access cases consistently from multiple entry points, so they can drive on-time completion across all stores.

## Procedure

1.  Navigate to **Store Plans** and open the required Store Plan record.

2.  Select the **Track Plan** tab.

    The tab displays the plan progress summary and the hierarchical list view for the plan. The tab is available only when the plan is published.

3.  If the plan runs on a schedule, select an occurrence from the occurrence selector.

    The latest occurrence is selected when the tab loads. Everything on the tab is scoped to the occurrence that you select. The selector isn't displayed for One-Time or Immediate plans. For more information, see [Plan progress summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-plan-progress-summary.md).

4.  Review the progress metrics for the selected occurrence.

    The summary reports the percentage of store cases closed, and the number of open, overdue, closed, and total store cases.

5.  Select a count in the summary to open the matching tab in the hierarchical list view, or select a node in the navigation tree to review a specific part of the plan.

    The tree contains nodes for the HQ case, each HQ task, the store cases, and each store task. The store case node is selected when the tab loads.

6.  Select **All**, **Open**, **Closed**, or **Overdue** to filter the list by state.

    Each tab shows a count for the selected node. The state filter and the tree selection apply together, and the active tab is kept when you select a different node. For the states behind each tab, see [Hierarchical list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/rahi-retail-hierarchical-list-view.md).

7.  Filter store cases and store tasks by store name to narrow the list.

8.  Open a record from the list to view its details.

    The list is read-only. Records can't be created or edited from the list.


**Parent Topic:**[Track and monitor store plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/retail-industry/track-monitor-store-plans.md)

