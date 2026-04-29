---
title: Order Management for business location
description: Integrate Service Model Foundation with Order Management to support channel sales.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with Sales and Order Management, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Order Management for business location

Integrate Service Model Foundation with Order Management to support channel sales.

## Overview of the integration

Use the Order Management Business Locations plugin \(com.snc.business\_organization\_orm\) to perform the following actions.

-   Create orders for business locations
-   Modify and manage orders for the business locations
-   Track seller and buyer details of the order

## Data model

The Customer Order Related Party \[sn\_ind\_tmt\_orm\_customer\_order\_related\_party\] table is a list of service organizations. You can add a related party record to the table to provide access to another party that is different from the service organization associated with the customer order. All related parties listed as **Authorized organizations** and associated with a particular customer order have access to the order, the order line items, and all other related entities. Channel partners such as referral partners, influencer partners, and more can be added as related parties to an order.

<table id="table_dkv_4h5_vfc"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td>

Customer Order

</td><td>

Customer order that the related party can access.

</td><td>

Reference

</td></tr><tr><td>

Type

</td><td>

Type of related party.

</td><td>

Reference

</td></tr><tr><td>

Responsibility

</td><td>

Responsibility associated with the related party.**Note:** The default responsibility is set to **default\_responsibility**.

</td><td>

Reference

</td></tr><tr><td>

Channel partner

</td><td>

Channel partner whose members can access the order when added as a related party.

</td><td>

Reference

</td></tr><tr><td>

Class

</td><td>

Class of the record.

</td><td>

sys\_class\_name

</td></tr><tr><td>

Rank

</td><td>

A numerical value to establish the priority of the relationship.

</td><td>

Integer

</td></tr><tr><td>

Domain

</td><td>

Domain of the related party record.

</td><td>

Domain ID

</td></tr><tr><td>

Active

</td><td>

Current state of the record, whether active or inactive.

</td><td>

Boolean

</td></tr></tbody>
</table>**Related topics**  


[Roles and responsibilities](personas-roles-and-tables-post-integration.md)

[Activate Order Management for Business Locations](../task/activate-order-management-for-business-locations.md)

