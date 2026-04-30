---
title: Customer Contracts and Entitlements release notes
description: The ServiceNow Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Customer Contracts and Entitlements release notes

The ServiceNow® Customer Contracts and Entitlements application provides the foundation for storing and managing customer service contracts and entitlements. Customer Contracts and Entitlements was enhanced and updated in the Yokohama release.

## Customer Contracts and Entitlements highlights for the Yokohama release

-   Enable customers to create contracts from product inventory.
-   Added a new workspace view for service contracts and entitlements in Customer Service Management workspace for efficiently managing service contracts and entitlements.
-   Enable initiation of contract renewal automatically based on the configured date and pricing details.
-   Calculate the price of future renewals of contracts with a markup or mark down percentage of the current contract price.
-   Validate the contract end date to the product offering end date.

See [Customer Contracts and Entitlements](https://www.servicenow.com/docs/access?context=exploring-post-sales-support&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

**Important:** Customer Contracts and Entitlements is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Create contracts from product inventory](https://www.servicenow.com/docs/access?context=create-cont-ent-workflows-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables customer to create and manage contracts for product inventory records.


-   **[New workspace view for service contracts and entitlements](https://www.servicenow.com/docs/access?context=components-installed-pss&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    A new workspace view named Service Contract Workspace has been added for customers on service contracts and entitlements in the Customer Service Management workspace. This view is set as the default view and can be changed by an administrator.


-   **[Enhancement on contract lines and entitlements](https://www.servicenow.com/docs/access?context=using-post-sales-support&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    View location and subscription pricing information on contract lines and entitlements.


-   **[Automatic renewal of contracts](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables customers to configure the date and pricing details of contract renewal while creating initial contracts.


-   **[Enable renewal opportunity creation](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Create an opportunity or an opportunity and quote when you renew service contracts and service contract lines.


-   **[Co-terminating of Contract lines](https://www.servicenow.com/docs/access?context=using-customer-cnt-ent-wf&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables customers to assign same start and end date to multiple quote lines.


-   **[End-of-life check​](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Alert customers when the contract end date is exceeding the product offering end date during quote processing. Customers can then match the contract and product offering end date if required.


-   **[Renewal Uplift feature](https://www.servicenow.com/docs/access?context=cce-renew-service-contract&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Enables customers to set the pricing parameters of future renewals of contracts. You can select the markup or mark down percentage of the current contract price or you can apply the market price of the contract at the time of renewal.


## Activation information

Install Customer Contracts and Entitlements by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Customer Contracts and Entitlements is available with activation of the Customer Contracts and Entitlements \(com.sn\_pss\_core\) plugin, which requires a separate subscription. For details, see [Configure Customer Contracts and Entitlements](https://www.servicenow.com/docs/access?context=configuring-post-sales-support&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

**Note:** With the activation of Customer Contracts and Entitlements, new contracts and entitlements are created using the new data model only. The new entitlement verification APIs and change workflows are based on the new data model. Older contracts and entitlements can still be viewed but not modified.

## Related ServiceNow applications and features

-   **[Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer-components&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    ServiceNow® Workflow Studio components enable you to invoke flows or subflows that are designed as part of a workflow and used to find out the output or execution status of the flows or subflows.

-   **[Order Management](https://www.servicenow.com/docs/access?context=order-mgt-exploring&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Order and fulfillment agents can use ServiceNow® Order Management to fulfill customer orders created from the Sales Agreement Management application.

-   **[Install base management](https://www.servicenow.com/docs/access?context=install-base-item&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    ServiceNow® Install Base Management is used to capture a customer’s use or purchase of a product across any industry with the Customer Service Management application.

-   **[Next Experience UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    ServiceNow® Next Experience UI Builder is a low-code web user interface builder that enables developers to build pages for workspace and portal web-based experiences. Use the base system and custom web components to build your pages.

-   **[Product Catalog Management](https://www.servicenow.com/docs/access?context=product-catalog-managment&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    ServiceNow® Product Catalog Management organizes products into catalogs and categories so that agents can easily find and add products and services to a quote.

-   **[Pricing Management](https://www.servicenow.com/docs/access?context=pricing-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    ServiceNow® Pricing Management helps you set pricing for products and services that can be added to a quote. Pricing Management also enables agents to make pricing adjustments to products in the quote.

-   **[Workspace](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues. CSM Configurable Workspace and CSM Agent Workspace are customer service-specific implementations that provide tools to the tier 1 agents that they must use to respond to customers and resolve cases.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

