---
title: Platform Analytics dashboard cache
description: Changes to the layouts of Platform Analytics dashboards are stored in the par\_dashboard\_cache table. Whenever a dashboard is called, a new entry is made in this table. Delete entries in this table to regenerate the cache for troubleshooting.
locale: en-US
release: australia
topic_type: concept
last_updated: "2024-09-26"
reading_time_minutes: 1
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Platform Analytics dashboard cache

Changes to the layouts of Platform Analytics dashboards are stored in the par\_dashboard\_cache table. Whenever a dashboard is called, a new entry is made in this table. Delete entries in this table to regenerate the cache for troubleshooting.

In the context of troubleshooting a dashboard's layout, navigate to `par_dashboard_cache_list.do` to open the PAR Dashboard Metadata Caches table. Delete a dashboard's record on this table to regenerate the cache.

These access control lists \(ACLs\) apply to the PAR Dashboard Metadata Caches **par\_dashboard\_cache** table:

-   Admin only role: report\_on, report\_view, create, write, delete
-   Any logged-in user: read

For a full guide to roles connected to Platform Analytics dashboards, see [Platform Analytics roles](../reference/platform-analytics-roles.md).

