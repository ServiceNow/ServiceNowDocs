---
title: Subscription-based costs for AI vendors
description: Use the Subscription cost type in AI Control Tower to track vendor costs billed per licensed seat under a fixed-term contract rather than by token or usage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/mc-subscription-based-cost-for-ai-vendors.html
release: zurich
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 3
keywords: [subscription, seat-based pricing, AI cost, AI Control Tower, amortization]
breadcrumb: [Cost, Explore, Measure AI system, Measure AI systems, AI Control Tower, Enable AI experiences]
---

# Subscription-based costs for AI vendors

Use the **Subscription** cost type in AI Control Tower to track vendor costs billed per licensed seat under a fixed-term contract rather than by token or usage.

## Subscription-based cost overview

Subscription-based cost, also called seat-based pricing, is a cost type for AI vendors that bill through a contract with a fixed monthly price per licensed seat. It's available alongside the existing overall cost and input and output cost options.

In a seat-based contract, you purchase a specified number of seats at a fixed price per seat for a defined contract period. Because the contract does not limit token consumption, the subscription cost calculated by AI Control Tower remains the same regardless of token usage.

## Benefits

Token-based cost types don't reflect the actual spend for vendors that bill by seat. With the Subscription cost type, you enter the contract value once, and AI Control Tower applies the resulting monthly cost to each month of the contract period. The cost and value figures on your dashboards then match what your organization pays the vendor.

## When to configure subscription costs

The **Subscription** cost type is available when you add vendor costs during the cost configuration steps of AI Control Tower onboarding, also called the day zero experience. Configure subscription costs during onboarding, when you set up the rest of your AI cost configuration.

You can update a subscription cost at any time after onboarding. Updates apply only from the next day onward. You can't change cost data for today or earlier dates. For details, see [Cost updates and calculation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-cost-updates-and-calculation-schedule.md).

## Subscription cost components

A subscription cost consists of the following parts:

-   **Licensed seats and cost per seat**

    The number of seats in the contract and the price for each seat per month. Both values are required.

-   **Contract period**

    The contract start and end dates. AI Control Tower applies the monthly cost to each month from the contract start date until the contract end date. Both dates are required.

-   **One-time setup fee \(optional\)**

    A flat fee that some vendors charge for eligibility for seat-based pricing or discounted seat-based pricing. Organizations refer to this fee by different names, such as base license fee or one-time setup fee. For example, a vendor might require you to buy another subscription before it offers a discounted per-seat price.

-   **Amortization period**

    The number of months over which AI Control Tower spreads the one-time setup fee. The amortization period is populated by default from the contract start and end dates. You can override the default value.


## Monthly cost calculation

AI Control Tower calculates subscription costs monthly. The estimated monthly cost is the licensed seat cost plus the amortized setup fee, if configured:

```
Estimated monthly cost = (licensed seats × monthly cost per seat) + (one-time setup fee ÷ amortization period)
```

## Example calculation

A contract includes 1,000 licensed seats at $25 per seat each month and a $20,000 one-time setup fee amortized over 14 months:

-   Monthly seat cost: 1,000 × $25 = $25,000
-   Monthly amortized setup fee: $20,000 ÷ 14 = $1,428.57
-   Estimated monthly cost: $25,000 + $1,428.57 = $26,428.57

**Related topics**  


[Cost updates and calculation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-cost-updates-and-calculation-schedule.md)

[Cost configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/mc-cost-configurations.md)

