---
title: Purchase on behalf of another user in Shopping Hub
description: Shoppers can purchase products and services on behalf of another user in Shopping Hub. When purchasing on behalf of another user, shoppers can also view the carts and purchases associated with that user. A shopper who is authorized to purchase on behalf of other users is referred to as a super shopper.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 3
breadcrumb: [My purchases on Shopping Hub, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase on behalf of another user in Shopping Hub

Shoppers can purchase products and services on behalf of another user in Shopping Hub. When purchasing on behalf of another user, shoppers can also view the carts and purchases associated with that user. A shopper who is authorized to purchase on behalf of other users is referred to as a super shopper.

## Key benefits

This functionality provides the following benefits:

-   Shopping controls allow administrators to define purchasing eligibility, ensuring that restricted products cannot be purchased.
-   Checkout is allowed only if the product can be shipped to the delivery location of the user on whose behalf the purchase is made. If shipping is not supported, Shopping Hub prevents the purchase from being submitted.
-   Shoppers purchasing on behalf of other users can easily view those users’ carts and purchases by selecting the user name from the filter list.

## System properties for purchasing on behalf of another user

<table id="table_txk_l3d_d3c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_shop.skip\_shopping\_controls\_for\_purchase\_on\_behalf\_of\_users

</td><td>

Controls how Shopping Hub enforces shopping control restrictions when a super shopper purchases on behalf of another user.-   Default value: false
-   When set to false, shopping control restrictions for the selected user are enforced and restricted products cannot be purchased.
-   When set to true, restricted products for the selected user display a warning, but the purchase on behalf of another user is allowed to proceed.

</td></tr><tr><td>

sn\_shop.skip\_delivery\_restrictions\_for\_purchase\_on\_behalf\_of\_users

</td><td>

Controls how Shopping Hub enforces delivery address restrictions when a super shopper purchases on behalf of another user and the product cannot be delivered to the selected user’s default delivery address.-   Default value: false
-   When set to false, products that cannot be delivered to the selected user’s delivery address cannot be purchased.
-   When set to true, a warning is displayed for non-deliverable products, and the super shopper is allowed to proceed with the purchase.

</td></tr><tr><td>

sn\_spend\_uib.purchased\_bahealf.enable.card.actions

</td><td>

Controls the availability of purchase card actions for purchases made on behalf of other users in My purchases.-   Default value: true
-   When set to true, all supported card options are available for purchases made on behalf of other users.
-   When set to false, only the **View purchase** option is available.

</td></tr></tbody>
</table>## How to configure

Role required: sn\_shop.shopping\_hub\_admin

Plugin required: Shopping Hub \(sn\_spend\_uib\)

Ensure that you configure the super shopper to purchase on behalf of other users. For more information, see [Enable a shopper to purchase on behalf of another user](../task/config-shoppinghub-purchase-behalf.md).

## How it works

The following points describe how this capability works:

To make a purchase on behalf of another user, select a product and then select the **Purchase on behalf of** check box. From the **On behalf of** list, select the user for whom the purchase is being made \(for example, Andrew Griffin\).

![Shopping Hub product page showing "Purchase on behalf of" checkbox with "Andrew Griffin" selected.](../image/sh-purchase-behalf-field.png)

After **Request to buy** is selected, the system displays the relevant details configured for the selected user, such as cost center and delivery location. These details can be modified before the request is submitted.

![Request to buy dialog showing purchase details for Andrew Griffin with delivery and cost center options.](../image/sh-purchase-behalf-details.png)

After the request is submitted, the purchase is available in My purchases. By default, the page displays purchases made by you. You can use the filter to view purchases made on behalf of other users.

Tasks are not automatically assigned to the person the item was purchased for. To ensure they can confirm receipt of the item, make sure the selected address includes the business owner’s name in the **Recipient** field. For all other tasks, the procurement specialist can reassign ownership to the business owner.

![My purchases page with the filter drop-down showing a list of users.](../image/sh-purchase-behalf-my-purchases.png)

If the **sn\_spend\_uib.purchased\_bahealf.enable.card.actions** system property is set to true, all available card options are displayed for purchases made on behalf of other users. If the property is set to false, only the View purchase option is available.

![My purchases page showing card actions menu with Inquire, Add to cart, and View purchase options.](../image/sh-purchase-behalf-cards.png)

You can also view the carts of users on whose behalf you are making purchases.

![Shopping cart interface showing user drop-down with Shirley Ross and Warren Summers options.](../image/sh-purchase-behalf-cart.png)

If a user is selected from the **Shopping for** list \(for example, Warren Summers\), the **Purchase on behalf of** check box is disabled. In this case, Shopping Hub automatically sets the purchasing capability to the selected user only.

![Shopping Hub interface showing "Shopping as" drop-down with Warren Summers selected](../image/sh-purchase-behalf-list.png)

![Shopping Hub product page with disabled "Purchase on behalf of" check box showing Warren Summers selected.](../image/sh-purchase-behalf-disabled.png)

**Parent Topic:**[My purchases on Shopping Hub](my-purchases.md)

