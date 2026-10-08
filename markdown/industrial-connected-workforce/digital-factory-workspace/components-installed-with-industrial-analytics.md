---
title: Components installed with Industrial Analytics and Reporting
description: Several types of components are installed with activation of the Industrial Analytics and Reporting plugin, including dependency tables, intra-day indicators, and plugin dependencies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/components-installed-with-industrial-analytics.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Industrial Analytics and Reporting, components installed, plugin dependencies]
breadcrumb: [Industrial Analytics and Reporting, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Components installed with Industrial Analytics and Reporting

Several types of components are installed with activation of the Industrial Analytics and Reporting plugin, including dependency tables, intra-day indicators, and plugin dependencies.

## Plugin dependencies

The Industrial Analytics and Reporting plugin provides the shopfloor insights capability for Industrial Guided Tasks \(IGT\). This plugin must be activated to enable the embedded analytics dashboard on IGT standard records in the Digital Factory Workspace.

The Industrial Analytics and Reporting plugin has the following dependencies:

-   RaptorDB Pro
-   PA Premium
-   PA DataSnapshots
-   Industrial Guided Tasks

**Note:** Confirm the plugin ID and specific dependencies with your administrator or product documentation.

## Roles installed

<table id="table_fnl_wfr_pdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

-   IGT user

\[sn\_icw\_igt.user\]

-   ICW Report User

\[sn\_icw.report\_user\]


</td><td>

Required to access the available IGT standards.

 Required to access the overview tab in the dashboard. You have access to **Completed tasks \(%\)**, **Average score**, **Tasks planned per status** and **Average duration**.

</td><td>

The ICW Report User role contains the `sn_icw.user` role.

</td></tr><tr><td>

Action user

 \[sn\_icw.action\_user\]

</td><td>

Required to view the **Total actions** widget.

</td><td>

sn\_icw.user

</td></tr><tr><td>

Deviation user

 \[sn\_icw.deviation\_user\]

</td><td>

Required to view the**Total deviations** widget.

</td><td>

sn\_icw.user

</td></tr></tbody>
</table>## Intra-day indicators installed

The following intra-day indicators are installed with the plugin to support shopfloor insights:

|Indicator|Description|
|---------|-----------|
|Guided tasks opened|Automated indicator tracking the number of tasks opened.|
|Completed guided tasks|Automated indicator tracking the number of completed tasks.|
|Guided task completion %|Formula-based indicator calculating the completion percentage.|
|Average duration guided tasks|Indicator tracking the average execution duration of tasks.|
|Actions created|Indicator tracking the number of action follow-up tasks created.|
|Deviations created|Indicator tracking the number of deviation follow-up tasks created.|

## Dashboard configuration

The embedded shopfloor insights dashboard is configured with the following default settings:

-   Targets enabled: Allows setting performance targets for indicators.
-   Auto mode: For Single-score visualization, automatic aggregation is applied based on the selected time period.
-   Header separator: Displayed to organize dashboard sections.
-   Date range filtering: Applied where possible for visualizations.

## Business calendar configuration

As an ICW administrator, you can manually set up the following to support shopfloor insights:

-   Business calendar group
-   Business calendars which are automatically generated

This configuration ensures that shopfloor insights data is properly aggregated based on the shift patterns defined for each functional location.

**Parent Topic:**[Reference for Industrial Analytics and Reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/reference-for-industrial-analytics-and-reporting.md)

