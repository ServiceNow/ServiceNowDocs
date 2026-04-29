---
title: Migrated artifact locations
description: After data migration, your artifacts such as dashboards, visualizations, and filters, reside in different tables in your instance.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Perform full data migration, Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Migrated artifact locations

After data migration, your artifacts such as dashboards, visualizations, and filters, reside in different tables in your instance.

Users with the admin, pa\_admin, report\_admin, or dashboard\_admin roles have access to the migrated artefact tables.

In addition to these tables, snpar\_sched\_export\_v\_scheduled\_export\_visualization is a virtual table for the scheduled export UI form.

|Functionality|Core UI table|Platform Analytics experience table|
|-------------|-------------|-----------------------------------|
|Dashboards|pa\_dashboards|par\_dashboard|
|Dashboard groups|pa\_dashboards\_group|analytics\_category|
|Reports|sys\_report|par\_visualization|
|PA widgets|pa\_widgets|par\_visualization|
|Interactive filters|sys\_ui\_hp\_publisher|par\_component\_filter|
|Scheduled reports|sysauto\_report|sysauto\_par, par\_export\_visualization, par\_notification\_email|

