---
title: Workforce Optimization ITSM Manager Workspace components
description: The configurable ITSM Manager Workspace has roles to administer the workspace, properties to configure default behavior, and indicators to analyze performance.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Advanced configurations, Workforce Optimization for ITSM, IT Service Management]
---

# Workforce Optimization ITSM Manager Workspace components

The configurable ITSM Manager Workspace has roles to administer the workspace, properties to configure default behavior, and indicators to analyze performance.

## Roles

<table id="table_klf_rxp_dlb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Manager Workspace User \[sn\_wfo\_cfg\_ws.user\]

</td><td>

Grants read access to the Next Experience UI Builder workspace.

</td><td>

-   workspace\_user
-   canvas\_user

</td></tr><tr><td>

Manager Workspace Manager \[sn\_wfo\_cfg\_ws.manager\]

</td><td>

Grants read access to primary assignment groups and additional managers. Grants read access to home and list modules.

</td><td>

-   sn\_wfo\_cfg\_ws.user
-   sn\_wfo.user
-   sn\_wfo\_skillreview.manager

</td></tr><tr><td>

Manager Workspace Admin \[sn\_wfo\_cfg\_ws.admin\]

</td><td>

Grants administrative rights to create, read, update, and delete \(CRUD\) all applications and settings in Manager Workspace.

</td><td>

-   sn\_wfo\_cfg\_ws.manager
-   workspace\_admin
-   ui\_builder\_admin
-   canvas\_admin
-   sn\_wfo.admin

</td></tr></tbody>
</table>**Parent Topic:**[Workforce Optimization for ITSM reference](workforce-optimization-itsm-reference.md)

