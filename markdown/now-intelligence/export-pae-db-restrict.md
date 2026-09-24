---
title: Restrict export of Platform Analytics dashboards
description: Configure two system properties to restrict dashboard and data visualization export to specified roles or to all users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/export-pae-db-restrict.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Restrict export of Platform Analytics dashboards

Configure two system properties to restrict dashboard and data visualization export to specified roles or to all users.

## Before you begin

Role required: admin

## About this task

The export feature is enabled by default unless explicitly turned off by the system administrator. Once configured, these properties apply to all dashboards on the instance, not to individual dashboards.

-   **glide.par.export.enabled**

    Set this property to false to deny all users the ability to export dashboards. Set the property to true to enable export for all users and to enable the **glide.par.export.allowed\_roles** role.

    The **glide.par.export.enabled** property applies to:

    -   Dashboard export from the Dashboard Builder menu
    -   Visualization export from the Visualization Designer's export menu
    -   Visualization export options from the visualization's header
-   **glide.par.export.allowed\_roles**

    When **glide.par.export.enabled** is set to true, the admin can use this property to specify the roles that are permitted to export dashboards.


## Procedure

1.  Navigate to `sys_properties.list`.

2.  Open the property **glide.par.export.enabled**.

3.  Configure the property as follows:

    1.  Description: Enable or disable the export of Platform Analytics dashboards and visualizations.
    2.  Default value: `true`. When set to `false`, no user can export dashboards and visualizations.
4.  Select **Save**.

5.  Open the property **glide.par.export.allowed\_roles** and configure it as follows;

    1.  Description: Users with any of these roles can export dashboards and data visualizations.
    2.  Default value: Empty, meaning all users can export dashboards and data visualizations. Specify a comma-separated list of roles to limit this ability to only those roles.
6.  Select **Save**.


## Result

Dashboard export is restricted as configured in these two properties.

