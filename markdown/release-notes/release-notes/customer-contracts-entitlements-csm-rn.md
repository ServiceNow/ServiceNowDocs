---
title: Customer Contracts and Entitlements release notes
description: The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Customer Contracts and Entitlements release notes

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Zurich release.

## Customer Contracts and Entitlements highlights for the Zurich release

-   Initiate renewals from contracts at the contract or contract line level.
-   Add new line items to an existing contract.
-   Initiate modification from the contract header.
-   Add or reduce quantities on a contract line.
-   Define pricing and quantity schedules in contracts across specific time periods.

See [Customer Contracts and Entitlements](https://www.servicenow.com/docs/access?context=exploring-post-sales-support&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** Customer Contracts and Entitlements is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Renew a service contract](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Initiate renewals from contracts at either the line level or the contract level. The resulting renewal quotes and orders generate a new contract that is associated with the original contract in the renewal history.


-   **[Add contract lines to a service contract](https://www.servicenow.com/docs/access?context=cce-add-contract-lines&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Add new line items to an existing contract by initiating the flow from contract. You can also add new line items to an existing contract while modifying a quote or contract.


-   **[Modify a service contract](https://www.servicenow.com/docs/access?context=cce-modify-service-contract&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Initiate a modification from the contract header to generate a quote or order containing all contract lines. You can also select specific contract lines and initiate a modification, resulting in a quote or order that includes only the selected lines.


-   **[Upsell or Downsell a service contract line](https://www.servicenow.com/docs/access?context=cce-upsell-downsell-service-contract&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Select one or more root contract lines to adjust quantities. You can add or reduce quantities on a contract line by selecting the Upsell or Downsell feature. After updating the quantities of the contract lines, a single quote or order is generated with the updated quote lines.


-   **[Support Price Ramps in contract](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Enable customers to specify price ramps for a product or service in a single quote. When the quote is completed and the order process is finalized, the contract captures the new pricing details.​


-   **[Enhancements in Renewals workflow](https://www.servicenow.com/docs/access?context=create-cont-ent-workflows-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**
    -   Configure renewal opportunity and quote generation dates on separate dates.
    -   Renewed quotes automatically update when new products are added to auto-renewed contracts.

-   **[Non-Standard Renewals](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Renew customer contracts outside the standard renewal cycle. You can perform early renewals to generate new contracts with updated pricing terms or late renewals to extend contracts after the expiry date.


-   **[Modify line item quantities](https://www.servicenow.com/docs/access?context=cce-upsell-downsell-service-contract&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Swap an existing subscribed product or service with another product, either partially or fully.


## Activation information

Install Customer Contracts and Entitlements by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Customer Contracts and Entitlements is available with activation of the Customer Contracts and Entitlements \(com.sn\_pss\_core\) plugin, which requires a separate subscription. For details, see [Configure Customer Contracts and Entitlements](https://www.servicenow.com/docs/access?context=configuring-post-sales-support&version=zurich&pubname=zurich-order-management&ft:locale=en-US).

**Note:** With the activation of Customer Contracts and Entitlements, new contracts and entitlements are created using the new data model only. The new entitlement verification APIs and change workflows are based on the new data model. Older contracts and entitlements can still be viewed but not modified.

## Related ServiceNow applications and features

-   **[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-components&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    ServiceNow® Workflow Studio components enable you to invoke flows or subflows that are part of a workflow and are used to find out the output or execution status of the flows or subflows.

-   **[Order management](https://www.servicenow.com/docs/access?context=explore-order-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Order and fulfillment agents can use ServiceNow® Order Management to fulfill customer orders created from the Sales Agreement Management application.

-   **[Install base management](https://www.servicenow.com/docs/access?context=install-base-item&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    ServiceNow® Install Base Management is used to capture a customer’s use or purchase of a product across any industry with the Customer Service Management application.

-   **[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    ServiceNow® Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    ServiceNow® Product Catalog Management organizes products into catalogs and categories so agents can easily find and add products and services to a quote.

-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    ServiceNow® Pricing Management helps you set pricing for products and services that can be added to a quote. Pricing Management also enables agents to make pricing adjustments to products in the quote.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service-specific implementations that provide tools to tier 1 agents used to respond to customers and resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

