---
title: Base system procurement case type reference
description: Procurement Case Management provides 13 base system case types that classify procurement work.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-04-13"
reading_time_minutes: 4
keywords: [procurement case types, base system case types, procurement case management, PCM, sourcing and procurement operations, SPO, case type reference]
breadcrumb: [Reference, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Base system procurement case type reference

Procurement Case Management provides 13 base system case types that classify procurement work.

## Purchase modification cases

Purchase modification cases are initiated by a requestor or shopper from within ShoppingHub.

<table><thead><tr><th>

Case type

</th><th>

Purpose

</th><th>

How it is created

</th></tr></thead><tbody><tr><td>

**Edit a purchase** `edit_purchase`

</td><td>

Modify an existing purchase requisition or purchase order — for example, to change quantity, price, delivery date, or line items.

</td><td>

Requestor selects the edit action in ShoppingHub. The system creates a purchase modification record and the `create_procurement_case` subflow creates the case.

</td></tr><tr><td>

**Return a purchase** `return_purchase`

</td><td>

Return received goods to the supplier.

</td><td>

Requestor selects the return action in ShoppingHub. The system creates a purchase modification record and the `create_procurement_case` subflow creates the case.

</td></tr><tr><td>

**Replace a purchase** `replace_purchase`

</td><td>

Replace damaged, incorrect, or defective goods.

</td><td>

Requestor selects the replace action in ShoppingHub. The system creates a purchase modification record and the `create_procurement_case` subflow creates the case.

</td></tr><tr><td>

**Edit a receipt** `edit_receipt`

</td><td>

Correct a receiving record after goods have been received — for example, to adjust the quantity received.

</td><td>

Requestor selects the edit receipt action in ShoppingHub. The case is handled end-to-end by the Edit a Receipt playbook.

</td></tr></tbody>
</table>## Compliance review cases

Compliance review cases are created automatically by the system when a purchase requisition or purchase order meets the conditions defined in the Task Generation Decision Table, or when a procurement specialist opens a case manually.

<table><thead><tr><th>

Case type

</th><th>

Purpose

</th><th>

How it is created

</th></tr></thead><tbody><tr><td>

**GL Coding Review** `gl_coding_review`

</td><td>

Verify and correct the general ledger account coding on a purchase line before the order is placed.

</td><td>

Automatic — the Task Generation Decision Table creates the case when a purchase requisition is submitted and the GL coding review rule fires.

</td></tr><tr><td>

**Budget Review** `budget_review`

</td><td>

Confirm that sufficient budget exists for the purchase before the order is placed or sourced.

</td><td>

Automatic — the Task Generation Decision Table creates the case when a purchase requisition is submitted and the budget review rule fires.

</td></tr><tr><td>

**Contract Review** `contract_review`

</td><td>

Review applicable contracts before the purchase proceeds.

</td><td>

Automatic — the Task Generation Decision Table creates the case when a purchase requisition is submitted and the contract review rule fires.

</td></tr><tr><td>

**Send NDA for Signature** `send_nda`

</td><td>

Send a non-disclosure agreement to the supplier associated with the purchase for signature before the purchase proceeds.

</td><td>

Automatic — the Task Generation Decision Table creates the case when a purchase requisition is submitted and the NDA rule fires.

</td></tr><tr><td>

**Delivery Address Review** `delivery_address_review`

</td><td>

Verify and approve the delivery address on a purchase before the order proceeds. The case is created when the delivery address on the purchase requisition requires verification or company approval.

</td><td>

Automatic — created by the system when a purchase requisition is submitted and the delivery address on a line item requires review. Requires the Purchase Modification Content Pack \(`sn_spend_cp`\).

</td></tr><tr><td>

**Due Diligence** `due_diligence`

</td><td>

Conduct a supplier due diligence assessment before a purchase proceeds.

</td><td>

Manual — opened by a procurement specialist — or automatically via the Task Generation Decision Table during supplier qualification. The case is initially assigned to the user who creates it.

</td></tr></tbody>
</table>## Support request cases

Support request cases are opened by employees through the Service Catalog or Employee Center to get help from the procurement organization.

<table><thead><tr><th>

Case type

</th><th>

Purpose

</th><th>

How it is created

</th></tr></thead><tbody><tr><td>

**Inquiry** `inquiry`

</td><td>

Request general support or ask a question of the procurement organization.

</td><td>

Employee submits the **Ask procurement** catalog item in the Service Catalog or Employee Center.

</td></tr><tr><td>

**Request a Corporate Card** `request_cc`

</td><td>

Request a corporate purchasing card for business expenses. The procurement or finance team processes the request and coordinates card issuance.

</td><td>

Employee initiates the request. The specific catalog item or portal entry point is configured during implementation.

</td></tr><tr><td>

**Request a copy of contract** `request_contract_copy`

</td><td>

Obtain a copy of an existing supplier contract for reference.

</td><td>

Employee submits the **Request a copy of contract** catalog item in the Service Catalog or Employee Center. The system links the case to the relevant contract record and populates the case description with the contract number.

</td></tr></tbody>
</table>**Parent Topic:**[Sourcing and Procurement Operations reference](spo-reference.md)

**Related topics**  


[Create New Pipeline Project form](create-pipeline-project-form.md)

[Pipeline project record tabs and UI actions](pipeline-form-tabs-actions.md)

[Purchase requisition, purchase order, and sourcing request states](pr-po-sr-states.md)

[SPO and ITAM data model mappings](../concept/itam-spo-data-model.md)

[Domain separation and Sourcing and Procurement Operations](../concept/psm-domain-separation.md)

[Sourcing and Procurement Operations glossary](../concept/spo-glossary.md#)

[Procurement case types](../concept/procurement-case-types.md)

