---
title: Sourcing and Procurement Operations release notes
description: The ServiceNow Sourcing and Procurement Operations application provides your employees with a simple automated tool that they can use to shop for goods and services that they need at work. Sourcing and Procurement Operations was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Sourcing and Procurement Operations release notes

The ServiceNow® Sourcing and Procurement Operations application provides your employees with a simple automated tool that they can use to shop for goods and services that they need at work. Sourcing and Procurement Operations was enhanced and updated in the Zurich release.

## Sourcing and Procurement Operations highlights for the Zurich release

-   Enable shoppers to view and select their local currency throughout the Shopping Hub experience, including supplier cards, product detail pages, cart, checkout, my purchases, and request tracker.
-   Enable procurement admins to configure and render unique question types for quick and full checkout experiences for each product or service line.
-   Use dashboards and tabs in the Source-to-Pay Workspace to view spend, savings, and pipeline projects, identify savings opportunities, and create pipeline projects directly from filtered lists.
-   Enable requesters to submit sourcing requests with multiple products in a single sourcing intake form, automatically generating individual sourcing events for each product.
-   Allow requesters to view and manage third-party RFx tasks in the Employee Center and navigate to the third-party sourcing tool to review, publish, and award RFx.
-   Initiate catalog and off-catalog procurement workflows from the IT Asset Management \(ITAM\) workspace using the ITAM-SPO better together feature.
-   Enable decimal quantities for service items when creating purchase requisitions using quick or full checkouts in Shopping Hub and Employee Center.
-   Enable requesters to accept or reject case resolutions through email or Employee Center before closure, reducing premature case closures.

See [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/psm-overview.md) for more information.

**Important:** Sourcing and Procurement Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Multi-currency support in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sh-multicurrency-overview.md)**

    Enable multi-currency display across approval-related views, including To-Dos, tasks, email notifications, and the Bundles page. Currency values are shown in both the approver’s local currency and the original supplier currency where applicable. The local currency is displayed as the primary value, with the original currency shown as a secondary reference. This display format provides consistent currency visibility for approvers during review.

-   **[Decimal quantity support for service-based purchases in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/decimal-support-services.md)**

    Enable requesters to enter and edit decimal quantities for service-based purchase requisitions and purchase orders without validation errors. Decimal quantities are supported only for services to maintain data integrity. Decimal quantities for goods are not supported and return a clear validation message. This validation logic is consistent across Shopping Hub and Employee Center.

-   **[Automatically assign categories during SR and PR creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/automatically-assign-categories.md)**

    Automatically classify service requests, purchase requisitions, and purchase orders into the correct spend categories using the Spend categorization agent. This classification process reduces manual classification effort and improves consistency across procurement workflows.

-   **[Purchase on behalf of another user in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/purchase-on-behalf-sh.md)**

    Enable users to purchase on behalf of others without requiring delegate configuration in Shopping Hub. Users can manage individuals they are authorized to purchase for, directly within the buying experience. Purchases made on behalf of others are visible through filtering by business owner in the My Purchases view.

-   **[Purchase requisition line-level questions in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/prl-question-shoppinghub.md)**

    Create configurable, line-level questions during checkout in Shopping Hub. These questions are defined in Catalog Builder and are specific to certain products or product categories.

-   **[Multi-currency support in Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/sh-multicurrency-overview.md)**

    View and select your local currency while shopping for products in Shopping Hub to provide a seamless multi-currency experience.

-   **[Category management tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/category-mgmt-tab.md)**

    Access a unified, filter-based view of category performance across spend, savings, pipeline projects, contracts, purchase orders, and suppliers.

-   **[Category analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/spo-category-analytics.md)**

    View savings opportunities across the sourcing pipeline using the Savings dashboard in the Category Analytics module of the Source-to-Pay Workspace.

-   **[Pipeline management tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/pipeline-mgmt-tab.md)**

    Gain insights into savings and pipeline projects to enhance visibility, tracking, and collaboration across teams.

-   **[Report savings when awarding multiple suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/report-savings-multiple-suppliers.md)**

    Enter the spend and savings data for the sourcing event associated with the pipeline project when awarding multiple suppliers.

-   **[Create a pipeline project from an expiring contract](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/create-pipeline-expire-contract.md)**

    Create a pipeline project directly from an expiring contract using a guided, decision-based workflow.

-   **[Submit multi-product sourcing requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/multi-product-sourcing-intake-with-third-party-integration.md)**

    Submit sourcing requests with multiple products in a single sourcing intake form, and the third-party sourcing solution will automatically create separate sourcing events for each product.

-   **[Manage third-party RFx tasks in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/third-party-rfx-task-management-for-requestors.md)**

    View and manage third-party Request for anything \(RFx\) tasks in the Employee Center and navigate to the third-party sourcing tool to review, publish, and award RFx.

-   **[Sourcing and Procurement Operations integration with IT Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/spo-itam-better-together.md)**

    The Asset Management Integration for Sourcing and Procurement Operations plugin \(com.snc.sn\_spend\_asset\) provides an integration between IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\) applications, enhancing operational efficiency. This integration enables asset managers to access catalog items, including those items without assigned prices, directly within the ITAM workspace. By enabling procurement actions without switching platforms, it streamlines workflows and improves the user experience.

-   **[Sourcing Pipeline Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/spo-sourcing-pipeline-mgmt.md)**

    Sourcing Pipeline Management introduces a centralized approach to managing sourcing projects, enabling you to create, track, and manage sourcing activities in one place. It includes workflow automation to reduce manual effort, improves visibility into sourcing activities, and supports tracking and forecasting of cost savings.

-   **[Using Shopping Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/use-shoppinghub-portal.md)**

    Enter decimal quantities when creating purchase requisitions for service items using quick or full checkout flows in Shopping Hub. Edit service acknowledgments with decimal values to enable more precise tracking of service consumption.

-   **[Purchasing tasks and procurement cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/purchasing-tasks.md)**

    Review and respond to proposed case resolutions based on conditions defined in the decision tables before the case is permanently closed. When a fulfiller marks a case as resolved, the system now automatically transitions the case status to Awaiting Acceptance, pausing closure until the requester takes action. Requesters are notified via email with actionable buttons and can also accept or reject the resolution directly through the Employee Center. This notification helps to ensure that unresolved issues are addressed before a case is closed, improving resolution accuracy and customer satisfaction.


## UI change

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Components installed with Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/installed-with-FSC.md)**

    The Negotiation event table label has been renamed to Sourcing event. This change affects the label only. The underlying table name, \[sn\_shop\_negotiation\_event\], remains unchanged.


## Activation information

Install Sourcing and Procurement Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-spo.md)**

    Use the ServiceNow® Now Assist for SPO application to simplify request creation with conversational intake and summarize records to help fulfillers act promptly.

-   **[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/source-to-pay-ws-overview.md)**

    Provide experiences and tools to support key activities, such as procuring goods and services, onboarding high-performing suppliers, and processing invoices.


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/source-to-pay-operations-rn-landing.md)

