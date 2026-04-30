---
title: Document life cycle
description: The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The document life-cycle value pairs represent the overall life cycle of document assets \(contracts\) and CIs \(business process\) as related to their products.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Document life cycle

The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The document life-cycle value pairs represent the overall life cycle of document assets \(contracts\) and CIs \(business process\) as related to their products.

## Life-cycle values for documents

A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. For example, a document CI in the **Operational** stage might change status over time from **In Use** to **Published** to **Pending Retirement**. A different document CI in the **Operational** stage might go from the **In Use** status directly to **Pending Retirement** status without ever having been in the **Published** status.

![Document life-cycle process: pipeline, operational, and end of life.](../image/csdm-lifecycle-document.png)

The life-cycle value pairs for documents are visible only in tables related to documents in Contract Management and the CMDB.

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(hardware, document, logical and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](foundation-domain.md).

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

