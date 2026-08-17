---
title: Quote Management release notes
description: The ServiceNow Quote Management application enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Quote Management release notes

The ServiceNow® Quote Management application enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Yokohama release.

## Quote Management highlights for the Yokohama release

-   Enable agents to manage sales agreements in quotes.
-   Enable agents to view the price adjustments that are applied to the base and list price of a product in a quote.
-   Enable agents to create PDF documents from a quote using the ServiceNow PDF generator.
-   Use the hierarchical list view to view parent and child relationships within quote lines.
-   Provide agents with offer recommendations to upsell or cross-sell products that complement products in quotes.

See [Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/quote-management.md) for more information.

## New in the Yokohama release

-   **[Apply a sales agreement to a quote in Quote Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/quote-add-sales-agreement-quotes.md)**

    Create a new sales agreement or apply an existing sales agreements to a quote. When a sales agreement is enabled in a quote, the products and services added to the quote are also added to a sales agreement. When an existing sales agreement is added to a new quote, the catalog is filtered to show the products and options from the sales agreement, the price list is set to the agreement price list, and the sales agreement line is referenced on quote line.

-   **[View price adjustment details for a quote line item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/view-price-adjustment-details-for-quote-lines.md)**

    Agents gain visibility into the price adjustments that were applied to the base and list price of the product ordered. This provides sales agent the visibility of how the net price is determined.


-   **[Quote PDF documents generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/quote-create-pdf-document.md)**

    Generate a quote PDF document. Quote PDF documents can have designated signers and be emailed to customers for signatures through Docusign. Customers can also create PDF templates that reflect customer branding and logos.


-   **[Hierarchical quote line list view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/quote-management-view-hierarchical-line-items.md)**

    View quote lines as a hierarchical list. Agents can then view parent and child relationships for quote line items.


-   **[Product offer recommendations for quotes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/quote-get-product-offer.md)**

    Enable your agents to get product offer recommendations that complement or supplement existing products within a quote.


## Deprecations

The Subscription start date and Subscription end date have been deprecated starting with the Q2 2024 release. Use the Contract start date and Contract end date to calculate Terms for setting subscriptions for recurring products.

## Activation information

Install Quote Management by requesting it from the ServiceNow Store.

To add Docusign plugin to the Quote Management PDF document function, use the Docusign eSignature Spoke plugin \(sn\_docusign\_spoke\).

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    The Sales Agreement Management application uses the Customer Service Management account, consumer, and product inventory data model. Customer service agents have full visibility into quotes created using Quote Management.

-   **[Opportunity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/opportunity-management.md)**

    The Opportunity Management application provides your sales agents and account executives with product recommendations for customers based on a needs analysis. You can seamlessly convert sales opportunities to quotes when the customer is ready.

-   **[Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/product-catalog-managment.md)**

    The Product Catalog Management feature in Sales Customer Relationship Management enables your catalog administrators to create product catalogs with pricing that enable agents to find and add products and services to sales quotes.

-   **[Pricing Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/pricing-management.md)**

    The Pricing Management feature in Sales Customer Relationship Management enables your pricing administrators to set pricing for products and services that are used in quotes. Pricing administrators also set the controls that enable your sales agents to adjust pricing for complex product offers in quotes.

-   **[Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/order-mgt-exploring.md)**

    Order and fulfillment agents can use Order Management to fulfill customer orders created from the Sales Agreement Management application.


**Parent Topic:**[Sales Customer Relationship Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/sales-order-management-rn-landing.md)

