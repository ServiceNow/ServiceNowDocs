---
title: Definitions of life-cycle values for location entities
description: The values for the location life-cycle process reflect the locations used by your organization and are visible only in the common data locations table.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Location life cycle, Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Definitions of life-cycle values for location entities

The values for the location life-cycle process reflect the locations used by your organization and are visible only in the common data locations table.

## Definitions of location life cycle stage and life cycle stage status values

![Relationships between CSDM stages and life cycle values.](../image/csdm-lifecycle-vp-location.png)

-   **Ideation life cycle stage**

    The location is in the initial planning and setup phase.

    -   **Chartered**: The location is approved for development, but no physical presence has yet been established.
    -   **Build**: The location is under construction, setup, or is being prepared for operational use.
-   **Operational life cycle stage**

    The location is active and in use for business operations.

    -   **Available**: The location is fully built and ready for use but currently unoccupied or not assigned for a specific function.
    -   **In Use**: The location is actively occupied and is being used for its intended purpose.
    -   **Pending Retirement**: The location is still operational but is scheduled for decommissioning or repurposing.
-   **End of Life life cycle stage**

    The location is no longer in active use and is being decommissioned.

    -   **Sold**: The location has been sold to another entity.
    -   **Lease Return**: A leased location has been returned to the owner or landlord after the lease period ended.
    -   **Obsolete**: The location is no longer viable for use due to physical deterioration, business strategy changes, or other constraints.

**Note:** The \[life\_cycle\_control\] table uses the type of CI \(tangible/physical, document and contract, location and so on\) to determine which *life cycle stage status* values are available for each *life cycle stage*.

For additional information on how you can benefit from implementing life-cycle value pairs for CMDB entities, see the ['Map existing status values to CSDM life-cycle value pairs' section in the 'Foundation domain' topic](../concept/foundation-domain.md).

**Parent Topic:**[Life cycle of location entities](../concept/csdm-lifecycle-location.md)

