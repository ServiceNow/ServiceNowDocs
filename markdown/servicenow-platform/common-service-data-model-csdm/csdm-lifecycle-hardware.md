---
title: Life cycle of tangible/physical CIs
description: The tangible/physical life-cycle states represent the overall life cycle of physical assets and CIs as related to their products. Tangible/physical assets are physical items that are stocked, for example computers, monitors, and keyboards. The stages and statuses for the tangible/physical life-cycle process are visible only in hardware-related tables in Asset Management and the CMDB.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle of tangible/physical CIs

The tangible/physical life-cycle states represent the overall life cycle of physical assets and CIs as related to their products. Tangible/physical assets are physical items that are stocked, for example computers, monitors, and keyboards. The stages and statuses for the tangible/physical life-cycle process are visible only in hardware-related tables in Asset Management and the CMDB.

## Life-cycle values for tangible/physical CIs

For definitions of the values in the diagram, see [Definitions of life-cycle values for tangible/physical CIs](../reference/csdm-lifecycle-df-tangible-physical.md).

![Relationships between CSDM stages and life cycle values.](../image/csdm-lifecycle-vp-tangible-physical.png)

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(tangible/physical, document and contract, location and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](foundation-domain.md).

## Examples of tangible/physical classes

View attributes, identification rules, and other important schema structures for the CMDB Computer \[cmdb\_ci\_computer\] class in [Hardware \[cmdb\_ci\_hardware\] class](../../configuration-management/concept/class-hardware.md).

-   **[Definitions of life-cycle values for tangible/physical CIs](../reference/csdm-lifecycle-df-tangible-physical.md)**  
The tangible/physical life-cycle states represent the overall life cycle of physical assets and CIs as related to their products. Tangible/physical assets are physical items that are stocked, for example computers, monitors, and keyboards. The stages and statuses for the tangible/physical life-cycle process are visible only in hardware-related tables in Asset Management and the CMDB.
-   **[Retiring a service instance can affect tangible/physical CIs](../reference/csdm-retire-srvc-inst-affects-hdw.md)**  
Because a service instance might depend on a hardware \(tangible/physical\) device that other service instances depend on, you must take care when retiring a service instance.
-   **[Tangible/physical tables in the CMDB](../reference/csdm-lifecy-tables-tang-physical.md)**  
List of tangible/physical tables.

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

**Related topics**  


[Definitions of life-cycle values for tangible/physical CIs](../reference/csdm-lifecycle-df-tangible-physical.md)

[Retiring a service instance can affect tangible/physical CIs](../reference/csdm-retire-srvc-inst-affects-hdw.md)

