---
title: Components installed with Retail customer complaint
description: Certain roles and dependencies must be considered when using the Retail customer complaint plugin.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with plugins, Reference, Retail]
---

# Components installed with Retail customer complaint

Certain roles and dependencies must be considered when using the Retail customer complaint plugin.

## Plugins installed with Retail customer complaint

<table id="table_a3t_sxr_1cc"><thead><tr><th>

Plugin Name

</th><th>

Description

</th><th>

Plugin Dependencies

</th></tr></thead><tbody><tr><td>

Retail Customer Complaint

 \[com.sn\_rtl\_cs\_cmplnt\]

</td><td>

The customer complaint case type helps manage and resolve customer feedback related to store experiences. This case type enables customers to submit complaints anonymously to encourage honest feedback and help stores improve their service. This case type is included in the Retail customer complaint plugin.

</td><td>

-   com.sn\_customerservice
-   com.sn\_retail\_core

</td></tr></tbody>
</table>## Roles installed with Retail Customer Complaint

<table id="table_e44_1yr_1cc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

sn\_rtl\_cs\_cmplnt.agent

</td><td>

Create, update, and resolve retail complaint cases.

</td><td>

sn\_retail.support\_agent

</td></tr><tr><td>

sn\_rtl\_cs\_cmplnt.agent\_manager

</td><td>

Create, update, resolve, and manage retail complaint cases.

</td><td>

-   sn\_rtl\_cs\_cmplnt.agent
-   sn\_customerservice\_manager

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with plugins](rahi-retail-components-installed-with-plugins.md)

