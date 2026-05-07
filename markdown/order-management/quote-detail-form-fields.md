---
title: Quote details forms
description: Use Quote details forms to capture, view, and manage all key information about a quote.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Quote details forms

Use Quote details forms to capture, view, and manage all key information about a quote.

<table id="table_c12_hxd_x1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System‑generated unique identifier for the quote.

</td></tr><tr><td>

Active

</td><td>

Option indicating that the current quote is the active quote. When there are multiple versions of a quote, selecting this option indicates this is the active quote.

</td></tr><tr><td>

State

</td><td>

Options that reflect the quote status.-   Draft - The default state of a quote that indicates the quote is still in development.
-   In review - Use this state to indicate that the quote is in a review state.
-   Pending customer acceptance - Set to this state when the quote is created and in review with a customer.
-   Accepted - Use this state to indicate that the quote was accepted by the customer.
-   Revised - Revised indicates that changes have been made to the quote that other working on the quote can take note.
-   Expired - Shows that the quote is beyond its expiration date. Reset the expiration date to make the quote active again.
-   Canceled - Use this state to show that the quote is canceled.
-   Closed - Shows that the quote is closed.
-   Completed - Shows that the quote is completed. When a quote is set to **Completed**, the quote can be used to create an order. For more info, see [Convert quotes into orders](../task/quote-management-customer-orders-tab.md).

</td></tr><tr><td>

Synced

</td><td>

Indicates whether the quote is synchronized with a downstream or external process.

</td></tr><tr><td>

Created by

</td><td>

Identifies the user who created the quote.

</td></tr><tr><td>

Source Opportunity

</td><td>

References the opportunity from which the quote was created, if applicable.

</td></tr><tr><td>

Account

</td><td>

The customer account for which the quote is created.

</td></tr><tr><td>

Enable sales agreement quote

</td><td>

Option to enable a quote to be governed by a sales agreement.

</td></tr><tr><td>

Contact

</td><td>

Primary customer contact associated with the quote.

</td></tr><tr><td>

Sales agreement

</td><td>

A sales agreement that defines the scope, pricing, and conditions under which the quote is created.

</td></tr><tr><td>

Partner account

</td><td>

Specifies the partner organization associated with the quote, such as a reseller or distributor, if applicable.

</td></tr><tr><td>

Existing contract

</td><td>

References an existing contract associated with the quote.

</td></tr><tr><td>

Partner contract

</td><td>

Specifies the contact person from the partner organization.

</td></tr><tr><td>

Assignment group

</td><td>

The group responsible for owning and processing the quote.

</td></tr><tr><td>

Channel partner

</td><td>

Specifies the channel partner involved in the quote.

</td></tr><tr><td>

Assigned to

</td><td>

The individual user responsible for the quote.

</td></tr><tr><td>

Deal type

</td><td>

Indicates the type of deal associated with the quote:-   Direct: The seller engages directly with the customer, with no intermediary partner involved.
-   Indirect: The seller engages the customer through an intermediary, such as a reseller, service provider, or distributor.

</td></tr><tr><td>

Route to market

</td><td>

Identifies the exact sales channel used to execute the deal:-   Direct
-   Reseller
-   Distributor

</td></tr><tr><td>

Short description

</td><td>

A brief description that summarizes the quote.

</td></tr><tr><td>

Consolidated quote

</td><td>

Indicates the quote is generated after consolidating multiple contracts, contract lines, or source opportunities into a single unified commercial offer.

</td></tr></tbody>
</table>| | |
|---|---|
|Currency|The currency for the price matches the currency stated in the account information.|
|Renewal adjustment basis|Specifies the price reference used to calculate renewal pricing adjustments, such as contracted price or price list.|
|Price list|The Standard Price List field is the default price list for the product catalogs referenced in the quote.|
|Renewal adjustment type|Specifies the method used to adjust the renewal price, such as applying a markup percentage to the selected renewal adjustment basis. The adjustment type is applied after the renewal adjustment basis is determined.|
|Cost book|The Standard Cost Book is the default cost book for the product catalogs referenced in the quote.|
|Renewal adjustment value|Specifies the numeric value used to adjust the renewal price, such as a percentage increase or decrease applied during renewal pricing.|

<table id="table_hxc_skx_m3c"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Total annual price

</td><td>

Sum of the cumulative annual recurring price of all root parent quote lines. This value represents the total recurring revenue for the quote over one year.

</td></tr><tr><td>

Total cost

</td><td>

Roll‑up of the cumulative net cost of all root parent quote lines. This includes one‑time costs and recurring costs calculated over the quote term.

</td></tr><tr><td>

Total amount

</td><td>

Roll‑up of the cumulative net price of all root parent quote lines. This represents the total quoted amount, including recurring and one‑time charges.

</td></tr><tr><td>

Total margin%

</td><td>

Percentage representing the overall profitability of the quote. Calculated as:\(Total amount − Total cost\) ÷ Total amount × 100

</td></tr><tr><td>

Total net new amount

</td><td>

Sum of the cumulative net price for all root quote lines with Line Type = Net New. This value represents incremental revenue generated from new products or services only.

</td></tr></tbody>
</table>| | |
|---|---|
|Quote date|Date from which the quote is considered valid. This date is used as the reference point for quote lifecycle and pricing calculations.|
|Contract start date|Date on which the contract associated with the quote becomes effective. This date is used to calculate subscription pricing, term, and contract end date.|
|Expiration date|Date after which the quote is no longer valid. This date defines the offer validity period and is used on generated quote and order documents.|
|Contract end date|Date on which the contract term ends. This date is derived from the contract start date and term, and is used to determine renewal eligibility and renewal quote generation.|
|Payment Terms|Specifies the payment conditions agreed for the quote, such as when payment is due after invoicing. Payment terms are applied to the quote document and downstream orders.|
|Term \(months\)|Duration of the contract or subscription in months. When a start and end date are provided, the system automatically calculates the term value.|
|Quote Document Details|Contains information used when generating the quote document, such as dates, pricing, and validity details displayed on the document sent to the customer.|
|Auto-renew contract|Indicates whether the contract is enabled for automatic renewal. When selected, the system automatically generates renewal opportunities and renewal quotes based on configurable rules before the contract end date.|

| | |
|---|---|
|Billing address same as shipping|Indicates whether the billing address is the same as the shipping address. When enabled, billing address fields are automatically populated from the shipping address.|
|Shipping location|Reference to the shipping location associated with the quote. This location identifies where products or services are delivered.|
|Shipping street|Street address of the shipping location.|
|Shipping city|City of the shipping address.|
|Shipping state/Province|State or province of the shipping address.|
|Shipping country|Country of the shipping address.|
|Shipping Zip/Postal code|ZIP or postal code of the shipping address.|
|Billing location|Reference to the billing location associated with the quote. This location is used for invoicing and billing purposes.|
|Billing street|Street address of the billing location.|
|Billing city|City of the billing address.|
|Billing state/Province|State or province of the billing address.|
|Billing country|Country of the billing address.|
|Billing Zip/Postal code|ZIP or postal code of the billing address.|

| | |
|---|---|
|Work notes|Internal notes used to record behind‑the‑scenes information related to the quote, such as negotiation details, pricing decisions, or internal follow‑ups. Work notes are intended for internal users only and are included in the quote activity history.|
|Additional comments|Free‑form comments used to capture customer‑facing or general information related to the quote. Additional comments can be used to communicate updates or clarifications and are visible to a broader audience, depending on access permissions.|

**Parent Topic:**[Configure, price, quote reference](../concept/reference-cpq.md)

