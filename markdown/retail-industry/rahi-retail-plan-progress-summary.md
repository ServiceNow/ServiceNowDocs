---
title: Plan progress summary
description: The plan progress summary gives headquarters and regional managers a single view of how a published plan is progressing for a selected schedule occurrence, without opening individual cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/retail-industry/rahi-retail-plan-progress-summary.html
release: australia
topic_type: concept
last_updated: "2026-10-05"
reading_time_minutes: 2
breadcrumb: [Track and monitor store plans, Retail]
---

# Plan progress summary

The plan progress summary gives headquarters and regional managers a single view of how a published plan is progressing for a selected schedule occurrence, without opening individual cases.

The plan progress summary appears on the **Track Plan** tab of a store plan. The tab is displayed as the first tab on the template and appears only when the template is in the Published state.

The tab requires both the Planned Work Management and Multi Case Creation plugins to be active. If either plugin is inactive, the tab is not displayed.

The summary supports the plan types provided with the base system, HQ Communications and Store Audit. Custom plan types that use complex configuration might require additional configuration before the summary reports on them accurately.

## Selecting a schedule occurrence

Plans that run on a schedule generate a separate set of cases and tasks for each occurrence. The occurrence selector lists the occurrences that are in the Scheduled state and scopes everything on the tab to the occurrence that you select.

-   The latest occurrence is selected when the tab loads. If no occurrence is currently running, the most recently completed occurrence is selected.
-   The selector is not displayed for plans with a One-Time or Immediate schedule, because those plans produce a single set of records.
-   The due date for the selected occurrence is shown in the summary header. It is omitted for plans where a due date doesn't apply.

## Progress metrics

The summary reports the following metrics for the selected occurrence. Selecting a case count opens the matching tab in the hierarchical list view, with the tree positioned on the store case node.

|Metric|Description|Selectable|
|------|-----------|----------|
|Store Cases Closed \(%\)|The proportion of generated store cases that are closed, calculated as the total closed store cases divided by the total store cases generated. The value is rounded to the nearest whole number and shown without decimal places.|No|
|Open Store Cases|The number of store cases in an open state for the selected occurrence.|Yes|
|Overdue Store Cases|The number of store cases in an open state for the selected occurrence whose due date and time have passed.|Yes|
|Closed Store Cases|The number of store cases in a closed state for the selected occurrence.|Yes|
|All Store Cases|The total number of store cases generated for the selected occurrence.|Yes|

For the states that count as open, closed, and overdue for each type of record, see [Hierarchical list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/rahi-retail-hierarchical-list-view.md).

**Note:** For plans with a Recurring or Immediate schedule type, an empty state shows the schedule details until cases and tasks are generated, or start generating, for a schedule occurrence.

After you manually refresh the page, the data view appears if cases and tasks have been generated for at least one schedule occurrence.

**Parent Topic:**[Track and monitor store plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/retail-industry/track-monitor-store-plans.md)

