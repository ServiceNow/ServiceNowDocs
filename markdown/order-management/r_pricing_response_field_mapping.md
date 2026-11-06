---
title: Pricing response field mapping
description: Pricing response fields that the pricing service returns to ServiceNow Quote Experience, with the ServiceNow Quote Experience field each one maps to. Use this reference to check header totals, line item prices, and settings in the response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/r\_pricing\_response\_field\_mapping.html
release: australia
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
keywords: [pricing response, field mapping, Transaction Manager, pricing service, response]
breadcrumb: [Pricing Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Pricing response field mapping

Pricing response fields that the pricing service returns to ServiceNow Quote Experience, with the ServiceNow Quote Experience field each one maps to. Use this reference to check header totals, line item prices, and settings in the response.

## Reading the mapping

Values in code format in the TXM field column are ServiceNow Quote Experience field names. Values in plain text are literal values or descriptions sent to Pricing instead of a field. Fields marked Not mapped have no ServiceNow Quote Experience field in the source.

## Header fields

|Pricing response field|TXM field|
|----------------------|---------|
|`header.currency`|`txn.pricing.currencyCode`|
|`header.costbook`|Not mapped|
|`header.total_amount`|`txn.pricing.total`|
|`header.total_one_time_price`|`txn.pricing.extendedPrice`|
|`header.total_one_time_cost`|`txn.pricing.cost`|
|`header.total_monthly_cost`|`txn.pricing.costRecurring`|
|`header.total_cost`|`txn.pricing.netCost`|
|`header.total_monthly_recurring_price`|`txn.pricing.netPriceRecurring`|
|`header.total_annual_recurring_price`|`txn.pricing.annualPriceRecurring`|
|`header.total_one_time_margin`|`txn.pricing.margin.amount`|
|`header.total_monthly_margin`|`txn.pricing.marginRecurring.amount`|
|`header.total_margin_amount`|`txn.pricing.margin.total.amount`|
|`header.total_one_time_margin_percentage`|`txn.pricing.margin.percentage`|
|`header.total_monthly_margin_percentage`|`txn.pricing.marginRecurring.percentage`|
|`header.total_margin_percentage`|`txn.pricing.margin.total.percentage`|
|`header.total_renewal_amount`|`txn.pricing.source.contract.amount`|
|`header.total_new_amount`|`txn.pricing.netNew`|
|`header.total_upsell_downsell_amount`|`txn.pricing.delta.upsellDownsellAmount`|
|`header.status`|Not mapped|

## Line item fields

|Pricing response field|TXM field|
|----------------------|---------|
|`header.lineItems`|Not mapped|
|`header.lineItems[].line_id`|Not mapped|
|`header.lineItems[].parent_line_id`|Not mapped|
|`header.lineItems[].top_line_id`|Not mapped|
|`header.lineItems[].status`|Not mapped|
|`header.lineItems[].currency`|Not mapped|
|`header.lineItems[].derived_price`|`txn.line.pricing.isDerived`|
|`header.lineItems[].floorPrice`|Not mapped|
|`header.lineItems[].ceilingPrice`|Not mapped|
|`header.lineItems[].base_price.value`|Not mapped|
|`header.lineItems[].list_price.value`|Not mapped|
|`header.lineItems[].pricelist`|Not mapped|
|`header.lineItems[].product_offering`|Not mapped|
|`header.lineItems[].parent_product_offer`|Not mapped|
|`header.lineItems[].top_product_offer`|Not mapped|
|`header.lineItems[].quantity`|Not mapped|
|`header.lineItems[].messages[].type`|Not mapped|
|`header.lineItems[].messages[].code`|Not mapped|
|`header.lineItems[].messages[].message`|Not mapped|
|`header.lineItems[].messages[].showToUser`|Not mapped|
|`header.lineItems[].price_list_line`|Not mapped|
|`header.lineItems[].product_offering_display_name`|Not mapped|
|`header.lineItems[].one_time_price.value`|`txn.line.pricing.extendedPrice`|
|`header.lineItems[].monthly_recurring_price.value`|`txn.line.pricing.netPriceRecurring`|
|`header.lineItems[].annual_recurring_price.value`|`txn.line.pricing.annualPriceRecurring`|
|`header.lineItems[].unit_net_price.value`|`txn.line.pricing.net`|
|`header.lineItems[].cumulative_net_price.value`|`txn.line.pricing.extendedNet`|
|`header.lineItems[].cumulative_acv.value`|Not mapped|
|`header.lineItems[].cumulative_one_time_price.value`|`txn.line.pricing.rollupPrice`|
|`header.lineItems[].cumulative_monthly_recurring_price.value`|`txn.line.pricing.rollupExtendedPriceRecurring`|
|`header.lineItems[].cumulative_annual_recurring_price.value`|`txn.line.pricing.rollupAnnualPriceRecurring`|
|`header.lineItems[].unit_adjustment.value`|`txn.line.pricing.adjustment.unit`|
|`header.lineItems[].term_month.value`|Not mapped|
|`header.lineItems[].cumulative_annual_recurring_price_v1.value`|Not mapped|
|`header.lineItems[].cumulative_monthly_recurring_price_v1.value`|Not mapped|
|`header.lineItems[].cumulative_ramp_price.value`|Not mapped|
|`header.lineItems[].total_recurring_price.value`|Not mapped|
|`header.lineItems[].total_new_amount.value`|Not mapped|
|`header.lineItems[].total_upsell_downsell_amount.value`|`txn.line.pricing.delta.upsellDownsellAmount`|
|`header.lineItems[].total_renewal_amount.value`|Not mapped|
|`header.lineItems[].attr_adj_config.adjustment_record`|Not mapped|
|`header.lineItems[].attr_adj_config.rules`|Not mapped|
|`header.lineItems[].attr_adj_config.status`|Not mapped|
|`header.lineItems[].attr_adj_config.messages[].type`|Not mapped|
|`header.lineItems[].attr_adj_config.messages[].code`|Not mapped|
|`header.lineItems[].attr_adj_config.messages[].message`|Not mapped|
|`header.lineItems[].attr_adj_config.messages[].showToUser`|Not mapped|
|`header.lineItems[].pricingAdjustments[].adjustment_type.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_value.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_amount.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_amount_total.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_description.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_sequence_id.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_matrix_type.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_basis.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].price_point.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].pricing_plan_step.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].rule_id.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].rule_condition.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_sys_id`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].adjustment_source`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].manual_adjustment_source`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].contributing_sold_product`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].contributing_line_item`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].pricingAdjustments[].running_price.value`|`txn.line.pricing.priceAdjustments`|
|`header.lineItems[].total_adjustment_amount[].pricePoint`|Not mapped|
|`header.lineItems[].total_adjustment_amount[].value`|`txn.line.pricing.adjustment.net`|
|`header.lineItems[].total_manual_adjustment`|`txn.line.pricing.adjustment.manual`|
|`header.lineItems[].delta_price_treatment`|Not mapped|
|`header.lineItems[].extended[].field`|Not mapped|
|`header.lineItems[].extended[].variable`|Not mapped|
|`header.lineItems[].extended[].type`|Not mapped|
|`header.lineItems[].extended[].value`|Not mapped|

## Settings

|Pricing response field|TXM field|
|----------------------|---------|
|`settings.pricing_context_id`|Not mapped|
|`settings.pricing_elements`|Not mapped|

**Parent Topic:**[Pricing Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/price-management-reference.md)

