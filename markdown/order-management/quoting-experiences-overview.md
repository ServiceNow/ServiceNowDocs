---
title: ServiceNow Quote Experience
description: CPQ provides a unified Quote Experience for creating, pricing, approving, and completing quotes. An integrated pricing service prices quotes manually or automatically, and consistent workflows and governance apply wherever your sales teams operate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quoting-experiences-overview.html
release: australia
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 2
breadcrumb: [Configure, price, quote apps, Explore, Sales Customer Relationship Management]
---

# ServiceNow Quote Experience

CPQ provides a unified Quote Experience for creating, pricing, approving, and completing quotes. An integrated pricing service prices quotes manually or automatically, and consistent workflows and governance apply wherever your sales teams operate.

## Quote Experience

The Quote Experience is a single, modern quoting solution that supports both simple and complex quoting needs. It provides a configurable workspace for managing quotes, including products, pricing, approvals, and lifecycle progression.

Key capabilities include:

-   Create and manage quotes directly from your CRM opportunity workflow.
-   Add products using the product configurator.
-   Apply flexible pricing, including discounts, markups, and overrides.
-   Reprice quotes manually or automatically through an integrated pricing service.
-   Route quotes through configurable approval workflows.
-   Track the quote lifecycle from creation through completion.
-   Generate customer-ready quote documents.

## Composable architecture

The Quote Experience is modular and can be embedded into your existing CRM or customer experience platform without requiring a full reimplementation. This flexibility enables you to:

-   Use the quote experience within ServiceNow Sales CRM or another CRM.
-   Embed the quote experience in partner portals or custom sales applications.
-   Integrate with external pricing, order management, and document systems.

## Configuration experience

The product configurator lets users select and configure products directly within the Quote Experience. It supports complex product structures, dependencies, and pricing inputs while remaining embedded in the quoting workflow.

## Implementation considerations

CPQ supports a range of deployment models and regulatory requirements:

-   Deploy cloud-first implementations for modern, composable quoting experiences.
-   Support tailored implementations for on-premises or federally regulated environments.
-   Configure the solution to align with organizational controls, compliance requirements, and integration constraints.

## Pricing and repricing

The Quote Experience prices quotes through an integrated pricing service. When pricing is enabled for a deployment, quote and line pricing fields are populated automatically, and the quote can be repriced on demand or in response to changes.

-   **Manual and automatic repricing**

    Reprice a quote explicitly with the **Reprice** action, or let repricing run automatically when a pricing-affecting change occurs, such as adding or reconfiguring a product.

-   **Pricing state**

    Each quote and line tracks whether its pricing is current. When a pricing-affecting field changes, the quote or line is marked as needing a reprice until a successful pricing call completes.

-   **Manual and automatic adjustments**

    Sales representatives can apply manual discounts, markdowns, or price overrides, and the pricing service can apply rule-driven adjustments such as volume tiers and promotions. A manual adjustment takes precedence over an automatic adjustment on the same line or header.


For a conceptual overview of how the pricing service integrates with the Quote Experience, including pricing states and repricing, see [Pricing in the ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/pricing-in-quote-experience.md). Administrators configure the pricing connection and repricing behavior as part of setting up the quoting experience. For more information, see [Configuring ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-crm-tm-quoting-configure.md).

## Supported use cases for the CPQ

Use the Quote Experience when you need a scalable, configurable quote solution that:

-   Supports both simple and complex sales processes
-   Integrates with your existing systems
-   Provides consistent governance across the quote lifecycle

**Related topics**  


[Configuring ServiceNow Quote Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-crm-tm-quoting-configure.md)

