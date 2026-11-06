---
title: MACD for Product Inventory
description: Move, Add, Change, Disconnect \(MACD\) for Product Inventory \(PI\) enables the Advanced Configurator to manage provisioned product instances during a change flow. The configurator handles PI records differently based on the product offer type and whether pricing is enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/macd\_product\_inventory.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Explore, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# MACD for Product Inventory

Move, Add, Change, Disconnect \(MACD\) for Product Inventory \(PI\) enables the Advanced Configurator to manage provisioned product instances during a change flow. The configurator handles PI records differently based on the product offer type and whether pricing is enabled.

## MACD for Product Inventory

The default fulfillment flows create PI records during order decomposition; each record starts with a status of **Installation Pending**. After fulfillment completes without fallout, the status changes to **Active**.

The system property **sn\_ind\_tmt\_orm.enable\_prod\_invt\_for\_order\_management** controls whether PI records or Sold Product records are created during order fulfillment. When set to **true**, the system creates PI records.

When a product offer is associated with a specification or specification hierarchy, the system creates one PI record for each unit. Each record has a quantity of 1 when the ordered quantity is greater than 1. For example, if a product offer is ordered with a quantity of 5, fulfillment creates 5 PI records. The Advanced Configurator handles these multiple PI records correctly during MACD.

## Sold Product vs. Product Inventory

A Sold Product \[sn\_install\_base\_sold\_product\] is the commercial record of a product or service sold to a customer. It represents the customer's entitlement or subscription. A PI record extends Sold Product to add technical provisioning details: what was delivered, in what configuration, and how external systems reference it for MACD.

PI records include additional fields not present on Sold Product records:

-   External ID \(**sn\_prd\_invt\_external\_id**\)
-   Location fields
-   Overridden states
-   Inventory relationships

## PI record behavior by offer type

The Advanced Configurator loads PI records during MACD based on the product offer type. Each PI record always loads as a separate instance with a quantity of 1. The table that follows describes the supported operations for each offer type.

|Product offer type|How PI records load|Supported operations|
|------------------|-------------------|--------------------|
|Simple offer with specification or specification hierarchy|Each PI record loads as a separate instance with quantity 1.|Add an instance, disconnect an instance, duplicate an instance. Each instance always has a quantity of 1. Quantity split and per-instance quantity update aren't supported.|
|Configurable offer with specification \(offer hierarchy with matching specification hierarchy\)|Each PI record loads as a separate instance with quantity 1.|Add an instance, disconnect an instance, duplicate an instance. All operations are subject to cardinality rules.|

## Multi-instance Sold Product records

When a product offer has no associated specification, the system creates Sold Product records instead of PI records. The behavior during MACD depends on whether multiple configurations are enabled on the product offer.

Multiple configurations enabled.

During a new order, you can create more than one configuration of the same child offer under a parent offer. Each configuration instance can have a quantity greater than 1 and its own attribute values. For example:

-   Configuration 1: child offer instance with quantity 2, bandwidth = 100 Mbps
-   Configuration 2: child offer instance with quantity 3, bandwidth = 200 Mbps

During MACD, each configuration is managed as a separate instance. You can duplicate, split, update the quantity, or disconnect each configuration within cardinality limits.

Multiple configurations turned off.

Only one configuration with a quantity of 1 or greater is supported. During MACD, only one configuration is supported and the quantity can be updated.

## Line types and line steps for PI MACD

Each change made during a PI MACD session produces a transaction line with a specific line type and line step. The table that follows shows the expected values.

|Change|Line type|Line action|
|------|---------|-----------|
|Added a product offering or specification instance|**New**|**Add**|
|Removed a product offering or specification instance|**Cancel**|**Disconnect**|
|Changed a configuration attribute|**Amend**|**Change**|
|Increased quantity \(pricing enabled\)|**New**|**Add**|
|Decreased quantity \(pricing enabled\)|**Cancel**|**Disconnect**|

## PI MACD flow behaviors

-   **Cancel and disconnect in change flows**

    In PI flows, contract dates don't carry the same meaning they do in Sold Product flows. The fulfillment process controls when changes take effect. The configurator submits removed PI lines with a **Cancel** line type and **Disconnect** line step. The line step is not overwritten to **Change** for PI lines.

-   **Line splitting**

    Line splits don't occur in PI MACD flows. This differs from MACD flows for Sold Products.

-   **Quantity increase and CBOM lines**

    When a PI instance is added, a single bill of materials \(BOM\) line with a summary quantity is set to multiple composite BOM lines. The composite bill of materials \(CBOM\) displays a summary line for that unit. When a PI instance is disconnected, the system removes the corresponding CBOM summary line.


