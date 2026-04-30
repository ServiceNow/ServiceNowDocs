---
title: Components installed with Retail In-store Operations
description: Certain roles and dependencies must be considered when using the Retail In-store Operations plugin.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Retail In-store Operations

Certain roles and dependencies must be considered when using the Retail In-store Operations plugin.

## Plugins installed with Retail In-store Operations

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail In-store Operations

 \[com.sn\_rtl\_in\_store\_ops\] 

</td><td>

The Retail In-store Operations plugin allows store team members to report and track in-store operational issues, whether for routine or cyclical demands. This ensures that issues are documented and monitored for consistent execution and support.

</td><td>

-   com.sn\_retail\_core
-   com.sn\_retail\_mobile
-   com.snc.fsm\_work\_types

</td></tr></tbody>
</table>## Roles installed with Retail In-store Operations

<table id="table_e44_1yr_1cc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_rtl\_in\_store\_ops.associate

</td><td>

Create, update, and close Store Operations case for their stores. Can view and close Store tasks for their stores.

</td><td>

-   sn\_retail.associate\_fulfiller
-   wm\_location\_agent

</td></tr><tr><td>

sn\_rtl\_in\_store\_ops.manager

</td><td>

Can Create, update, and close Store Operations case for the stores and associated child locations they manage. Can create, update, and close Store tasks and assign tasks to others in the stores and associated child locations they manage.

</td><td>

-   sn\_rtl\_in\_store\_ops.associate
-   sn\_retail.manager\_fulfiller
-   wm\_location\_assignment\_manager

</td></tr></tbody>
</table>## Table for in-store operations task

|Field|Example|
|-----|-------|
|Number |RIS00001 |
|Short description |Aisle 2 and 9 needs clean-up |
|Description  |Aisle 2 and 9 is cluttered and lot of products are on the floor |
|Priority |High/Medium/Low |
|Assignment Group |Store Managers Group |
|Assigned to |Store Manager  |
|Requesting retail Organization |Store of the persona, who is creating the case |
|Supporting retail organization |Same as requesting retail organization |
|Due Date |2 hours from now \(date/time\) |

**Parent Topic:**[Components installed with plugins](rahi-retail-components-installed-with-plugins.md)

