---
title: Remove Core UI artifacts from the Platform Analytics library
description: Set a system property that will remove Core UI artifacts from the Platform Analytics libraries and restore the Core UI navigation paths.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/hide-platform-analytics-library-banner.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Remove Core UI artifacts from the Platform Analytics library

Set a system property that will remove Core UI artifacts from the Platform Analytics libraries and restore the Core UI navigation paths.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Locate the system property **com.glide.par.unified\_analytics.enabled**.

3.  Set the value of the property to `false`.

4.  Log out and start a new session.


## Result

Only Platform Analytics dashboards and data visualizations are listed in their respective Platform Analytics experience libraries. Core UI dashboards and reports are available under **Platform Analytics Administration** &gt; **Core UI Artifacts** &gt; **Dashboards** and **Reports**, respectively.

Non-admin users can navigate to **All** &gt; **Reports** &gt; **View/Run** and **All** &gt; **Self-Service** &gt; **Dashboards** to open the sys\_report table and pa\_dashboards\_overview, respectively. The system properties **com.snc.par.coreui.dashboard\_create.enabled** and **com.snc.par.coreui.report\_create.enabled** must be set to `true`.

## What to do next

You can revert to the default situation where all Core UI artifacts are in the Platform Analytics experience libraries by changing **com.glide.par.unified\_analytics.enabled** back to `true`. If the system properties **com.snc.par.coreui.dashboard\_create.enabled** and **com.snc.par.coreui.report\_create.enabled** are also `true`, non-admin users can create Core UI reports and dashboards from the Create actions in the libraries.

