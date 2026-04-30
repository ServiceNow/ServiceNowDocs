---
title: Location life cycle
description: The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The location life-cycle value pairs represent the overall life cycle of a location within common data.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CSDM reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Location life cycle

The CSDM framework provides standard fields and values that you can use to track the life cycle of an asset or a CI. The location life-cycle value pairs represent the overall life cycle of a location within common data.

## Life-cycle values for location

A life-cycle value pair is the combination life cycle stage and life cycle stage status values for a CI, asset, or IBI over the life cycle of a product instance. For example, a location CI in the **Operational** stage might change status over time from **In Use** to **Pending Retirement**. A different location CI in the **Operational** stage might go from the **Available** status directly to **Pending Retirement** status without ever having been in the **In Use** status.

![Location life cycle process: pipeline, operational, and end of life.](../image/csdm-lifecycle-location.png)

The stage and status values for locations are visible only in the common data locations table.

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(hardware, document, logical and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](foundation-domain.md).

## CSDM videos in the ServiceNow Community

[Playlist of all CSDM videos](https://www.youtube.com/playlist?list=PLkGSnjw5y2U7QNr9jL6TAgwQvYBI_LEtK)

**Parent Topic:**[CSDM reference](csdm-content-frame-reference.md)

