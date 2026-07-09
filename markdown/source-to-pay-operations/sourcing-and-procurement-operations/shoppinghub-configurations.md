---
title: ShoppingHub configurations
description: ShoppingHub configurations control the shopper experience for procurement workflows, including request modifications and sourcing checkouts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/shoppinghub-configurations.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-06-29"
reading_time_minutes: 2
breadcrumb: [Set up master data, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# ShoppingHub configurations

ShoppingHub configurations control the shopper experience for procurement workflows, including request modifications and sourcing checkouts.

The ShoppingHub configuration creates records that standardize the shopper experience across procurement workflows such as request modifications and sourcing checkouts. These records provide more control and flexibility over business processes.

When you enable Edit or Cancel configuration options, your shoppers can raise revision requests without contacting a support team from Service Catalog or ShoppingHub.

## ShoppingHub configuration properties

You can enable or disable specific ShoppingHub features using system properties. These toggle-based settings provide detailed control over the shopper experience without requiring code changes.

|Property name|Type|Default|Description|
|-------------|----|-------|-----------|
|`sn_spend_uib.local_currency.enable.menuoption`|Boolean|true|Enables or disables the **View prices in** currency selector in the ShoppingHub navigation menu. When set to `false`, the selector is hidden and prices revert to the default catalog currency.|
|`sn_spend_uib.purchased_behalf.enable.card_actions`|Boolean|true|Enables or disables purchase action cards \(reorder, cancel\) on the My Purchases page for users who shop on behalf of another user. When set to `false`, action buttons are suppressed for buy-on-behalf sessions.|
|`sn_shop.watchlist.user.limit`|Integer|20|Maximum number of users that can be added to the watchlist during Quick Checkout and Full Checkout. If the limit is exceeded, shoppers see an error and the save is blocked.|

To configure these properties, navigate to **System Properties** and search for the property name or filter by application scope \(`sn_spend_uib` or `sn_shop`\).

**Note:** Other ShoppingHub behavior such as catalog rules, approval policies, checkout record producers, and UI images is configured through the ShoppingHub Configuration table \(`sn_shop_shopnow_content`\), not through system properties.

-   **[Enable a shopper to purchase on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-purchase-behalf.md)**  
Configure the Shopping Hub to enable a shopper to purchase on behalf of another user.
-   **[Purchase modification configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-modification-configuration.md)**  
As an admin, you can configure the conditions that must be met for the purchase modification records to be available to the shopper for editing or canceling.
-   **[Configure sourcing checkout details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-table.md)**  
Manage the Shopping Hub configuration to standardize the request fulfillment at the checkout. You can ensure the accuracy and availability of the required items in the procurement catalogs.
-   **[Enable user actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-request-revisions.md)**  
Configure the edit and cancel options to enable modifications to the purchases.

**Parent Topic:**[Setting up primary data for ShoppingHub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/set-up-master-data-shopping-hub.md)

**Related topics**  


[Enable a shopper to purchase on behalf of another user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-purchase-behalf.md)

[Purchase modification configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/purchase-modification-configuration.md)

[Configure sourcing checkout details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-table.md)

[Enable user actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/config-shoppinghub-request-revisions.md)

