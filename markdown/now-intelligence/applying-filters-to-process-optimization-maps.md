---
title: Applying filters to Process Mining maps
description: If a dashboard filter is on the same table as the breakdown of a process project, that filter can apply to a Process Mining map of that project.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/applying-filters-to-process-optimization-maps.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a Process Mining map on a dashboard, Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Applying filters to Process Mining maps

If a dashboard filter is on the same table as the breakdown of a process project, that filter can apply to a Process Mining map of that project.

You can apply a single-select or true/false filter to a Process Mining map.

## Single-select filter on Process Mining maps

For a single-select filter to apply to a Process Mining map, the filter source and the data to filter must both be on the same table as the table of the process project. Furthermore, they must be on a field of that table that is also a breakdown of the process project.

For example, consider a process project on the Incident \[incident\] table. The breakdown filters for this project include the Category field. In the Process Mining Workspace, you can see the breakdowns in the Breakdown Filters column of the Analyst Workbench for the project.

\[Omitted image "po-map-project-bkdowns.png"\] Alt text: Analyst Workbench showing breakdowns

You can also see and change the breakdowns in the table configuration record for the project. For more information, see [Configure a breakdown definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/configure-breakdown.md).

In the dashboard where you have added your Process Mining map for this project, you want users to be able to filter the map by Category. Category is a breakdown of the process project, so it is simple to add such a filter. When you create the filter, select the Incident table, then the Category field. This selection automatically applies to both the filter source and the date to filter, as described in [Configure a Single/Multiple select or cascading filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-select-filter-workspace.md).

\[Omitted image "po-map-filter-singleselect-source.png"\] Alt text: Filter configuration showing the process project table and breakdown field

The filter applies to the Process Mining map the same as it does to a bar visualization of the Incident table.

\[Omitted image "po-map-filtering-category.gif"\] Alt text: Both a Process Mining map and a Bar data visualization filtered by the Network category

## True/false filter on Process Mining maps

For a true/false filter, you only select the data to filter. Again, select the table of the process project and a field that is used as a breakdown. Continuing with the project from the Single Select filter example, Active is a true/false, or Boolean, field that is used as a breakdown. Therefore, you can set a true/false filter to filter Incident.Active, and it will filter the Process Mining map. For more information, see [Configure a True/False filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-boolean-filter-workspace.md).

\[Omitted image "po-map-set-incident-active.png"\] Alt text: True/false filter configured to filter the Active field of the Incident table

Again, the filter affects both a data visualization and a Process Mining map on the Incident table.

\[Omitted image "po-map-apply-true-false.gif"\] Alt text: Both a Process Mining map and a Bar data visualization filtered by whether Active is true

