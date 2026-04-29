---
title: Set redirection for admins
description: Migrated responsive dashboards automatically redirect to the Platform Analytics experience library. However, you can set a system property to specify redirection for admins.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Perform full data migration, Platform Analytics Migration Center, Platform Analytics experience, Platform Analytics]
---

# Set redirection for admins

Migrated responsive dashboards automatically redirect to the Platform Analytics experience library. However, you can set a system property to specify redirection for admins.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Create the boolean property **com.glide.par.coreui.migration.admin\_redirection.enabled**.

    -   Set the value to true to redirect users with the admin or dashboard\_admin role from the responsive dashboard to the migrated dashboard.
    -   Set the value to false to enable users with the admin or dashboard\_admin role to open responsive dashboards in the Core UI experience.

        If Active Experience=Next for dashboards in the bridging tables, redirection is to the migrated version of the dashboard.


