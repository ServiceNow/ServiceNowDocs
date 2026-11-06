---
title: Sales CRM for Telecommunications release notes
description: The ServiceNow Sales Customer Relationship Management application manages the sales and order lifecycle, from product catalog definition through order capture, fulfillment orchestration, and AI-assisted task templating. See the following sections for release notes by version.Extend task plan template orchestration to Sales CRM for Telecommunications customers, and generate templates automatically with an enhanced AI Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/sales-customer-relationship-management-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-28"
reading_time_minutes: 2
keywords: [Task Plan Template, AI Agent, Order Orchestration, Sales and Order Management, Task Plan Template, AI Agent, Order Orchestration, Legal Name, Order Integrator]
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Sales CRM for Telecommunications release notes

The ServiceNow® Sales Customer Relationship Management application manages the sales and order lifecycle, from product catalog definition through order capture, fulfillment orchestration, and AI-assisted task templating. See the following sections for release notes by version.

## About Sales Customer Relationship Management

-   Manage the full sales and order lifecycle, from product catalog and specification management to order capture, fulfillment orchestration, and fallout handling.
-   Generate and reuse catalog-driven task plan templates to orchestrate order fulfillment automatically, without manual task setup on repeat orders.
-   Use AI Agents to convert a fulfilment-journey image or similar past orders into a ready-to-publish orchestration template.

See [Sales Customer Relationship Management for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/sales-crm.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Sales CRM for Telecommunications by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html). For activation details, see [Activate Sales CRM for Telecommunications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/activate-somt.md).


## Accessibility and localization

-   **Accessibility information**

    Sales Customer Relationship Management follows standard ServiceNow platform accessibility support, including keyboard navigation and compatibility with screen readers.

-   **Localization information**

    Sales Customer Relationship Management does not include dedicated language packs. Language support relies on the base system language plugins active on your instance.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/technology-industry-rn-landing.md)

## Version 15.0.4

Extend task plan template orchestration to Sales CRM for Telecommunications customers, and generate templates automatically with an enhanced AI Agent.

### What's new

-   **Task plan templates for Sales Customer Relationship Management \(Sales CRM\)**

    Define and use task plan templates without a Sales Customer Relationship Management for Telecommunications \(SOMT\) license. Define task plan templates, task plan items, and dependencies, and trigger them based on order action \(add, change\) and product type.

-   **[AI Agent for template-driven order orchestration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-task-template-generation-somt.md)**

    Generate reusable orchestration templates with an enhanced conversational AI Agent instead of a flat task list. When no template exists for a product specification, the agent converts an uploaded fulfilment-journey image into a draft template, or proposes one from the closest matching specification's past orders. Product Catalog Managers define dependencies and publish the template, which then automatically orchestrates the current and all future orders for that specification and action.


### What's changed

-   **[Legal name persistence during account creation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/account-details-form-fields.md)**

    Legal name entered during account creation is now correctly persisted. Previously, the value was mapped to a database field that did not exist.

-   **[Order integrator role no longer blocks other roles from creating consumers and locations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/components-installed-with-order-management.md)**

    Fixed an access control issue where the order integrator role's create permissions on Consumer and Location records inadvertently blocked other roles, such as CSM Agent, from creating those records.


