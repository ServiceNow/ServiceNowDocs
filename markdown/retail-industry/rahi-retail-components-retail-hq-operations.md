---
title: Components installed with Retail HQ Operations
description: Certain roles and dependencies must be considered when using the Retail HQ Operations plugin.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Retail reference, Retail]
---

# Components installed with Retail HQ Operations

Certain roles and dependencies must be considered when using the Retail HQ Operations plugin.

## Plugins installed with Retail HQ Operations

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail HQ Operations

 \[com.sn\_rtl\_hq\_ops\] 

</td><td>

The Retail HQ Operations plugin enables effective coordination between HQ teams. It facilitates the execution of assigned work and allows HQ teams to monitor progress.

</td><td>

com.sn\_retail\_core

</td></tr></tbody>
</table>## Roles installed with Retail HQ Operations

<table id="table_e44_1yr_1cc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_rtl\_hq\_ops.agent

</td><td>

Create, update, and resolve HQ communications case.

</td><td>

sn\_retail.support\_agent

</td></tr><tr><td>

sn\_rtl\_hq\_ops.agent\_manager

</td><td>

Create, update, and resolve HQ communications case. The agent manager also manages the agents.

</td><td>

-   sn\_rtl\_hq\_ops.agent
-   sn\_customerservice\_manager

</td></tr><tr><td>

sn\_rtl\_hq\_ops.location\_agent

</td><td>

Create, update, and resolve HQ communications case for their location.

</td><td>

sn\_retail.associate\_fulfiller

</td></tr><tr><td>

sn\_rtl\_hq\_ops.location\_agent

</td><td>

Create, update, and resolve HQ communications case for their location.

</td><td>

-   sn\_rtl\_hq\_ops.location\_agent
-   sn\_retail.manager\_fulfiller

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with plugins](rahi-retail-components-installed-with-plugins.md)

