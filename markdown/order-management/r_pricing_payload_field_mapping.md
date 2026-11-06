---
title: Pricing payload field mapping
description: Pricing payload fields that ServiceNow Quote Experience sends to the pricing service, with the ServiceNow Quote Experience field each one maps to. Use this reference to check header, line item, and entity metadata values in the payload.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/r\_pricing\_payload\_field\_mapping.html
release: australia
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 2
keywords: [pricing payload, field mapping, Transaction Manager, pricing service, payload]
breadcrumb: [Pricing Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Pricing payload field mapping

Pricing payload fields that ServiceNow Quote Experience sends to the pricing service, with the ServiceNow Quote Experience field each one maps to. Use this reference to check header, line item, and entity metadata values in the payload.

## Reading the mapping

Values in code format in the TXM field column are ServiceNow Quote Experience field names. Values in plain text are literal values or descriptions sent to Pricing instead of a field. Fields marked Not mapped have no ServiceNow Quote Experience field in the source.

## Header fields

|Pricing payload field|Pricing field type|TXM field|Required|
|---------------------|------------------|---------|--------|
|`header.source_system`|Text|`sn_l2c_quote_exp`|Yes|
|`header.sys_class_name`|Text| |No|
|`header.requesting_record_id`|Reference|`txn.id`|Yes|
|`header.currency`|Text|`txn.pricing.currencyCode`|Yes|
|`header.pricelist`| |`txn.pricebook.id`| |
|`header.costbook`|Reference|`txn.costbook`|Optional|
|`header.account`|Reference|`txn.account.id`|Yes|

## Line item fields

|Pricing payload field|Pricing field type|TXM field|Required|
|---------------------|------------------|---------|--------|
|`header.lineItems.account`|Reference|Derived internally using header account|Yes|
|`header.lineItems.currency`| |Derived internally using header currency|Yes|
|`header.lineItems.line_type`|Text|`txn.line.lineType`|Yes|
|`header.lineItems.action`|Text|`txn.line.lineAction`|Yes|
|`header.lineItems.pricelist`|Reference|Derived internally using header pricelist|Yes|
|`header.lineItems.product_offering`|Reference|`txn.line.product.partnerId`|Yes|
|`header.lineItems.quantity`|Decimal|`txn.line.quantity`|Yes|
|`header.lineItems.selected`|Boolean|Not applicable|Not applicable|
|`header.lineItems.shipping_city`|Text|Not Productizing|Optional|
|`header.lineItems.shipping_country`|Text|Not Productizing|Optional|
|`header.lineItems.shipping_state`|Text|Not Productizing|Optional|
|`header.lineItems.shipping_zip`|Text|Not Productizing|Optional|
|`header.lineItems.term_month`|Decimal|`txn.line.term`|Optional|
|`header.lineItems.top_line_item`|Reference|Derived internally|Yes|
|`header.lineItems[].top_product_offer`|Reference|Derived internally. Line's top line's txn.line.product.partnerId|Yes, to confirm|
|`header.lineItems[].top_line_id`|Text|Derived internally. Line's top line's txn.line.id|Yes|
|`header.lineItems.parent_product_offer`|Reference|Derived internally. Line's parent line's txn.line.product.partnerId|Yes, to confirm|
|`header.lineItems[].parent_line_id`|Text|Derived internally. Line's parent line's txn.line.id|Yes|
|`header.lineItems.unit_of_measure`|Reference|`txn.line.product.uom`|Yes|
|`header.lineItems.transaction_date`|Date|`txn.quoteDate`|Yes|
|`header.lineItems.line_id`|Number|`txn.line.id`|Yes|
|`header.lineItems.characteristics`|Array\[Characteristic\]|`txn.line.product.characteristics`|Optional|
|`header.lineItems.characteristics.characteristic`|Reference|Not Productizing|Optional|
|`header.lineItems.characteristics.characteristic_option`|Reference|Not Productizing|Optional|
|`header.lineItems.characteristics.characteristic_option_value`| |Not Productizing|Optional|
|`header.lineItems.line_ramp`| |Not mapped|Optional|
|`header.lineItems.ramp_type`| |Not mapped|Optional|
|`header.lineItems.ramp_api`| |Not mapped|Optional|
|`header.lineItems.ramp_sequence`| |Not mapped|Optional|
|`header.lineItems.source_sold_product`| |`txn.line.source.splitFromSoldProduct`|Optional|
|`header.lineItems.split_from_line_id`| |Empty|Optional|
|`header.lineItems.delta_price_treatment`| |`txn.line.pricing.delta.priceTreatment`|Optional|
|`header.lineItems.renewed_from_contract_line`| |`txn.line.source.contract.line`|Optional|
|`header.lineItems.renewed_from_entitlement`| |`txn.line.source.entitlement`|Optional|
|`header.lineItems.consolidated_from_clis`| |`txn.line.source.consolidation.lines`|Optional|
|`header.lineItems.pricingAdjustments.adjustment_type`|Text|`txn.line.pricing.discount.adjustmentType`|Optional|
|`header.lineItems.pricingAdjustments.adjustment_value`|Decimal|`txn.line.pricing.discount.value`|Optional|
|`header.lineItems.pricingAdjustments.name`|Text|`txn.line.pricing.discount.description`|Optional|

## Entity metadata and settings

|Pricing payload field|Pricing field type|TXM field|Required|
|---------------------|------------------|---------|--------|
|`entity_meta_data.entity_id`|Text|`sn_l2c_quote`|Yes|
|`entity_meta_data.scope`|Text|`quote_experience`|Yes|
|`entity_meta_data.config_top_line_identifier`|Number|Not needed|No|
|`entity_meta_data.header_sys_class_name`|Text|Not needed|No|
|`entity_meta_data.header_sys_id`|Reference|`txn.id`|Yes|
|`entity_meta_data.line_sys_class_name`|Text|Not needed|No|
|`entity_meta_data.price_line_id`|Array\[Number\]|Array of txnLineIds|Yes|
|`entity_meta_data.settings.pricing_elements`|Text|`PRICE,NET_PRICE,HEADER_ROLLUPS,LINE_ROLLUPS,COST,ADJUSTMENTS,DELTA`|Yes|
|`entity_meta_data.settings.execution_mode`|Text|`sync`|Yes|
|`entity_meta_data.settings.disable_validation`|Boolean|Not needed|No|

**Parent Topic:**[Pricing Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/price-management-reference.md)

