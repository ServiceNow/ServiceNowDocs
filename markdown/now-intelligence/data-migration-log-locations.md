---
title: Migration log locations
description: A set of logs is stored for each dashboard, report, filter, and dashboard element \(widget\) in the bridging tables.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Perform full data migration, Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migration log locations

A set of logs is stored for each dashboard, report, filter, and dashboard element \(widget\) in the bridging tables.

Users with the admin, pa\_admin, report\_admin, or dashboard\_admin roles have access to the Migration logs. You can view the logs from within the Migration Center or navigate to the associated list to review them.

|Log|Type|
|---|----|
|par\_coreui\_migration\_bridge\_dashboard.list|Dashboard logs|
|par\_coreui\_migration\_bridge\_sysauto.list|Scheduled export logs|
|par\_coreui\_migration\_bridge\_widget.list|Migrated dashboard element logs|
|par\_coreui\_migration\_bridge\_component.list|Logs associated with reports, PA widgets, and filters when migrated outside of a dashboard|

**Note:** Logs may be empty as only negative events such as incompatibilities are logged.

