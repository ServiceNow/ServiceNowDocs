---
title: Spend optimization savings opportunities
description: Spend Optimization Opportunity Finder Agent identifies opportunities where purchase activity is outside negotiated contracts or fragmented across multiple contracts. Addressing these opportunities helps redirect spend to contracted pricing and increase purchasing volume for negotiation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spend-optimization-savings-opportunities.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-05-15"
reading_time_minutes: 3
keywords: [spend optimization, off-contract spend, unconsolidated spend, savings opportunity]
breadcrumb: [Savings opportunities, Spend and Savings Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Spend optimization savings opportunities

Spend Optimization Opportunity Finder Agent identifies opportunities where purchase activity is outside negotiated contracts or fragmented across multiple contracts. Addressing these opportunities helps redirect spend to contracted pricing and increase purchasing volume for negotiation.

Spend Optimization Opportunity Finder Agent analyzes purchase order activity from the preceding 12 months to detect patterns where spend is either outside contracted sources or spread across multiple contracts for the same supplier and product. The agent supports two savings levers: off-contract spend and unconsolidated spend.

## Off-contract spend opportunities

Off-contract spend refers to purchases made without using a negotiated contract, often at prices higher than the contracted rate. The agent identifies categories and products where off-contract spend exists alongside on-contract spend so that sourcing teams can redirect future purchases to the contracted source.

The agent examines closed-paid and closed-released purchase order lines and determines whether each purchase was on-contract by matching against contract-to-purchase-order relationships and date ranges. The agent groups activity by supplier, spend category, and product, then separates on-contract activity from off-contract activity. For each grouping that contains both, the agent calculates the discount missed by buying off-contract and the potential savings from redirecting that spend to the contracted price.

For services, the agent normalizes the contract value over the duration of the service to derive a daily rate, which is then used when comparing on-contract and off-contract pricing. Rebates are not included in the savings estimate.

An off-contract spend opportunity captures the following information:

-   The supplier and the spend category where off-contract activity was detected.
-   The on-contract and off-contract purchase order lines that contributed to the finding.
-   The estimated savings from moving the off-contract spend to the contracted price.

If a category, supplier, or product has only off-contract activity and no comparable on-contract activity, the agent does not generate an opportunity. A reference price is required to calculate the potential savings.

## Unconsolidated spend opportunities

Unconsolidated spend refers to purchases of the same or similar products or services placed across multiple contracts or business units with the same supplier. When these purchases are aggregated, the resulting volume can support negotiating a lower per-unit price or improved contract terms.

The agent examines purchase order lines from the preceding 12 months and groups activity by supplier, business unit, and product. The agent identifies cases where the same supplier delivers similar products across different contracts at different prices, then compares the actual prices paid against the lowest contracted price for the same or closely related product. The difference represents the potential savings from consolidating future purchases under the lower-priced contract.

An unconsolidated spend opportunity captures the following information:

-   The supplier and the spend categories where the fragmentation was detected.
-   The contracts and purchase order lines that contributed to the finding.
-   The baseline spend and the estimated savings from consolidation.
-   A complexity rating that reflects the number of source records involved.

When you act on an unconsolidated spend opportunity, the linked purchase orders are attached to the draft pipeline project under the Previous purchase orders related list so that sourcing teams can include the source evidence into the next negotiation.

If a grouping does not include enough recent activity, if the products cannot be matched as similar, or if there is no lower-priced contract available for comparison, the agent does not create an opportunity for that grouping. No administrator-configurable spend or volume thresholds apply.

**Parent Topic:**[Savings opportunity identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-identification.md)

