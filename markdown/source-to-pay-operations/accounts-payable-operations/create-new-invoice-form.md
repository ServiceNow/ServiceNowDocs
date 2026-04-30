---
title: Create New Invoice form
description: Use the Create New Invoice form to enter the details of the new invoice.
locale: en-US
release: yokohama
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create New Invoice Line form, Accounts Payable Operations reference, Accounts Payable Operations, Finance and Supply Chain]
---

# Create New Invoice form

Use the Create New Invoice form to enter the details of the new invoice.

<table id="table_lwn_2jj_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Invoice

</td></tr><tr><td>

Number

</td><td>

An auto-generated number that uniquely identifies the invoice.

</td></tr><tr><td>

Supplier invoice number

</td><td>

The invoice number of the supplier invoice.

</td></tr><tr><td>

Type

</td><td>

The type of invoice.**Note:** Accounts Payable Operations supports invoices of type **PO invoice** and **Non-PO invoice**.

</td></tr><tr><td>

Business owner

</td><td>

An individual or group who owns the invoice.

</td></tr><tr><td>

Status

</td><td>

The status of the invoice.

</td></tr><tr><td>

Channel

</td><td>

The channel used to send the invoice. The choices are:-   **Web**
-   **Email**
-   **integration**
-   **Virtual agent**

</td></tr><tr><td>

Supplier tax id

</td><td>

The tax ID of the supplier.

</td></tr><tr><td>

Supplier tax

</td><td>

The total tax amount charged by the supplier.

</td></tr><tr><td>

System tax

</td><td>

The total tax amount calculated by the third party tax calculation engine.

</td></tr><tr><td>

ERP number

</td><td>

Unique number generated within the ERP system for the invoice.This field is applicable when there is an ERP integration. The value is populated after the invoice is posted in the ERP system through the integration.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the invoice.

</td></tr><tr><td class="sub-head" colspan="2">

Summary Details

</td></tr><tr><td>

Supplier

</td><td>

Supplier who delivers the product or service.

</td></tr><tr><td>

Purchase order

</td><td>

Purchase order associated with this invoice.**Note:** For **Non-PO invoice** the purchase order is not made available.

</td></tr><tr><td>

Payment terms

</td><td>

How and when to make a payment for the products and services.

</td></tr><tr><td>

Subtotal

</td><td>

The total amount from all the invoice lines without tax and shipping charges.

</td></tr><tr><td>

Tax amount

</td><td>

Tax applied on the invoice amount.

</td></tr><tr><td>

Shipping

</td><td>

Shipping charges incurred for the invoice.

</td></tr><tr><td>

Other charges

</td><td>

Other charges applied on the invoice amount.

</td></tr><tr><td>

Discounts

</td><td>

The discount applied on the invoice amount.

</td></tr><tr><td>

Early payment discount amount

</td><td>

The discount applied on the total invoice amount on early payment.

</td></tr><tr><td>

Amount invoiced without tax \(Transactional currency\)

</td><td>

Total amount to be paid to the supplier excluding tax and shipping charges. This amount is displayed in transactional currency.

</td></tr><tr><td>

Amount invoiced \(Transactional currency\)

</td><td>

Total amount to be paid to the supplier including tax and shipping charges. This amount is displayed in transactional currency.

</td></tr><tr><td class="sub-head" colspan="2">

Dates

</td></tr><tr><td>

Invoice date

</td><td>

Date on which this invoice is created.

</td></tr><tr><td>

Due date

</td><td>

Date by when you must make the payment.

</td></tr><tr><td>

ERP posting date

</td><td>

Date on which the invoice is posted in the ERP system.

</td></tr><tr><td>

Payment date

</td><td>

The date by when you must make the payment.

</td></tr><tr><td class="sub-head" colspan="2">

Accounting Details

</td></tr><tr><td>

Legal entity

</td><td>

The internal legal entity which incurs the cost of this invoice.

</td></tr><tr><td>

Default tax code

</td><td>

The tax code levied on the total invoice amount.

</td></tr><tr><td>

Default tax jurisdiction code

</td><td>

The tax code jurisdiction to which you must pay the tax.

</td></tr><tr><td class="sub-head" colspan="2">

Addresses

</td></tr><tr><td>

Remit to street

</td><td>

The street address to which the payment is made.

</td></tr><tr><td>

Remit to country

</td><td>

The country to which the payment is made.

</td></tr><tr><td>

Remit to city

</td><td>

The city to which the payment is made.

</td></tr><tr><td>

Remit to zip/postal code

</td><td>

The zip code to which this payment is made.

</td></tr><tr><td>

Remit to state/province

</td><td>

The state to which the payment is made.

</td></tr><tr><td>

Bill to street

</td><td>

The street address to which the invoice is sent.

</td></tr><tr><td>

Bill to country

</td><td>

The country to which the invoice is sent.

</td></tr><tr><td>

Bill to city

</td><td>

The city to which the invoice is sent.

</td></tr><tr><td>

Bill to zip/postal code

</td><td>

The zip code to which the invoice is sent.

</td></tr><tr><td>

Bill to state/province

</td><td>

The state to which the invoice is sent.

</td></tr><tr><td>

Ship to street

</td><td>

The street address to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to country

</td><td>

The country to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to city

</td><td>

The city to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to zip/postal code

</td><td>

The zip code to which the items on the purchase order should be shipped.

</td></tr><tr><td>

Ship to state/province

</td><td>

The state to which the items on the purchase order should be shipped.

</td></tr></tbody>
</table>-   **[Invoice form tabs](invoice-form-related-list.md)**  
The Invoice form includes tabs that store invoice information that an Accounts Payable Specialist can use to perform related tasks.
-   **[Inbound Invoice Fields](inbound-invoice-fields.md)**  
The Inbound invoice table is the source table from where you import the invoice required fields to successfully create an invoice through the integration framework.
-   **[Outbound invoice fields](outbound-invoice-fields.md)**  
The outbound invoice table transfers the invoice details from ServiceNow® to third party applications through integration framework.

**Parent Topic:**[Create New Invoice Line form](create-invoice-line-form.md)

