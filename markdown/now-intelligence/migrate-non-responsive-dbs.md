---
title: Migrate non-responsive dashboards
description: Non-responsive dashboards that no one has opened migrate to the Platform Analytics experience with empty tabs. Open these dashboards in the Core UI before migration to populate them.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Unmigrated solutions dashboard, Unmigrated out of the box dashboard, Empty dashboards]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migrate non-responsive dashboards

Non-responsive dashboards that no one has opened migrate to the Platform Analytics experience with empty tabs. Open these dashboards in the Core UI before migration to populate them.

## Before you begin

Role required: admin

Unopened non-responsive dashboards have empty canvas pages. This issue affects solutions dashboards as well as dashboards that users create. Opening the dashboard creates the canvas page that the Migration Center looks for. Once the canvas pages are created, re-trigger the migration to create the Platform Analytics experience version of the dashboard.

## Procedure

1.  Navigate to `pa_dashboards.list`.

2.  Open each of the problematic non-responsive dashboards.

3.  [Perform full data migration](data-migration-perform.md) to migrate these dashboards to Platform Analytics experience.


