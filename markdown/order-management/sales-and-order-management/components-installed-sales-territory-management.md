---
title: Components installed with Sales Territory Management​
description: Several types of components are installed with activation of the Sales Territory Management​ plugin, including user roles.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Lead and opportunity management, Reference, Sales and Order Management]
---

# Components installed with Sales Territory Management​

Several types of components are installed with activation of the Sales Territory Management​ plugin, including user roles.

## Roles installed

<table id="table_cws_cgj_dhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Sales Territory Override

\[sn\_sales\_territory.sales\_territory\_override\_user\]

</td><td>

Role for overriding territory associated on Lead, Opportunity, Account, or Consumer.

</td><td>

None

</td></tr><tr><td>

Sales Territory Viewer

\[sn\_sales\_territory.sales\_territory\_viewer\]

</td><td>

Role for viewing sales territory levels, territory models, territories, and sales data.

</td><td>

-   sn\_tp.territory\_read
-   sn\_sales\_territory.sales\_territory\_basic

</td></tr><tr><td>

Sales Territory admin

\[sn\_sales\_territory.sales\_territory\_admin\]

</td><td>

Role for creating and managing sales territory levels, territory models, and territories.

</td><td>

-   sn\_lead\_mgmt\_core.lead\_viewer
-   sn\_quote\_mgmt\_core.quote\_viewer
-   sn\_tp.territory\_admin
-   sn\_opty\_mgmt\_core.opportunity\_viewer
-   sn\_tmt\_core.inbound\_queue\_read
-   sn\_customerservice.customer\_data\_viewer
-   sn\_sales\_territory.sales\_territory\_basic
-   sn\_sales\_territory.sales\_territory\_override\_user

</td></tr><tr><td>

Sales Territory Manager

\[sn\_sales\_territory.sales\_territory\_manager\]

</td><td>

Role for managing resources of the assigned territory and its child territories.

</td><td>

-   sn\_sales\_territory.sales\_territory\_basic
-   sn\_tp.territory\_resource\_manager

</td></tr><tr><td>

Sales Territory Basic

\[sn\_sales\_territory.sales\_territory\_basic\]

</td><td>

Granular role to access sales territory data.

</td><td>

None

</td></tr><tr><td>

Sales Territory Member

 \[sn\_sales\_territory.sales\_territory\_member\]

</td><td>

Role for viewing the sales territory associated on the CRM entities like Lead, Opportunity, Account, or Consumer.

</td><td>

-   sn\_tp.territory\_member
-   sn\_crm\_customer\_access\_management\_user
-   sn\_sales\_territory.sales\_territory\_basic

</td></tr></tbody>
</table>**Parent Topic:**[Lead and opportunity management reference](../concept/reference-lead-opportunity-mgt.md)

