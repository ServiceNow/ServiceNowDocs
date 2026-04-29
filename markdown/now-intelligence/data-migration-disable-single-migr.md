---
title: Disable migration of single dashboards
description: Hide the banner on individual dashboards that enables owners to migrate dashboards that they own.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [How to migrate a few dashboards]
breadcrumb: [Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Disable migration of single dashboards

Hide the banner on individual dashboards that enables owners to migrate dashboards that they own.

## Before you begin

Role required: admin.

## About this task

Add a system property to prevent users from migrating their own dashboards.

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Add the system property **com.glide.par.coreui\_single\_migration.enabled** if it does not already exist.

    For more information, see [Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  Set **com.glide.par.coreui\_single\_migration.enabled** to `false`.


## Result

The banner with the button to convert individual dashboards from Core UI to Next Experience is hidden.

