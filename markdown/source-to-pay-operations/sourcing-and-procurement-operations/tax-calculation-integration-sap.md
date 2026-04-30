---
title: Tax calculation integration with SAP
description: SAP's tax engine API consumes necessary parameters from the tax calculation generic API to provide tax estimates.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Tax calculations, Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Tax calculation integration with SAP

SAP's tax engine API consumes necessary parameters from the tax calculation generic API to provide tax estimates.

|Parameter|ServiceNow Field|SAP Field|
|---------|----------------|---------|
|Ship to|Delivery Location|Delivery Address Number|
|Date|System Date|Tax Posting Date|
|Quantity|Purchase Quantity|Quantity|
|Net price|Total Line Amount|Net Amount|
|Ship from|Street Address, City, State, County, Zip, Country, Region|Shipping Address|
|Vendor name|Legal Name|Vendor Code|
|Material/Material group|Model Category|Material/Material Group|
|Unit of measure|Unit|Base Unit of Measure|
|Entity|Entity|Company Code|

The tax estimates are consumed by ServiceNow and updated in the **Estimated Tax** field on the cart line.

**Parent Topic:**[Tax calculations](tax-calculations.md)

