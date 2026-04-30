---
title: Roll back migrated dashboards
description: Convert a migrated Platform Analytics dashboard back to a Core UI dashboard.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-10"
reading_time_minutes: 1
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Roll back migrated dashboards

Convert a migrated Platform Analytics dashboard back to a Core UI dashboard.

## About this task

You can return unchanged Platform Analytics dashboards to the Core UI format, but the content is iframed. This is useful when a dashboard has custom charts, custom content blocks, or custom interactive filters.

**Note:** It is not possible to roll back dashboards created in UI Builder \(also known as technical or advanced dashboards\).

## Before you begin

Role required: dashboard\_admin

## Procedure

1.  Navigate to `par_dashboard.list`.

2.  Check one or more boxes next to the names of dashboards on the list.

    Technical dashboards are identified with the phrase Advanced Dashboards in the Experience column. You cannot roll these back to Core UI dashboards.

3.  Select Rollback from the **Action on selected rows** menu.


## Result

The version of the rolled back dashboard that is shown as **Active** in the Dashboard library is the Core UI version, not the version of the dashboard migrated to Platform Analytics experience version.

