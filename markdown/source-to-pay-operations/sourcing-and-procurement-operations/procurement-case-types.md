---
title: Procurement case types
description: Procurement case types classify and route procurement work items to the appropriate team, and can block order or sourcing processing until the required review or action is complete.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-04-13"
reading_time_minutes: 4
keywords: [procurement case types, procurement case management, PCM, sourcing and procurement operations, SPO]
breadcrumb: [Procurement Case Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Procurement case types

Procurement case types classify and route procurement work items to the appropriate team, and can block order or sourcing processing until the required review or action is complete.

## What procurement case types do

Each procurement case in Procurement Case Management \(PCM\) carries a case type that determines its purpose, the team that handles it, and its effect on the associated purchase order or sourcing activity. When a case is open, the case type controls whether the purchase order or sourcing process can advance or must wait until the case is resolved.

Procurement Case Management provides 13 base system case types covering purchase modifications, compliance reviews, and employee support requests. Each case type follows a defined workflow, and some are handled through guided playbooks that walk fulfillers through the required activities.

## Case type categories

The 13 base system case types fall into three categories based on who initiates them and what they are used for.

|Category|Case type|Purpose|
|--------|---------|-------|
|Purchase modification|Edit a purchase|Modify an existing purchase requisition or purchase order — for example, to change quantity, price, or delivery date.|
|Return a purchase|Return received goods to the supplier.|
|Replace a purchase|Replace damaged, incorrect, or defective goods.|
|Edit a receipt|Correct a receiving record after goods have been received.|
|Compliance review|GL Coding Review|Verify and correct the general ledger account coding on a purchase line before the order is placed.|
|Budget Review|Confirm that sufficient budget exists for the purchase.|
|Contract Review|Review applicable contracts before the purchase proceeds.|
|Send NDA for Signature|Send a non-disclosure agreement to the supplier associated with the purchase.|
|Delivery Address Review|Verify and approve the delivery address for a purchase before the order proceeds.|
|Due Diligence|Conduct a supplier due diligence assessment before a purchase proceeds.|
|Support request|Inquiry|Ask a general procurement question or request support from the procurement team.|
|Request a Corporate Card|Request a corporate purchasing card for business expenses.|
|Request a copy of contract|Obtain a copy of an existing supplier contract for reference.|

## How it works

When a procurement event occurs — such as a purchase requisition submission, a Shopping Hub action, or an employee catalog request — the system creates a procurement case on the `sn_spend_psd_procurement_request` table and stamps the appropriate case type.

The following describes how a procurement case moves through its lifecycle:

1.  A case is created, either automatically by the system or manually by a user, with a specific case type that determines the workflow and the assignment group.
2.  If the case type is configured to block processing, the associated purchase order or sourcing activity is placed on hold until the case is closed. Compliance review cases — such as GL Coding Review and Budget Review — commonly use this behavior.
3.  The assigned group works through the required activities. For playbook-driven case types, a guided playbook presents the fulfiller with structured activities and decision points.
4.  When the fulfiller resolves the case, any blocking flag is released and the purchase order or sourcing activity can continue.

## Order and sourcing blocking

Some case types prevent a purchase order or sourcing activity from advancing while the case is open. Two independent flags on the case record control this behavior:

-   Order dependent on case: The purchase order step in the procurement workflow cannot advance until the case is closed. GL Coding Review, Budget Review, Contract Review, Send NDA for Signature, and Delivery Address Review all set this flag by default.
-   Sourcing dependent on case: The sourcing and negotiation step cannot advance until the case is closed. Budget Review sets this flag by default.

The blocking is enforced by the Procurement Operations Platform work item and step framework. When a purchase order or procurement request is viewed, the framework evaluates whether any open cases with blocking flags are associated with that record. While a blocking case remains open, the relevant step, such as the Reviewed step for order-dependent cases or the Negotiated step for sourcing-dependent cases, displays as in progress with the open case shown as a work item that must be resolved. The step cannot advance to complete while the case is active.

The hold releases automatically. When the blocking case is closed, the next time the purchase order or sourcing record is viewed, the framework re-evaluates the step and advances it to complete if no other blocking cases remain open.

**Note:** If you cancel a purchase order or purchase requisition that has open procurement cases, the system displays a warning and cancels all associated open cases when the cancellation is confirmed.

**Parent Topic:**[Procurement Case Management](psd-overview.md)

**Related topics**  


[Base system procurement case type reference](../reference/base-system-procurement-case-types.md)

