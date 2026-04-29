---
title: Roles and responsibilities
description: After successful integration of Order Management with Service Model Foundation, various roles are added to the list view menu.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order Management for business location, Integration with Sales and Order Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Roles and responsibilities

After successful integration of Order Management with Service Model Foundation, various roles are added to the list view menu.

## Description of roles and their responsibilities

<table id="table_rnc_gcs_ffc"><tbody><tr><td>

Role

</td><td>

Description

</td><td>

Contains roles

</td></tr><tr><td>

Organization B2B Sales Representative \(sn\_bus\_org\_orm.org\_b2b\_sales\_rep\)

</td><td>

This role enables organization staff to create and manage account-related offers at their specific locations.

</td><td>

-   Location Org Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Location Order Creator \(sn\_bus\_loc\_orm.location\_order\_creator\)
-   Location Account Viewer \(sn\_bus\_loc.location\_account\_viewer\)

</td></tr><tr><td>

Organization B2B Approver \(sn\_bus\_org\_orm.org\_b2b\_approver\)

</td><td>

This role enables organization staff to approve account-related orders at their specific locations. As a B2B order approver, you can only view the customer orders that are associated with your respective location.

</td><td>

This role contains the following inherited roles.

 -   Location Org Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Location Order Viewer \(sn\_bus\_loc\_orm.location\_order\_viewer\)
-   Location Account Viewer \(sn\_bus\_loc.location\_account\_viewer\)
-   Business Organization B2B Approver \(sn\_bus\_org\_orm.org\_b2b\_approver\)

</td></tr><tr><td>

Organization B2C Sales Representative \(sn\_bus\_org\_orm.org\_b2c\_sales\_rep\)

</td><td>

This role enables organization staff to create and manage consumer-related orders at their specific locations.They can also view consumer orders and associated order line items where both Consumer and Channel partner fields are specified. As a B2C Order Approver, you can:

-   View consumer detailed and related order line items.
-   Update editable fields on the Customer Order form.
-   Update the status of orders.

</td><td>

This role contains the following inherited roles.

 -   Location Org Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Location Order Creator \(sn\_bus\_loc\_orm.location\_order\_creator\)
-   Location Consumer Viewer \(sn\_bus\_loc.location\_consumer\_viewer\)
-   Business Organization B2C Approver \(sn\_bus\_org\_orm.org\_b2c\_approver\)

</td></tr><tr><td>

Organization B2C Approver \(sn\_bus\_org\_orm.org\_b2c\_approver\)

</td><td>

This role enables organization staff to approve consumer-related orders at their specific locations.

</td><td>

This role contains the following inherited roles.

 -   Location Org Viewer \(sn\_bus\_loc.location\_org\_viewer\)
-   Location Order Viewer \(sn\_bus\_loc\_orm.location\_order\_viewer\)
-   Location Consumer Viewer \(sn\_bus\_loc.location\_consumer\_viewer\)
-   Business Organization B2C Sales Approver \(sn\_bus\_org\_orm\_org.b2c\_sales\_approver\)

</td></tr><tr><td>

Organization Sales Manager \(sn\_bus\_org\_orm.org\_sales\_mgr\)

</td><td>

This role enables enterprise sales persona to create, manage, and approve account and consumer related orders for their assigned organizational hierarchy.They can view consumer-related orders and order line items across both parent and child business locations.

The Location Sales Manager has full access to create and approve all order types, including both B2B and B2C orders.

</td><td>

This role contains the following inherited roles

 -   Location Org Hierarchy Viewer \(sn\_bus\_loc.location\_org\_hierarchy\_viewer\)
-   Location Customer Order Agent \(sn\_bus\_loc\_orm.location\_customer\_order\_agent\)
-   Location Customer Order Approver \(sn\_bus\_loc\_orm.location\_customer\_order\_approver\)
-   Location Consumer Order Agent \(sn\_bus\_loc\_orm.location\_customer\_order\_agent\)
-   Location Consumer Order Approver \(sn\_bus\_loc\_orm.location\_consumer\_order\_approver\)

</td></tr><tr><td>

sn\_bus\_org\_orm.org\_ui

</td><td>

Granular role for organization staff to ensures consistent sales order experience across all user interfaces.

</td><td>

None

</td></tr></tbody>
</table>Apart from the functional roles, users also need to have the Business organization UI \(sn\_bus\_org\_orm.org\_ui\) granular role to have a uniform experience across all user interfaces.

