---
title: Definitions of life-cycle values for tangible/physical CIs
description: The tangible/physical life-cycle states represent the overall life cycle of physical assets and CIs as related to their products. Tangible/physical assets are physical items that are stocked, for example computers, monitors, and keyboards. The stages and statuses for the tangible/physical life-cycle process are visible only in hardware-related tables in Asset Management and the CMDB.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Tangible/physical life cycle, Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Definitions of life-cycle values for tangible/physical CIs

The tangible/physical life-cycle states represent the overall life cycle of physical assets and CIs as related to their products. Tangible/physical assets are physical items that are stocked, for example computers, monitors, and keyboards. The stages and statuses for the tangible/physical life-cycle process are visible only in hardware-related tables in Asset Management and the CMDB.

## Definitions of tangible/physical life cycle stage and life cycle stage status values

**Note:** The CI label tangible/physical includes and supersedes the "Hardware" label that had been used in earlier releases.

![Relationships between CSDM stages and life cycle values.](../image/csdm-lifecycle-vp-tangible-physical.png)

-   **Ideation life cycle stage**

    New tangible or physical models in this stage are being assessed for potential use in the organization.

    -   **Under Evaluation**: The model is being reviewed for compatibility, functionality, and business fit before approval. 
    -   **Pilot**: The model is in a limited deployment for real-world testing before broader adoption. 
-   **Purchase life cycle stage**

    After a tangible or physical model is approved, the organization proceeds with procurement.

    -   **On Order**: The asset has been ordered from a vendor but has not yet been received. 
    -   **Preallocated**: The asset is already assigned to a specific purpose or user before its arrival. 
-   **Inventory life cycle stage**

    The asset is received and stored in inventory before deployment.

    -   **Available**: The asset is in stock and is ready for deployment. 
    -   **Reserved**: The asset is set aside for a specific request but is not yet deployed. 
    -   **Preallocated**: The asset is assigned to a request but is not yet physically allocated. 
    -   **Pending Repair \(CI\)**: The asset is in stock but requires repairs before being usable such as on-site visit from manufacturer or RMA swap. 
    -   **Legal Hold \(CI\)**: The asset cannot be deployed due to legal restrictions or compliance reasons. 
    -   **Quarantine \(CI\)**: The asset is isolated due to potential security risks, failures, or non-compliance. 
-   **Deploy life cycle stage**

    The asset is prepared and moved to operational use.

    -   **In Stock**: The asset is stored and is designated for deployment, but is in the process of being prepared for deployment .
    -   **Reserved**: The asset is assigned to a user or department but has not been physically moved. 
    -   **Pending Transfer**: The asset is scheduled for relocation to another facility or user. 
    -   **In Transit**: The asset is currently being moved between locations. 
    -   **Test**: The asset has been identified as part of a deployment activity, has been built, and is ready for testing prior to operational usage .
-   **Operational life cycle stage**

    The asset is actively in use or is undergoing maintenance.

    -   **Pending Fulfillment**: The asset is put/placed into its operational environment/location but needs to be configured/provisioned before it can be used.
    -   **In Use**: The asset is deployed and functioning in a live environment. 
    -   **In Maintenance**: The asset is being serviced or is undergoing repairs while still considered operational. 
    -   **End of Support**: The asset has reached the end of vendor or internal support but is still in use. 
    -   **Pending Retirement**: The asset is still operational but is marked for decommissioning. 
-   **End of Operation life cycle stage**

    End of Operation is an intermediate stage between Operational and the next stage. Operation of the product have ended, but the product instance is transitioning to a new life cycle stage and life cycle stage status.

    -   **Pending Evaluation**: Non-operational intermediate status in which a product is evaluated to determine its next stage and stage status.
    -   **Pending Return**: Non-operational status before the asset is returned and/or the provider received the returned asset in an end of life stage: **RMA**, **Vendor Credit**, **Buyout** or **Lease Return**. 
    -   **In Transit**: Non-operational, transitional status to support repurposing the asset and/or true end-of-life.
    -   **Pending Resale**: Intermediate status prior to selling the asset to a third-party entity .
    -   **Pending Certificate**: Intermediate status prior to receiving a certificate of disposal.
    -   **Pending Disposal**: Intermediate status prior to the **Disposed** end of life stage.
    -   **Pending Donation**: Intermediate status prior to the **Donated** end of life stage.
    -   **On Hold**: Operation of the asset is halted for one of the following reasons:
        -   Suspended: service, subscription, and so on.
        -   Blocked: credit card, account, and so on.
        -   Paused: subscription, lease, and so on.
-   **Defective life cycle stage**

    Tangible or physical devices that have failed and require replacement or repair.

    -   **In Stock**: The defective asset is stored and is awaiting disposition. 
    -   **In Transit**: The defective asset is being shipped for return, repair, or disposal. 
-   **Missing life cycle stage**

    The asset is unaccounted for or stolen.

    -   **Lost**: The asset is missing and cannot be located. 
    -   **Stolen**: The asset has been confirmed as stolen. 
-   **End of Life life cycle stage**

    The asset is being decommissioned or disposed of.

    -   **Pending Disposal**: The asset is marked for disposal but has not yet been removed. 
    -   **In Transit**: The asset is being shipped to a disposal or return location. 
    -   **Pending Certificate**: The asset awaits official documentation for decommissioning or disposal. 
    -   **Disposed**: The asset has been discarded following proper procedures. 
    -   **Donated**: The asset has been given to a non-profit, employee, or other entity. 
    -   **RMA**: The asset is returned to the vendor for replacement or repair under warranty. 
    -   **Sold**: The asset has been sold as part of asset liquidation. 
    -   **Vendor Credit**: The asset was returned to the vendor for a credit instead of replacement. 
    -   **Buyout**: The asset was leased and has been purchased instead of returned. 
    -   **Lease Return**: The leased asset has been returned to the vendor at the end of its lease period.

**Parent Topic:**[Life cycle of tangible/physical CIs](../concept/csdm-lifecycle-hardware.md)

