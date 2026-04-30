---
title: Product life cycle
description: The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The product life-cycle value pairs represent the overall life cycle of a product model, a specific version, or a product configuration.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Product life cycle

The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The product life-cycle value pairs represent the overall life cycle of a product model, a specific version, or a product configuration.

## Life-cycle value pairs for products

A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. For example, a product CI in the **Operational** stage might change status over time from **Available** to **Pending Retirement** to **End of Support**. A different product CI in the **Operational** stage might go from the **Available** status directly to the **End of Support** status without ever having been in the **Pending Retirement** status.

![Product life cycle process: pipeline, design, operational, and end of life.](../image/csdm-lifecycle-product.png)

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(hardware, document, logical and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

For additional details on products, see [Products and product models](foundation-domain.md#section-product-models).

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](foundation-domain.md).

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

