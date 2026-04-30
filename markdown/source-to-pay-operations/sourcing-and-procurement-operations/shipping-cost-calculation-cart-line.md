---
title: Shipping cost calculation in cart line table
description: If the item in your cart is a good, a cart line shipping estimate prioritization logic is used to calculate the estimated shipping cost. If the item in your cart is a service, the estimated shipping cost shows as 0.0 in your currency.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Shipping cost calculations, Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Shipping cost calculation in cart line table

If the item in your cart is a good, a cart line shipping estimate prioritization logic is used to calculate the estimated shipping cost. If the item in your cart is a service, the estimated shipping cost shows as 0.0 in your currency.

The cart line for each item is updated with the shipping estimate.

1.  Use the product level shipping estimate percentage to calculate shipping, provided the sn\_shop.shipping.estimate.inclusion property is set to true:
    -   Pull the estimated shipping as percentage value from the supplier product record.
    -   Calculate shipping as \[Estimated Shipping as Percentage\] \* \[Quantity\] \* \[Negotiated Unit Price\].
2.  If 1 is null, use the supplier level shipping estimate percentage to calculate shipping, provided the sn\_shop.shipping.estimate.inclusion property is set to true:
    -   Pull the estimated shipping as percentage value from the supplier record.
    -   Calculate shipping as \[Estimated Shipping as Percentage\] \* \[Quantity\] \* \[Negotiated Unit Price\].
3.  If both 1 and 2 are null, use the default shipping estimate percentage to calculate shipping, provided the sn\_shop.shipping.estimate.inclusion property is set to true:
    -   Pull the estimated shipping as percentage value from the system properties.
    -   Calculate shipping as \[Estimated Shipping as Percentage\] \* \[Quantity\] \* \[Negotiated Unit Price\].
4.  If 1, 2, and 3 are all null, or the sn\_shop.shipping.estimate.inclusion property is set to false, shipping estimate is shown as Undetermined.

**Parent Topic:**[Shipping cost calculations](shipping-cost-calculations.md)

