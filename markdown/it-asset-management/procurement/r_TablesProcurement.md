---
title: Tables installed with Procurement
description: Procurement plugin adds the following tables.
locale: en-US
release: xanadu
product: Procurement
classification: procurement
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with Procurement, Activate Procurement, Procurement, IT Asset Management]
---

# Tables installed with Procurement

Procurement plugin adds the following tables.

<table id="table_yfh_trv_dp"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Purchase Order \[proc\_po\]

</td><td>

Stores information about items ordered, cost of items ordered, and users that require the items for orders placed with a vendor.**Note:** The asset, procurement\_user, inventory\_admin, or contract\_manager role can only access the reports. You must activate the Hardware Asset Management Professional \(com.sn\_hamp\) plugin for the contract\_manager and inventory\_admin role.

</td></tr><tr><td>

Purchase order line items \[proc\_po\_item\]

</td><td>

Stores information about items and quantity ordered on purchases orders.**Note:** The asset, procurement\_user, inventory\_admin, or contract\_manager role can only access the reports. You must activate the Hardware Asset Management Professional \(com.sn\_hamp\) plugin for the contract\_manager and inventory\_admin roles.

</td></tr><tr><td>

Receiving Slip \[proc\_rec\_slip\]

</td><td>

Stores receiving information for items ordered with a purchase order. Can reference multiple receiving slip lines.

</td></tr><tr><td>

Receiving Slip Line \[proc\_rec\_slip\_item\]

</td><td>

Stores receiving information for items ordered on a specific purchase order line, such as the items ordered, quantity ordered, and who ordered them.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Procurement](r_InstalledWithProcurement.md)

