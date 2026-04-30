---
title: Application plugin installation sequence in Purchase Order Management
description: View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Purchase Order Management.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [app installation sequence, Purchase order management installation, plugins]
breadcrumb: [Install Purchase Order Management, Configure, Purchase Order Management, Source-to-Pay Operations, Finance and Supply Chain]
---

# Application plugin installation sequence in Purchase Order Management

View the consolidated list of plugins, high-level description of each plugin, and the dependencies that are required before installing each plugin in Purchase Order Management.

## Application plugin list

<table id="table_ep1_c32_q2c"><thead><tr><th>

Plugin name

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

Sourcing and Purchasing Automation \(com.snc.sn\_pr\)

</td><td>

Provides workflows and automation for sourcing requests, negotiations, and purchase requisitions.

</td><td>

-   Source-to-Pay Common Architecture \(com.snc.sn\_shop\)
-   Supplier Common Architecture \(com.snc.sn\_slm\)

</td></tr><tr><td>

Purchase Order Management \(com.snc.sn\_poem\_core\)

</td><td>

Enables operational buyers and suppliers to flag purchase order issues and resolve them efficiently.

</td><td>

Sourcing and Purchasing Automation \(com.snc.sn\_pr\)

</td></tr><tr><td>

Advanced Work Assignment for Source-to-Pay Operations \(snc.sn\_spend\_awa\)

</td><td>

Provides configurations to support automatic routing, queuing, and assignment of finance cases and emails.

</td><td>

Advanced Work Assignment \(glide.awa\)

</td></tr></tbody>
</table>**Parent Topic:**[Install Purchase Order Management](../task/install-purch-order-mgmt.md)

