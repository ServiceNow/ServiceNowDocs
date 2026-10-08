---
title: Cost types and sub-vendor rates
description: Record what your organization pays each AI vendor so that AI Control Tower can calculate total Enterprise AI cost and net returns. Choose the cost type that matches each contract, and set sub-vendor rates where a specific service is billed differently from its vendor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mc-ai-cost-types-and-sub-vendor-rates.html
release: brazil
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 3
keywords: [AI cost, sub-vendor, subscription, cost type, AI Control Tower]
breadcrumb: [Cost, Explore, Measure AI system, Measure AI systems, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Cost types and sub-vendor rates

Record what your organization pays each AI vendor so that AI Control Tower can calculate total Enterprise AI cost and net returns. Choose the cost type that matches each contract, and set sub-vendor rates where a specific service is billed differently from its vendor.

AI Control Tower estimates the financial value of your AI assets by comparing total savings with total Enterprise AI cost. Total savings come from productivity gains and the hourly rates that you configure. Total Enterprise AI cost is the sum of integrated vendor costs and other vendor costs. Net returns are total savings minus total Enterprise AI cost.

## Integrated vendors and other vendors

Integrated vendors are vendors that have a trace or SDK integration with AI Control Tower, such as Microsoft, Google Vertex AI, and Amazon Web Services \(AWS\). AI Control Tower gets token consumption metrics for these vendors from the traces.

Other vendors are vendors that don't have a trace or SDK integration with AI Control Tower. Entering costs for these vendors is optional.

## Cost types

The cost type determines which values you enter and how AI Control Tower calculates the cost for a vendor.

|Cost type|Values you enter|
|---------|----------------|
|**Overall cost**|A single cost per million tokens.|
|**Input and output costs**|Separate costs per million input tokens and per million output tokens.|
|**Subscription**|The number of licensed seats, the cost per seat per month, and the contract start and end dates. You can also add a one-time setup fee.|

For other vendors, the Add Vendors menu offers three pricing options:

-   **Token-based**: Costs are calculated based on the total number of tokens used and the cost per token.
-   **Direct Cost**: The total cost is entered directly.
-   **Subscription**: Pricing is determined by a per-seat subscription model.

These options provide flexibility in how costs are determined.

## Sub-vendor rates

A sub-vendor is a specific service that a vendor offers. For example, Microsoft is a vendor, and Azure is one of its sub-vendors. In the cost list, it appears as the vendor name followed by the service name.

A sub-vendor rate takes precedence over its vendor's rate. When a vendor has at least one sub-vendor rate, its entry shows the message **Applies only where no sub-vendor rate is set**. The vendor rate continues to apply to usage that isn't covered by a sub-vendor rate.

## Estimated monthly cost for subscriptions

For a subscription, the **Estimated monthly cost** value is the number of licensed seats multiplied by the cost per seat per month. The value updates as you enter the details.

If you add a one-time setup fee, AI Control Tower spreads the fee evenly over the number of months that you enter in **Amortise over \(months\)**. It adds the resulting monthly amount to the estimated monthly cost. The per-month amount of the fee appears after the field.

## Cost entry status

A cost entry that you add or change has the status **Draft**, and the page shows the message **Changes will apply after you submit in Preview cost &amp; savings**. Draft entries don't affect calculated values until you submit the configuration in the **Preview cost &amp; savings** step. Submitted entries have the status **Active**.

An entry can also have the status **Expired**.

**Related topics**  


[Add costs for integrated vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mc-add-and-configure-costs-for-integrated-vendors.md)

[Add costs for other vendors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mc-add-and-configure-costs-for-non-integrated-vendors.md)

