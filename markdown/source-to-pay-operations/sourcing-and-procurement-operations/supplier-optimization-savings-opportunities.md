---
title: Supplier optimization savings opportunities
description: The Supplier Optimization Opportunity Finder Agent identifies spend placed with non-preferred suppliers and fragmented across multiple suppliers for similar products. Addressing these opportunities helps redirect spend to preferred sources and consolidate supplier relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/supplier-optimization-savings-opportunities.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-05-15"
reading_time_minutes: 3
keywords: [supplier optimization, non-preferred supplier, spend fragmentation, supplier consolidation, savings opportunity]
breadcrumb: [Savings opportunities, Spend and Savings Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Supplier optimization savings opportunities

The Supplier Optimization Opportunity Finder Agent identifies spend placed with non-preferred suppliers and fragmented across multiple suppliers for similar products. Addressing these opportunities helps redirect spend to preferred sources and consolidate supplier relationships.

The Supplier Optimization Opportunity Finder Agent analyzes supplier spend patterns to detect two types of savings opportunity: spend placed with non-preferred suppliers when a preferred alternative exists, and spend fragmented across multiple suppliers for similar products within the same spend category. Both levers use product similarity matching to identify consolidation opportunities.

## Non-preferred supplier spend opportunities

A non-preferred supplier is a supplier that has not been designated as preferred for its spend category. Spend placed with non-preferred suppliers can reduce negotiated savings and weaken supplier governance. The agent identifies cases where the same or a closely related product is being purchased from a non-preferred supplier when a preferred alternative exists.

The agent processes purchase order lines where the supplier is not marked as preferred for the relevant spend category. The agent groups activity by supplier, spend category, and product, then attempts to match each non-preferred grouping to a preferred supplier that offers the same or a closely related product. Product similarity is determined by comparing product attributes and descriptions, including both direct matches and semantically related items in the same spend category.

To avoid reprocessing every purchase order on each run, the agent tracks the date of the last run and processes only purchase order lines updated after that date. Deduplication based on spend category, supplier, and savings lever prevents the agent from generating a duplicate opportunity for the same finding on subsequent runs.

A non-preferred supplier opportunity captures the following information:

-   The non-preferred supplier and the spend category where the activity was detected.
-   The identified preferred supplier for the same or related products.
-   The purchase order lines that contributed to the finding.
-   The estimated savings from redirecting future purchases to the preferred supplier.

## Spend fragmentation opportunities

Spend fragmentation occurs when an organization buys similar products or services from multiple suppliers within the same spend category. The agent detects these patterns and identifies opportunities to consolidate purchases to fewer suppliers to negotiate better pricing and reduce supplier management overhead.

The agent groups historical spend by spend category and checks for cases where similar goods or services are being purchased from multiple suppliers in the same category. Product similarity is determined by comparing product attributes and descriptions. For each fragmented group, the agent calculates the potential savings if the spend is consolidated under the supplier offering the most favorable terms in the category.

The agent applies deduplication so that repeated weekly runs do not create a separate opportunity for the same fragmentation pattern. If new purchase activity changes the savings estimate, the existing open opportunity is updated rather than duplicated.

A spend fragmentation opportunity captures the following information:

-   The spend category and the suppliers identified in the fragmented spend pattern.
-   The amount of spend distributed across the multiple suppliers.
-   The estimated savings from consolidating spend to the identified supplier.
-   The currency used in the calculation, which reflects the session currency at the time the agent runs, with USD used when no session currency is available.

When you create a pipeline project from a spend fragmentation opportunity, the linked suppliers are attached to the project so that the sourcing team can reference the source evidence during supplier consolidation discussions.

**Parent Topic:**[Savings opportunity identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-identification.md)

