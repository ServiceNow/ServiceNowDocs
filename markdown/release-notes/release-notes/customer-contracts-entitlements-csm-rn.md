---
title: Customer Contracts and Entitlements release notes
description: The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# Customer Contracts and Entitlements release notes

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.

## About Customer Contracts and Entitlements

-   Initiate renewals from contracts at the contract or contract line level.
-   Add new line items to an existing contract.
-   Initiate modification from the contract header.
-   Add or reduce quantities on a contract line.
-   Define pricing and quantity schedules in contracts across specific time periods.

See [Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/exploring-post-sales-support.md) for more information.

## Activation and other requirements

**Important:** Customer Contracts and Entitlements is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Customer Contracts and Entitlements by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    Customer Contracts and Entitlements is available with activation of the Customer Contracts and Entitlements \(com.sn\_pss\_core\) plugin, which requires a separate subscription. For details, see [Configure Customer Contracts and Entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/configuring-post-sales-support.md).

    **Note:** With the activation of Customer Contracts and Entitlements, new contracts and entitlements are created using the new data model only. The new entitlement verification APIs and change workflows are based on the new data model. Older contracts and entitlements can still be viewed but not modified.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/customer-service-mgmt-rn-landing.md)

## December 2025

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.

### What's new

-   **[Support Price Ramps in contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/using-customer-cnt-ent-wf.md)**

    Enable customers to specify price ramps for a product or service in a single quote. When the quote is completed and the order process is finalized, the contract captures the new pricing details.​


-   **[Enhancements in Renewals workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/create-cont-ent-workflows-csm.md)**
    -   Configure renewal opportunity and quote generation dates on separate dates.
    -   Renewed quotes automatically update when new products are added to auto-renewed contracts.

-   **[Non-Standard Renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/cce-renew-service-contract.md)**

    Renew customer contracts outside the standard renewal cycle. You can perform early renewals to generate new contracts with updated pricing terms or late renewals to extend contracts after the expiry date.


-   **[Modify line item quantities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/cce-upsell-downsell-service-contract.md)**

    Swap an existing subscribed product or service with another product, either partially or fully.


## Zurich

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.

### What's new

-   **[Renew a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/cce-renew-service-contract.md)**

    Initiate renewals from contracts at either the line level or the contract level. The resulting renewal quotes and orders generate a new contract that is associated with the original contract in the renewal history.


-   **[Add contract lines to a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/cce-add-contract-lines.md)**

    Add new line items to an existing contract by initiating the flow from contract. You can also add new line items to an existing contract while modifying a quote or contract.


-   **[Modify a service contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/cce-modify-service-contract.md)**

    Initiate a modification from the contract header to generate a quote or order containing all contract lines. You can also select specific contract lines and initiate a modification, resulting in a quote or order that includes only the selected lines.


-   **[Upsell or Downsell a service contract line](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/cce-upsell-downsell-service-contract.md)**

    Select one or more root contract lines to adjust quantities. You can add or reduce quantities on a contract line by selecting the Upsell or Downsell feature. After updating the quantities of the contract lines, a single quote or order is generated with the updated quote lines.


