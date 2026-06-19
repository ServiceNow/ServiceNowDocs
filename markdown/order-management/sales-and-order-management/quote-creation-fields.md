---
title: Quote creation via Self-Service fields for Channel Partners
description: Store the main details related to a quote submitted by a partner and track the life cycle of the quote through its stages on the self-service quote \(sn\_quote\_mgmt\_core\_quote\) table. Use the fields to manage and store information related to quote creation by channel partners.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/quote-creation-fields.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-05-29"
reading_time_minutes: 2
breadcrumb: [Partner Relationship Management reference, Reference, Sales Customer Relationship Management]
---

# Quote creation via Self-Service fields for Channel Partners

Store the main details related to a quote submitted by a partner and track the life cycle of the quote through its stages on the self-service quote \(sn\_quote\_mgmt\_core\_quote\) table. Use the fields to manage and store information related to quote creation by channel partners.

**Note:**

The fields displayed on this form are pre-defined. You can configure the form to add or remove fields, and update the table to show or hide columns to match the partner experience.

|Field|Description|
|-----|-----------|
|Channel partner|Reference to the channel partner \(sn\_prm\_channel\_partner\) table.|
|Account|The customer account for which the quote is created.|
|Consumer|Reference to consumer \(csm\_consumer\).|
|Contact|Primary customer contact associated with the quote.|
|Short description|A brief description that summarizes the quote.|

|Field|Description|
|-----|-----------|
|Source opportunity|The opportunity record associated with this quote.|
|Currency|The currency for the price matches the currency stated in the account information.|
|Renewal adjustment basis|Specifies the price reference used to calculate renewal pricing adjustments, such as contracted price or price list.|
|Price list|The **Standard Price List** field is the default price list for the product catalogs referenced in the quote.|
|Renewal adjustment type|Specifies the method used to adjust the renewal price, such as applying a markup percentage to the selected renewal adjustment basis. The adjustment type is applied after the renewal adjustment basis is determined.|
|Quote date|Date from which the quote is considered valid. This date is used as the reference point for quote lifecycle and pricing calculations.|
|Contract start date|Date on which the contract associated with the quote becomes effective. This date is used to calculate subscription pricing, term, and contract end date.|
|Expiration date|Date after which the quote is no longer valid. This date defines the offer validity period and is used on generated quote and order documents.|
|Contract end date|Date on which the contract term ends. This date is derived from the contract start date and term, and is used to determine renewal eligibility and renewal quote generation.|
|Payment Terms|Specifies the payment conditions agreed for the quote, such as when payment is due after invoicing. Payment terms are applied to the quote document and downstream orders.|
|Term \(months\)|Duration of the contract or subscription in months. When a start and end date are provided, the system automatically calculates the term value.|
|Auto-renew contract|Indicates whether the contract is enabled for automatic renewal. When selected, the system automatically generates renewal opportunities and renewal quotes based on configurable rules before the contract end date.|
|Shipping/Billing location|Reference to the shipping/billing location associated with the quote. This location identifies where products or services are delivered.|
|Shipping/Billing street|Street address of the shipping location.|
|Shipping/Billing city|The city of the shipping address.|
|Shipping/Billing state / Province|The state or province of the shipping address.|
|Shipping/Billing country|The country of the shipping address.|
|Shipping/Billing Zip / Postal code|The postal code or ZIP of the shipping address.|

## Product offerings catalog

Enter the products that the customer is interested in the **Select a catalog** field.

## Line items

Apply a header discount across all line items, or delete line items in the **Apply header discount**.

**Parent Topic:**[Partner Relationship Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/partner-relationship-management-reference.md)

