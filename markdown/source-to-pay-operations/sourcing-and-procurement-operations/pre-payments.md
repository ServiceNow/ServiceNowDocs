---
title: Pre-payments
description: A prepayment is the amount paid for services before their receipt or invoiced due date. When an invoice is issued for a pre-payment, it is against the pre-paid account. During the defined pre-paid period, the amount is amortized accordingly against the capex or expense account.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Purchase lines, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Pre-payments

A prepayment is the amount paid for services before their receipt or invoiced due date. When an invoice is issued for a pre-payment, it is against the pre-paid account. During the defined pre-paid period, the amount is amortized accordingly against the capex or expense account.

The **Pre-payments required** field on the purchase line indicates if pre-payments can be credited to the supplier against a purchase. Selecting this field also results in the display of the Pre-payments related list on the purchase line. The pre-payment information is carried over to a purchase order line whenever a purchase order is created.

The following are the key fields of a prepayment:

<table id="table_o3g_fjp_hlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique identifier of the pre-payment.

</td></tr><tr><td>

Contract

</td><td>

Contract to which this pre-payment is associated.

</td></tr><tr><td>

Purchase line

</td><td>

The purchase line associated with this pre-payment. This field is auto-populated when created from the pre-payments related list on purchase line.

</td></tr><tr><td>

Purchase requisition

</td><td>

The purchase requisition associated with this pre-payment. This field is referenced from the purchase line.

</td></tr><tr><td>

Purchase order line

</td><td>

The purchase order for which pre-payments are authorized up to the specified amount.This field is auto-populated when a purchase order line is created from the purchase line.

</td></tr><tr><td>

Purchase order

</td><td>

The purchase order associated with this pre-payment. This field is referenced from the purchase order line.

</td></tr><tr><td>

Authorized by

</td><td>

The user who authorizes this pre-payment. This field is populated based on the user who creates the pre-payment.

</td></tr><tr><td>

Authorized on

</td><td>

The date on which the pre-payment is authorized.

</td></tr><tr><td class="sub-head" colspan="2">

Accounting Details

</td></tr><tr><td>

Amount

</td><td>

Total purchase line amount.

</td></tr><tr><td>

Currency code

</td><td>

Currency code of the total line amount.

</td></tr><tr><td>

Pre-pay on

</td><td>

Date on which the specified amount is pre-paid.

</td></tr><tr><td>

Pre-pay by

</td><td>

The type of pre-payment. For example, **Amount** or **Percentage**.

</td></tr><tr><td>

Pre-payment percentage

</td><td>

The percentage of the total line amount for the pre-payment.This field is visible only if the pre-payment type is set to **Percentage**.

</td></tr><tr><td>

Pre-payment amount

</td><td>

The portion of the total line amount for the pre-payment.

</td></tr><tr><td>

Pre-paid period start

</td><td>

The start date of the pre-payment period, from which the pre-payments start.

</td></tr><tr><td>

Pre-paid period end

</td><td>

The end date of the pre-payment period, after which no pre-payments are made.

</td></tr></tbody>
</table>Multiple pre-payments related to one line can be made. For example, you can pre-pay 50% of the total line amount on X date and another 50% on Y date. The total of the pre-payment amounts must not exceed the line amount.

**Parent Topic:**[Purchase lines](purchase-lines.md)

