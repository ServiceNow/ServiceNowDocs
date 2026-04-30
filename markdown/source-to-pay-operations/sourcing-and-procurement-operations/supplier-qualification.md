---
title: Supplier qualification
description: As a procurement specialist or Procurement Case Management \(PCM\) agent, you would want to engage with suppliers who are qualified to fulfill your organization's purchasing needs.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Procurement Case Management, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Supplier qualification

As a procurement specialist or Procurement Case Management \(PCM\) agent, you would want to engage with suppliers who are qualified to fulfill your organization's purchasing needs.

The supplier qualification process can be very involved with multiple teams wanting to engage with a supplier on different levels. Based on your process, you can define qualification cases to reflect the work that needs to be done to ready the engagement with a supplier. This is achieved through decision tables for your sourcing and negotiation work streams. For information on the relevant decision tables, see [Purchasing tasks and procurement cases](purchasing-tasks.md).

Qualification cases include:

-   Supplier cases:

    -   Conduct a Supplier Risk Assessment: Conduct a risk assessment for a supplier.
    -   Onboard a Supplier: Onboard a supplier for a purchase.
    -   Conduct a Supplier Tiering Assessment: Conduct a tiering assessment for a supplier.
    **Note:** For these supplier cases, the decision templates are available only when you have the Supplier Lifecycle Operations application installed. You must also enable the Risk Assessments Integration for Sourcing and Procurement Operations application and have the GRC Vendor Risk Management license if you want the Conduct a Supplier Tiering Assessment case to be generated. For information on how a supplier tiering assessment task influences sourcing request states, see [Sourcing and Procurement Operations integration with Third-party Risk Management](../concept/better-together-with-vrm.md).

-   Contract cases​:
    -   Contract Review: Review contracts for a purchase.
    -   Send NDA for Signature: Send an NDA for signature to the supplier for a purchase.
-   Finance cases​:
    -   GL Coding Review: Review accounting details for a purchase line.
    -   Budget Review: Review budget details for a purchase requisition.

For a case to be considered as a qualification case, the **Qualification dependent on case** field in that case template must be set to **Yes**.

To enable you be compliant with fair competition laws, when engaging with multiple suppliers, qualification cases that you’ve defined in the decision tables need to be completed before continuing your sourcing and negotiation work streams. You can define qualification cases to be initiated on a sourcing request, negotiation, or a negotiation event.

To initiate the supplier qualification flow on a sourcing request, select the sourcing request you want to work with from the Source-to-Pay Workspace list page, **All team work** &gt; **Sourcing Requests**, and select **Begin qualification**. This automatically creates the qualification cases that you’ve defined within the decision tables to be associated with this sourcing request, and also moves the sourcing request and its associated purchase lines to the Qualification Needed state. Alternatively, updating the negotiated unit cost on any of the purchase lines within the sourcing request automatically triggers the qualification flow on the sourcing request. Closing the cases moves them to the Qualified state, and readies the sourcing request for awarding.

**Note:** If a sourcing request is raised with qualified suppliers, qualification cases aren't created and the sourcing request is directly moved to the Qualified state.

When working within a negotiation or sourcing event that has an associated sourcing request, the supplier qualification flow is automatically initiated, and qualification cases are created for the negotiation or sourcing event respectively. Closing these cases moves the sourcing event and all its associated sourcing requests, negotiations, and purchase lines to the Qualified state, and readies the sourcing requests for awarding. All state changes are displayed in the activity streams of the respective records. You can use the activity stream to track your negotiations with your suppliers, from start to end.

**Note:** If the qualification event had been started for a sourcing request, and cases had been created on the sourcing request before it was mapped to a negotiation or negotiation event, and there’s an overlap in cases, then previously created cases on the sourcing request are automatically closed and the new cases created for the negotiation or sourcing event are retained.

**Parent Topic:**[Procurement Case Management](../concept/psd-overview.md)

