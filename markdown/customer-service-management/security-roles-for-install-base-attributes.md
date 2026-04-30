---
title: Security roles for the Install base characteristics
description: You can assign functional and granular roles to Customer Service Management \(CSM\) users and administrators so that they can access the different capabilities and features of the Install base characteristics.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install base characteristics, Install base items, Configure Install base, Configure product data, Product data, Set up your environment, Configure, Customer Service Management]
---

# Security roles for the Install base characteristics

You can assign functional and granular roles to Customer Service Management \(CSM\) users and administrators so that they can access the different capabilities and features of the Install base characteristics.

Functional and granular roles come with varying levels of permissions for the configuration of Install base characteristics on the Customer Service Management \(CSM\) application.

The following tables describe the different functional and granular roles and their descriptions.

<table id="table_dxv_cmp_zxb"><thead><tr><th>

Role title

</th><th>

Required Plugin

</th><th>

Description

</th><th>

Contains roles

</th><th>

Added to roles

</th></tr></thead><tbody><tr><td>

sn\_install\_base.install\_base\_viewer

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\_characteristics\] and Product Catalog Management Core\] \[sn\_prd\_pm plugin

</td><td>

This role provides read access to an Install base item, its characteristics, and all the product model characteristics. This role is intended for internal users only.

</td><td>

-   sn\_ib\_chars.install\_base\_item\_characteristics\_read\_granular
-   sn\_prd\_pm.product\_model\_characteristic\_viewer
-   sn\_install\_base.install\_base\_read\_granular

</td><td>

sn\_install\_base.install\_base\_manager

</td></tr><tr><td>

sn\_install\_base.customer\_install\_base\_viewer

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\_characteristics\] and Product Catalog Management Core \[sn\_prd\_pm plugin\]

</td><td>

This role provides read access to an Install base item, its characteristics, and only the customer visible product model characteristics. This role is intended for external users only.

</td><td>

-   sn\_ib\_chars.install\_base\_item\_characteristics\_read\_granular
-   sn\_prd\_pm.product\_model\_characteristic\_granular\_viewer
-   sn\_install\_base.install\_base\_read\_granular

</td><td>

None

</td></tr><tr><td>

sn\_install\_base.install\_base\_manager

</td><td>

Customer Service Install Base Management \[com.snc.install\_base\_characteristics\]

</td><td>

This role provides access to manage the Install base items and their characteristics. This role is intended for internal users only.

</td><td>

-   sn\_ib\_chars.install\_base\_item\_characteristics\_write\_granular
-   sn\_ib\_chars.install\_base\_item\_characteristics\_create\_granular
-   sn\_install\_base.install\_base\_viewer

</td><td>

None

</td></tr></tbody>
</table><table id="table_hps_tmp_zxb"><thead><tr><th>

Role title

</th><th>

Required Plugin

</th><th>

Description

</th><th>

Contains roles

</th><th>

Added to role

</th></tr></thead><tbody><tr><td>

sn\_ib\_chars.install\_base\_item\_characteristics\_read\_granular

</td><td>

Customer Service Install Base Characteristics \[com.snc.install\_base\_characteristics\]

</td><td>

This role provides granular read access to Install base item characteristics.

</td><td>

sn\_prd\_pm.characteristics\_viewer

</td><td>

-   sn\_ib\_chars.install\_base\_item\_characteristics\_create\_granular
-   sn\_ib\_chars.install\_base\_item\_characteristics\_write\_granular
-   sn\_install\_base.install\_base\_viewer
-   sn\_install\_base.customer\_install\_base\_viewer

</td></tr><tr><td>

sn\_ib\_chars.install\_base\_item\_characteristics\_create\_granular

</td><td>

Customer Service Install Base Characteristics \[com.snc.install\_base\_characteristics\]

</td><td>

This role provides granular create access to Install base item characteristics.

</td><td>

sn\_ib\_chars.install\_base\_item\_characteristics\_read\_granular

</td><td>

sn\_install\_base.install\_base\_manager

</td></tr><tr><td>

sn\_ib\_chars.install\_base\_item\_characteristics\_write\_granular

</td><td>

Customer Service Install Base Characteristics \[com.snc.install\_base\_characteristics\]

</td><td>

This role provides granular write access to Install base item characteristics.

</td><td>

sn\_ib\_chars.install\_base\_item\_characteristics\_read\_granular

</td><td>

sn\_install\_base.install\_base\_manager

</td></tr></tbody>
</table>