---
title: Product use case catalog
description: Define how a product solves a problem by creating use cases in the product use case catalog. Document process flow, ownership, complexity, audience, and industry context, then map use cases to product models.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-product-use-case.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 2
breadcrumb: [Customer success, Explore, Customer Success Management]
---

# Product use case catalog

Define how a product solves a problem by creating use cases in the product use case catalog. Document process flow, ownership, complexity, audience, and industry context, then map use cases to product models.

## Product use case catalog overview

The product use case catalog provides a structured, reusable way to define how a product addresses customer issues. Without a shared use case catalog, each team builds its own records in inconsistent formats, resulting in duplicated data, inconsistent lifecycle management, and no cross-product adoption insight.

The product use case catalog includes a supported use case catalog that product teams maintain. Supported use cases are associated with product models to show which products support each use case. This enables customer success teams to reference the catalog when documenting customer-specific implementations.

**Note:** This feature requires the Product Capability Core plugin \(com.sn\_prod\_cap\_core\). The Supported use case table is available when this plugin is installed.

## How supported use cases work

The Product Use Case catalog contains supported use cases that define the standard ways a product solves customer problems. Customer-facing teams reference these supported use cases when documenting customer use cases in the Customer Discovery Hub. Each customer use case is linked to a business need and aligned to one or more supported use cases using an alignment value: default \(the product's standard approach\), extended \(a supported variation\), or custom \(a customer-specific implementation\).

Use cases are associated with one or more product models, enabling traceability between use cases and product solutions. A use case can be associated with an entire product or with a specific capability within that product. These associations can be edited only while the use case is in **Draft** state.

The Industry and Audience type fields define which customer segments and verticals the use case targets. This helps customer success teams identify the most relevant use cases for a given customer context. Records follow a managed publication lifecycle \(Draft, Published, Retired, or Cancelled\) controlled by UI actions.

## Relationship with Customer Discovery Hub

The Customer Discovery Hub depends on the product use case catalog. When customer success teams create customer use cases, they specify an alignment to supported use cases from this catalog. This alignment determines whether and how many Supported Use Cases must be linked.

For more information on customer use cases and how they align to supported use cases, see [Customer Discovery Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-customer-discovery-hub.md).

**Related topics**  


[Customer Discovery Hub tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-cust-dh-tables.md)

[Supported use case table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-product-uc-tables.md)

