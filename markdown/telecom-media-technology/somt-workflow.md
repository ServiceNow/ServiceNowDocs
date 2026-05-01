---
title: Sales CRM for Telecommunications workflow
description: The Sales CRM for Telecommunications workflow shows the end-to-end process for managing sales orders, from initial prospect identification through order closure.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 5
breadcrumb: [Explore, Sales CRM for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Sales CRM for Telecommunications workflow

The Sales CRM for Telecommunications workflow shows the end-to-end process for managing sales orders, from initial prospect identification through order closure.

![Sales and Order Management for Telecommunications workflow](../image/somt-flow.jpg)

## Sales CRM for Telecommunications lifecycle stages

This diagram showcases the following key stages in the lifecycle including lead qualification, contract creation, order processing, and fulfillment activities:

1.  **Prospect identification - Lead qualification**: This is the initial stage where potential customers are identified and qualified as leads. At this stage, account information isn’t mandatory, allowing sales teams to capture leads without requiring complete customer details. The product catalog is optional at this point, though lead line items can reference catalog items to provide early product visibility and aid in qualification efforts.
2.  **Pre-order qualification**: The lead is converted to an opportunity, establishing a formal sales pursuit linked to a specific customer. An opportunity record is created with product line items tailored to the customer's needs and context. At this stage, the opportunity must be linked to a customer account. The product catalog remains optional but, when used, enables reference to specific catalog items and preliminary pricing estimates. This establishes the product configuration framework that supports detailed pricing and configuration in later stages.
3.  **Create sales agreement / Configure, price, and quote**: This stage represents a critical juncture where two parallel paths work through a bidirectional relationship, allowing continuous interaction and alignment between commercial terms and detailed pricing. The bidirectional arrows between these two paths indicate continuous interaction, allowing updates to commercial terms in the agreement to flow to pricing in the quote, and vice versa.
    -   **Configure, price, and quote**: Handles the detailed commercial configuration, pricing, and feasibility validation to ensure the proposed solution can be delivered. Feasibility results determine offer eligibility, compatibility, and pricing. The account is mandatory with a complete structure and hierarchy, and location information for all accounts must be provided. Site-level product configuration occurs at each child account, and global SLAs from the sales agreement apply automatically. The offer is configured with confirmed pricing, and approvals or repricing activities are completed. Quote versions accommodate iterative refinement. Quote confirmation produces a summary document and requires legal signature before proceeding to contract creation.
    -   **Create sales agreement**: Establishes the commercial framework and negotiates terms and conditions that govern all subsequent quotes and the entire customer relationship. Agreement is the reference for future quotes. Customer account is mandatory at the legal level, product catalog is also mandatory. Global level service-agnostic SLAs are negotiated that cascade to all service contracts. Terms and conditions for partner services are also negotiated at this level.

        **Note:** This is applicable if an existing customer wants to create a new quote. In this case, the existing contract is used as a reference and a quote is immediately generated.

4.  **Contract managementCreate sales contract**: Contracts can be sales contract or service contracts.
    -   Sales contract: Following quote confirmation, the sales contract represents the legally binding commercial agreement between a customer and service provider. Quote confirmation is mandatory before proceeding, and accounts with contacts at the child level must be established. The sales contract directly reflects quote line items, capturing the confirmed commercial configuration, pricing, and terms.
    -   Service contract: Represents a post-confirmation contractual agreement that handles non-commercial configuration with entitlements and service level commitments. Entitlements are mandatory, modeled as Product Offering \(PO\) types, and must follow the global SLAs established in the sales agreement. Service contracts are created at the child account or site level based on specific quote Line Item configurations including routing type, access type, and POP redundancy requirements.
5.  **Order submission**: The order consolidates all commercial and non-commercial configurations into a validated, ready-to-fulfill package. Account information including billing profile is mandatory. Order header and line items directly reflect the quote, maintaining traceability. Commercial modifications require reopening the quote, while non-commercial modifications occur directly in the order. The order is validated before approval.
6.  **Order approval**: Upon submission, the order undergoes financial and operational validation before fulfillment begins. Product inventory is created but remains inactive, awaiting successful completion before activation. This ensures inventory records exist but don't affect availability until services are confirmed as deliverable.
7.  **Order decomposition**: Order decomposition breaks down the order into executable components for orchestrated fulfillment. Order line items are created for product offerings and product specifications. Domain orders are created for each product specification to enable domain-specific orchestration. Order decomposition generates child orders for order line items and domain orders, creating a hierarchical structure that supports both parallel and sequential fulfillment.
8.  **Instantiate sub flows and tasks:** Sub flows are instantiated for every domain order, creating work streams for fulfillment. Tasks are triggered based on flow and decomposition rules. Tasks may be manual, API-driven, Field Service Management for Telecommunications \(FSMT\) for on-site work, or Strategic Portfolio Management for Telecommunications \(SPMT\) for complex projects. Processing occurs in parallel with dependencies for proper sequencing, or staggered to optimize resources.

    The workflow branches into two parallel paths for specialized handling of complex scenarios and exceptions.

    -   **Instantiate special project**: This path provides specialized handling for orders requiring project management discipline. A project is created with tasks designed for complex fulfillment scenarios, such as large enterprise deployments, multi-site installations, or any orders that require coordinated planning, resource management, and formal project tracking.
    -   **Fall out management**: This path handles exception management and resolution. When orders encounter issues, errors, or require special intervention, this path ensures proper tracking, escalation, and resolution without blocking the main fulfillment flow. Problematic orders are managed separately while successful orders continue processing normally.
9.  **Order closure**: The final stage consolidates fulfillment by progressively closing tasks at each level, from sub flows to domain orders to the complete order. Once all tasks are complete, the order closes and services are activated. Integration with the Configuration Management Database \(CMDB\) is established, enabling lifecycle management including monitoring, change control, and incident management.

The Sales CRM for Telecommunications workflow, upon completion, results in activated services ready for customer use, a fulfilled order completing the transaction, CMDB integration for lifecycle management and monitoring, service contracts with defined entitlements, a complete audit trail ensuring compliance, and integrated systems providing end-to-end visibility.

