---
title: Invoices
description: Invoices are generated for a payment against a purchase order. A purchase order can have multiple invoices depending on the payment schedule.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [invoices, invoice matching, create invoices]
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Invoices

Invoices are generated for a payment against a purchase order. A purchase order can have multiple invoices depending on the payment schedule.

You can manually create invoices in the ServiceNow platform or generate invoices through integration with an external supplier portal.

**Note:** Invoice matching is either done externally in the supplier portal or manually in ServiceNow. There’s currently no logic to perform invoice matching systematically in the ServiceNow platform.

![Invoice form.](../image/spo-invoice.png "Invoice form")

The following are the key fields of an invoice:

<table id="table_bxq_1gt_3lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier for the invoice.

</td></tr><tr><td>

ERP number

</td><td>

Unique identifier generated within an ERP system for the invoice. This field is applicable when there’s an ERP integration. The value is populated after the invoice is posted in the ERP system through the integration.

</td></tr><tr><td>

Status

</td><td>

Current status of the invoice.

</td></tr><tr><td>

Supplier invoice number

</td><td>

Invoice number of the supplier.**Note:** This is a mandatory field except when the invoice is in the Draft state.

</td></tr><tr><td>

Supplier tax id

</td><td>

Tax ID associated with the supplier.

</td></tr><tr><td>

Invoice date

</td><td>

Date on which this invoice is created.**Note:** This is a mandatory field except when the invoice is in the Draft state.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Supplier

</td><td>

Supplier from whom the product or service is procured.

</td></tr><tr><td>

Purchase order

</td><td>

Purchase order to which this invoice has been matched.

</td></tr><tr><td>

Invoice date

</td><td>

Date on which this invoice is created.**Note:** This is a mandatory field except when the invoice is in the Draft state.

</td></tr><tr><td>

Subtotal

</td><td>

Total amount of money to be paid to the supplier excluding tax and shipping charges.**Note:** This is an editable field.

</td></tr><tr><td>

Tax rate

</td><td>

Tax rate percentage applied for the order.

</td></tr><tr><td>

Sales tax

</td><td>

Sales tax charges incurred for the invoice.

</td></tr><tr><td>

Shipping

</td><td>

Shipping charges incurred for the invoice.

</td></tr><tr><td>

Other charges

</td><td>

Other additional charges associated to the invoice.

</td></tr><tr><td>

Discounts

</td><td>

Discounts applied to the invoice.

</td></tr><tr><td>

Amount invoiced \(Transaction currency\)

</td><td>

Total amount of money to be paid to the supplier including tax and shipping charges.**Note:** This is a mandatory field except when the invoice is in the Draft state. This is also an editable field.

</td></tr><tr><td class="sub-head" colspan="2">

Accounting Details

</td></tr><tr><td>

Legal entity

</td><td>

The internal legal entity which incurs the cost of this invoice.

</td></tr><tr><td>

Remit to address

</td><td>

The location to which this payment is made.

</td></tr></tbody>
</table>The following are the related lists of an invoice:

<table id="table_xdg_3rt_3lb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Invoice Lines

</td><td>

Captures the line amount and rolls up to the subtotal on the invoice.

</td></tr><tr><td>

Service Acknowledgments

</td><td>

Displays all the service acknowledgments associated with this invoice.

</td></tr><tr><td>

Approval Plans

</td><td>

Displays all the approval plans created against this invoice.

</td></tr><tr><td>

Approvals

</td><td>

When the services acknowledgment is set to **Invoice approval**, invoice approvals act as a form of receipt before issuing the payment to a supplier.In the absence of a receipt and three-way matching, invoice approvals are used to avoid an automatic two-way match.

 Invoice approvals are sent to the recipient of the line and the shopper can act on them as a to-do in ShoppingHub.

 For details, see [Shopper to-dos](shopper-todos.md).

</td></tr><tr><td>

Invoice Tasks

</td><td>

When a service acknowledgment is triggered, a task is created against the invoice and listed here.**Note:** If you are a new customer, or an existing customer who has upgraded and installed the Shopping Hub plugin, these tasks aren't applicable for you. However, if you choose to continue with the existing Source-to-Pay Common Architecture plugin and skip the Shopping Hub plugin, these tasks are available for you to work on.

</td></tr></tbody>
</table>To create an invoice from a supplier for a received product or service, edit the **Subtotal** field in the Invoice form to the actually received amount, add an invoice line to capture the specifics of that purchase order line, and update the **Line amount invoiced** field in that Invoice Line form to reflect the same received amount. When the invoice line and the invoice are both updated to the Paid state, an expense line in auto-generated in the Project form of Project Management for which the purchase was originally made.

For more information on Sourcing and Procurement Operations's integration with Project Management, see [Sourcing and Procurement Operations integration with Project Management](../concept/integration-psm-ppm.md).

## Invoice calculations and state flows

**Note:** Business rules pertaining to handling state changes, handling tax and charges, default invoice fields, populating invoice line amounts, handling line total changes, and populating supplier products are available only if you haven't installed the Shopping Hub \(sn\_spend\_uib\) plugin and are still using the Source-to-Pay Common Architecture \(sn\_shop\) plugin.​

A field named **Amount requiring approval** on the invoice approval record distinguishes the actual invoice amount that needs to be approved, as the invoice lines within an invoice could consist of different services acknowledgment types and/or goods receipt required conditions.

When an invoice line that is sent for approval is approved, the status of the invoice line is updated to Invoice Confirmed. If any line within the invoice is rejected, the entire invoice is rejected.

The status of the invoice is updated to Invoice Confirmed only when the status of all the corresponding invoice lines are Invoice Confirmed. If the status of the invoice is updated to Invoice Confirmed, then the status of all the associated invoice lines are also updated to Invoice Confirmed. This applies to the scenario when matching is done manually in the Now Platform and the user updates the invoice header instead of updating line by line. This update is done by selecting **Confirm** on the invoice header. When the invoice state is Invoice Confirmed, the **Confirm** button isn’t displayed for any subsequent state as well.

The invoice state on the invoice header is read-only as the state change is driven by the lines. In case of a multi-line invoice, if one line is in a Requires Review state, the invoice header is updated to Requires Review as well.

**Parent Topic:**[Sourcing and Purchasing Automation](purchase-experience-workflow.md)

