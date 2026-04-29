---
title: Components installed with Retail Store Services
description: Certain roles and dependencies must be considered when using the Retail Store Services plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Retail Store Services

Certain roles and dependencies must be considered when using the Retail Store Services plugin.

**Note:**

-   The Retail Store Services application installs the dependencies Retail Core and Retail Mobile.
-   If Retail Core and Retail Mobile are already installed, then, only the com.sn\_rtl\_stre\_servcs plugin gets installed with Retail Store Services. 

## Plugins installed with Retail Store Services

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail Store Services

 \[com.sn\_rtl\_stre\_servcs\]

</td><td>

This plugin facilitates streamlined communication between store teams and headquarters \(HQ\) regarding operational questions or issues. Store team members can request help directly from HQ, ensuring their day-to-day.

</td><td>

-   com.sn\_retail\_core
-   com.sn\_retail\_mobile

</td></tr></tbody>
</table>## Roles installed with Retail Store Services

<table id="table_e44_1yr_1cc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_rtl\_stre\_servcs.agent

</td><td>

Create, update, and close store inquiry case across organizations.

</td><td>

sn\_retail.support\_agent

</td></tr><tr><td>

sn\_rtl\_stre\_servcs.agent\_manager

</td><td>

Create, update, and close store inquiry case across organizations.

</td><td>

-   sn\_rtl\_stre\_servcs.agent
-   sn\_customerservice\_manager

</td></tr><tr><td>

sn\_rtl\_stre\_servcs.contributor

</td><td>

Create, update store inquiry case for their location.

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with plugins](rahi-retail-components-installed-with-plugins.md)

