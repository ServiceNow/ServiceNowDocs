---
title: Dashboard URL parameters
description: Dashboard URL parameters allow you to control the visibility of headers and the breakdown sources of dashboards used in application pages.Use the sysparm\_group parameter to select the default value of the dashboard group on the Dashboards overview page.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Dashboard URL parameters

Dashboard URL parameters allow you to control the visibility of headers and the breakdown sources of dashboards used in application pages.

## Dashboard header

This sysparm\_header URL system parameter controls the visibility of the header of the dashboard. It has the following values:

-   hidden — The header is hidden on the application page.
-   embedded — The dashboard header appears but only has limited options. Options to refresh, reset filters, and export to PDF are available on the context menu.
-   visible \(default\) — The full header is visible on the application page.

```
<your-servicenow-instance.com>/$dashboards.do?sysparm_dashboard=ABC123&sysparm_tab=123ABC&sysparm_editable=false&sysparm_active_panel=false&sysparm_element=fed654&sysparm_element_value=def456&sysparm_breakdown_source=ghi789&sysparm_homepage_filters=%7B%ihg789%22:%5B%7B%22table%22:%22incident%22,%22filter%22:%22assignment_group%jkl212%22%7D%5D%7D&sysparm_ignore_default_filter=true&sysparm_header=embedded
```

## Dashboard breakdown​

The sysparm\_breakdown URL system parameter controls the visibility of the dashboard breakdown. It has the following values:

-   visible \(default\) — The full breakdown is visible including source and element.
-   hidden — The full breakdown is hidden​.
-   embedded — Only the breakdown element is visible.​
-   readonly — The breakdown element is visible but is read only.

```
<your-servicenow-instance.com>/$dashboards.do?sysparm_dashboard=ABC123&sysparm_tab=123ABC&sysparm_editable=false&sysparm_active_panel=false&sysparm_element=fed654&sysparm_element_value=def456&sysparm_breakdown_source=ghi789&sysparm_homepage_filters=%7B%ihg789%22:%5B%7B%22table%22:%22incident%22,%22filter%22:%22assignment_group%jkl212%22%7D%5D%7D&sysparm_ignore_default_filter=true&sysparm_breakdown=hidden
```

## Dashboard group​

The sysparm\_group URL system parameter enables you to include a single dashboard group in the dashboard picker on the Dashboards overview page. This parameter takes only the name of the dashboard group for a value.

```
<your-servicenow-instance.com>/$dashboards.do?sysparm_dashboard=ABC123&sysparm_tab=123ABC&sysparm_editable=false&sysparm_group=incident
```

## Other dashboard URL parameters

-   **sysparm\_active\_panel**

    Indicates whether the editing panel is displayed.

-   **sysparm\_editable**

    Indicates whether the editing panel can be visible.


**Parent Topic:**[Administering dashboards](../concept/c_DashboardAdministration.md)

## Dashboards overview URL parameter

Use the sysparm\_group parameter to select the default value of the dashboard group on the Dashboards overview page.

### Dashboard group

The sysparm\_group URL system parameter enables you to open the **All** tab of the Dashboards overview page \(pa\_dashboards\_overview.do\) filtered by the specified dashboard group. This parameter takes as a value only the name of a dashboard group.

**Note:** If the dashboard group specified in the URL does not exist, the URL returns the Dashboards overview page with the **Recent** tab selected.

The example URL shows only the dashboards in the group CMDB Overview.

```
<your-servicenow-instance.com>nav_to.do?uri=%2F$pa_dashboards_overview.do?sysparm_group=CMDB Overview
```

