---
title: Life cycle value definitions for location entities
description: The values for the location life-cycle process reflect the locations used by your organization and are visible only in the common data locations table.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-05-07"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle value definitions for location entities

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

**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

