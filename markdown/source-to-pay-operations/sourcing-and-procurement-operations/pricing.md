---
title: Pricing
description: Pricing stores the relationship between supplier product, contracts, and price of a product.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Pricing

Pricing stores the relationship between supplier product, contracts, and price of a product.

You can store pricing as a single price or with a price break. Supplier quotes are stored in the Pricing table and are used to display in Shopping Hub to help with the decision of awarding a supplier.

A pricing record is created when the **Negotiated unit cost** field is populated on the purchase line within a sourcing request.

Several scenarios are documented here for clarity.

-   One-time single price, no negotiations:
    -   Sourcing request is automatically created.
    -   Procurement specialist directly enters price into the **Negotiated unit cost** field on the purchase line.
    -   Pricing record is automatically created when the **Negotiated unit cost** field is populated. Price value on the Pricing table is populated with the negotiated unit cost.
    -   The state changes based on the existence of a price value in the Pricing table.
-   One-time single price, with negotiations:
    -   Sourcing request is automatically created.
    -   Procurement specialist creates a negotiation.
    -   Pricing record is automatically created when the negotiation is created, with no price value.
    -   Procurement specialist directly enters price into the **Negotiated unit cost** field on the purchase line.
    -   Price value on the Pricing table is populated with the negotiated unit cost.
    -   The state changes based on the existence of a price value in the Pricing table.
    -   Systematic contract creation on negotiation remains as-is and is linked to the pricing record.
-   One-time price break, no negotiations:
    -   Similar to the one-time single price, no negotiations scenario.
    -   Procurement specialist confirms the quantity with the shopper, if not indicated by the shopper already, and enters the appropriate negotiated unit cost on the purchase line.

        **Note:** When quantity is revised on a line that has an underlying price break, the negotiated unit cost on the purchase line and purchase order line must be updated to reflect the corresponding pricing for that quantity tier.

    -   Pricing record is systematically created for a single price.
    -   Creating a price break entry in the Pricing table is optional.
    -   User manually changes the price type from single price to price break in the Pricing table, and enters the pricing tiers.
-   One-time price break, with negotiations:
    -   Similar to the one-time single price, with negotiations scenario.
    -   Procurement specialist confirms the quantity with the shopper, if not indicated by the shopper already, and enters the appropriate negotiated unit cost on the purchase line.

        **Note:** When quantity is revised on a line that has an underlying price break, the negotiated unit cost on the purchase line and purchase order line must be updated to reflect the corresponding pricing for that quantity tier.

    -   Pricing record is systematically created for a single price.
    -   Creating a price break entry in the Pricing table is optional.
    -   User manually changes the price type from single price to price break in the Pricing table, and enters the pricing tiers.
-   Term single price, no negotiations: Similar to the one-time single price, no negotiations scenario.
-   Term single price, with negotiations: Similar to the one-time single price, with negotiations scenario.
-   Term price break, no negotiations: Similar to the one-time price break, no negotiations scenario.
-   Term price break, with negotiations: Similar to the one-time price break, with negotiations scenario.

**Note:** For third party sourcing integration, the flow does not get impacted since both the **Negotiated unit cost** field and the Pricing table are populated systematically.

The **Original unit cost** field in the Pricing table populates the **Starting unit cost** field on a purchase line for any subsequent purchases using this active contractual price record.

## Contractual Price

A price for a supplier product is considered as an active contractual price when there is a contract reference to the pricing and the contract is active. Subsequent purchases of a product with contractual pricing uses the active contractual price, and the price is displayed in Shopping Hub accordingly.

The **Price Duration Type** field determines if the price is for a one-time purchase or a term purchase. This is a read-only field, whose values are populated based on the **One-time pricing** field on the purchase line.

**Note:** For a good, the value of this field on the Pricing table is always Term. This field is editable within the purchase line only when it is for a service, and the line is within the context of a sourcing request. Once a purchase requisition is created, the field becomes read-only. Any updates made to this field value on the purchase line is reflected accordingly on the Pricing table.

If there are multiple overlapping active contracts for a specific supplier product, and they are mapped to the same or different contract models, the contract with the lowest price is used to display pricing in Shopping Hub.

If there are overlapping active contracts in a blanket or release scenario, any subsequent release uses the lower price. For blanket purchase orders \(not releases\), the original contract associated to the blanket purchase order is not updated. The blanket line amount and quantity remain the same. Releases \(after the lower contractual price is active\) are associated to the contract with the lower contractual price. Contract association for releases that are complete shouldn't be changed.

If the overlapping contracts have a price break structure, use the minimum price to determine which contract to use during the overlapping period.

A reference to the pricing record is added on the purchase line to allow procurement specialists to select a different pricing record, if required. If the pricing reference is updated, the starting unit cost and negotiated unit cost are updated on the purchase line, and so is the requisition to contract association.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

