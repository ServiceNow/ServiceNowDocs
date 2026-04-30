---
title: Quote Management release notes
description: The ServiceNow Quote Management application enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Quote Management release notes

The ServiceNow® Quote Management application enables your sales agents to generate and manage sales quotes for your customers. Quote Management was enhanced and updated in the Zurich release.

## Quote Management highlights for the Zurich release

-   Support quote header discounts​.
-   View the cost and profit of the entire quote to support informed discounting decisions and avoid unprofitable deals.

See [Quote Management](https://www.servicenow.com/docs/access?context=quote-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** Quote Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   ****

    Enables sales agents to quickly view, add, and edit manual price adjustments for quote line items directly from the list view, making it easier to manage both automatic and manual adjustments. The new experience streamlines the quoting process and allows adjustments to be applied to individual or multiple line items at once.


-   **[Price and quantity ramps on quote line items](../../product/tmt-order-mgt/task/add-price-ramps-on-a-quote-line-item.md)**

    Create price and quantity ramps for product offerings in quotes to define incremental price and quantity changes over time. Product offerings eligible for ramps have the Ramps enabled option and Recurring price method selected. Agents can define ramps in two ways:

    1.  Ramp the parent line item, which automatically applies ramps to all child line items.
    2.  Leave the parent unramped, allowing child product offerings to have ramps defined individually.

        Agents can also make manual price adjustments per segment. When a quote with ramps is converted to an order, ramps become read-only.


-   **[Quote header discount](https://www.servicenow.com/docs/access?context=add-header-discount-to-a-quote&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Added a quote header discount feature that enables sales agents to apply a discount across multiple quote lines at once. This simplifies the quoting process and ensures consistent discount application, thereby improving overall sales efficiency and customer satisfaction.


-   **[Subscription revenue metrics](https://www.servicenow.com/docs/access?context=som-subscription-pricing&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Provides sales agents better visibility of the entire quote cost and profit with the addition of Cost and Margin calculations to the following levels:

    -   **Quote Header**: Total one-time cost, Total monthly cost, Total cost, Total one-time margin, Total monthly margin, Total margin amount, Total one-time margin %, Total monthly margin %, and Total margin %.
    -   **Quote Line**: One-time cost, Monthly recurring cost, Cumulative one-time cost, Cumulative monthly cost, Cumulative margin %, and Cumulative Net Cost.
    The automated calculation rules introduced at Quote Header and Quote Line levels enable informed discounting decisions and help prevent unprofitable deals.


## Activation information

Install Quote Management by requesting it from the ServiceNow Store.

To add Docusign plugin to the Quote Management PDF document function, use the Docusign eSignature Spoke plugin \(sn\_docusign\_spoke\).

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

