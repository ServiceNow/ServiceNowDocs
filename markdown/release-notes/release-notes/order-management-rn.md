---
title: Order Management release notes
description: The ServiceNow Order Management application enables you to capture, manage, and fulfill product and service orders from enterprise customers. Order Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Order Management release notes

The ServiceNow® Order Management application enables you to capture, manage, and fulfill product and service orders from enterprise customers. Order Management was enhanced and updated in the Australia release.

## Order Management highlights for the Australia release

-   Enable agents and customers to make faster, more confident decisions on orders by instantly seeing the impact of price and quantity changes, ensuring clarity on what's owed for every update.
-   Improve order approval accuracy by validating contract start and end dates and terms for recurring and entitlement orders, while preventing contract dates from being set on one-time orders. This helps orders process correctly the first and contract obligations to be properly tracked.
-   Enhance the Order management \(OM\) integration with Strategic Portfolio Management \(SPM\) for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.

See [Order management](https://www.servicenow.com/docs/access?context=explore-order-management&version=australia&pubname=australia-order-management&ft:locale=en-US) for more information.

**Important:** Order Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Delta pricing on orders](https://www.servicenow.com/docs/access?context=net-pricing-sp-contracts&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Calculate pricing and quantity changes during MACD activities and renewals by deriving deltas from existing products, contracts, or purchases. This improves accuracy when processing order modifications.

    -   Defaults contract type and contract line type when empty, based on the order and line actions being performed.
    -   Adds delta pricing–related header and line fields, along with pricing adjustment rule identifiers and conditions, and supports mapping these fields across order, product instance, and order copy flows.
-   **[Price and quantity ramps on order line items](https://www.servicenow.com/docs/access?context=defining-products-with-ramps&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    View price and quantity ramps directly on order line items to model planned changes over time within a single order, providing visibility into pricing changes without managing multiple orders. For more information, see the [Product Catalog Management and Pricing Management release notes](product-catalog-pricing-management-rn.md)

-   **[Manage order updates with Now Assist](https://www.servicenow.com/docs/access?context=bulk-update-order-lines-with-now-assist&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Use a conversational AI assistant to improve order triage and resolution. The assistant understands order context and supports guided actions such as updating shipping addresses and quantities across order line items. For more information, see the .


## Changed in this release

-   **[Managing inflight order for site projects](https://www.servicenow.com/docs/access?context=inflight-offering-somt&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    Use the OM integration with SPM for in-flight orders to support projects for site and maintain program project and sub-project hierarchy.


## Activation information

Install Order Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[CPQ Configurator](https://www.servicenow.com/docs/access?context=explore-servicenowcpq&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    The CPQ Configurator interface streamlines the process of configuring and pricing customizable products in Sales and Order Management transactions, such as quotes and orders.


-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    The Pricing Management application enables your pricing organization to set, manage, and optimize pricing strategies for any Sales and Order Management solution. These pricing strategies enable your sales teams to generate opportunities, quotes, and orders with accurate and competitive pricing quickly.

-   **[Sales Agreement Management](https://www.servicenow.com/docs/access?context=sales-agreement-mgmt&version=australia&pubname=australia-order-management&ft:locale=en-US)**

    The Sales Agreement application captures the scope and conditions from a quote for future sales transactions, over a specified period between a buyer and a seller.


**Parent Topic:**[Sales and Order Management release notes](sales-order-management-rn-landing.md)

