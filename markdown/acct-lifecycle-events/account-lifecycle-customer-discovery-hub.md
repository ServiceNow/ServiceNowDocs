---
title: Customer Discovery Hub
description: Use the Customer Discovery Hub to capture customer business context during pre-sales and carry that context forward to customer success teams at the post-sale handoff.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-customer-discovery-hub.html
release: australia
topic_type: concept
last_updated: "2026-06-28"
reading_time_minutes: 3
breadcrumb: [Customer success, Explore, Customer Success Management]
---

# Customer Discovery Hub

Use the Customer Discovery Hub to capture customer business context during pre-sales and carry that context forward to customer success teams at the post-sale handoff.

**Note:** This feature is available only if the Customer Discovery Hub \(com.sn\_cust\_disc\_hb\) plugin is installed.

When a deal closes, customer success managers \(CSMs\) receive an engagement record with product information but no insight into why the customer purchased, what problems they face, or what success looks like to them. Context about customer needs, challenges, and expectations is typically scattered across work notes, opportunity records, and documents with no structured path to the post-sale team.

Customer Discovery Hub provides a structured set of records for capturing business needs, challenges, and expectations during pre-sales. Those records transfer automatically to the engagement record, giving customer success managers immediate access to the full customer context.

## Key concepts

Customer context in Customer Discovery Hub is structured into four related objects.

-   Customer business need: The strategic problem a customer must solve. A business need is the core reason a customer purchases or uses a product. It can exist independently or be supported by one or more customer business challenges. Business needs are captured in both pre-sales and post-sales contexts.
-   Customer business challenge: A specific pain point, gap, or enhancement request that surfaces a business need. A challenge describes a symptom or frustration the customer experiences. When qualified, a challenge is linked to a parent business need. A challenge requires a parent business need to be actionable.
-   Customer business expectation: A measurable success outcome tied to a specific business need. Expectations define what success looks like for the customer, including target values, success criteria, and target dates. Each expectation is a child record of a business need.
-   Customer use case: A scenario-level description of how a product addresses a business need. Customer use cases document the customer's current process flow and their alignment to supported use cases — default, extended, or custom. Each customer use case is linked to a parent business need. The alignment value defines the relationship between the customer use case and the product's supported use cases and capabilities.

## Pre-sales to post-sales flow

Customer Discovery Hub is used by pre-sales personas \(account executives, solution consultants\) and post-sales personas \(customer success agents\). During pre-sales, account executives and solution consultants create customer business needs and challenges against lead or opportunity records. They document customer use cases to describe the customer's current process. When a deal closes and an engagement is created, the business needs, challenges, expectations, and use cases linked to the opportunity carry forward to the engagement record. The customer success manager can then continue capturing new business needs and challenges directly against the engagement throughout the customer lifecycle.

**Note:** Customer Discovery Hub does not include automated flows. The tables and forms are available for manual data entry and are accessible as related list items from the engagement record.

To view the Customer Discovery Hub tables, navigate to **All** &gt; **CSM/FSM Configurable Workspace**, open an engagement, and select the **Related Items** related list.

\[Omitted image "cust-discovery-hub.png"\] Alt text: Customer discovery hub related items

Expand the table you want to review and select the Number or Account link to view the record page.

\[Omitted image "cust-discovery-hub-bn.png"\] Alt text: Customer discovery hub: business needs

## Product Capability Core integration

Customer Discovery Hub requires the Product Capability Core plugin. Customer use cases can be aligned with supported use cases from the product catalog.

When you create a customer use case, you specify an alignment value: default, extended, or custom. For default and extended alignments, link at least one supported use case from the product catalog to the customer use case.

For more information, see [Product use case catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-product-use-case.md).

**Related topics**  


[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

[Manage engagements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-manage-engage.md)

