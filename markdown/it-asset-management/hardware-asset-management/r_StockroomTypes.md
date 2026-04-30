---
title: Stockroom types
description: Stockroom types are categories of stockrooms.
locale: en-US
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Hardware Asset Management, IT Asset Management]
---

# Stockroom types

Stockroom types are categories of stockrooms.

The stockroom type has two significant characteristics.

-   **Priority**: Order of stockrooms the parts should be sourced from. For example, if a personal stockroom \(priority 2\) contains the required part, the personal stockroom receives priority over the Central Stockroom \(priority 7\) because the part in the personal stockroom doesn’t require delivery.
-   **Shipment Required**: Informs the system if a transfer order must be created when the part is sourced from a stockroom of the given type. For example, a part in a personal stockroom doesn’t require shipment, so no transfer order is needed.

|Value|Name|Priority|Shipment Required|Description|Comment|
|-----|----|--------|-----------------|-----------|-------|
|on\_site|On Site|1|False|Stockroom at the customer site.|Close to the users and doesn’t require shipping.|
|field\_agent|Field Agent|2|False|Virtual, personal stockroom linked with a field service agent \(FSA\) directly, used for delivery.|Used to indicate to the system that the part has been delivered and is with the FSA.|
|fsl|FSL|4|True|Forward Shipping Location.|Small stockrooms where the parts can typically be shipped via overnight delivery.|
|pudo|PUDO|5|True|Pick Up/Drop out location.|This type is sometimes called a by-box. Can be a postal box that can receive new and returned parts that are often near major customer sites.|
|stockroom|Warehouse|6|True| |A regional stockroom.|
|central\_stockroom|Central Warehouse|7|True| |A central stockroom, usually a large facility from which most parts are shipped.|

**Parent Topic:**[Hardware Asset Management reference](../../hardware-asset-management/concept/reference-hardware-asset-management.md)

