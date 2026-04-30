---
title: Definitions of life-cycle values for product entities
description: The product life-cycle value pairs represent the overall life cycle of a product model, a specific version, or a product configuration. The life-cycle values for the product life-cycle process are visible only in Product \(Models\) tables.
locale: en-US
release: zurich
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Product life cycle, Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Definitions of life-cycle values for product entities

The product life-cycle value pairs represent the overall life cycle of a product model, a specific version, or a product configuration. The life-cycle values for the product life-cycle process are visible only in Product \(Models\) tables.

## Definitions of product life cycle stage and life cycle stage status values

![Relationships between CSDM stages and life cycle values.](../image/csdm-lifecycle-vp-product.png)

-   **Ideation life cycle stage**

    New product models to determine feasibility and potential adoption.

    -   **Under Evaluation**: The product is being assessed for business value, functionality, and technical viability. 
    -   **Pilot**: In a small-scale deployment, the product is being tested in a controlled environment before broader adoption. 
-   **Design life cycle stage**

    After a product is approved for development or configuration, its structure and features are defined.

    -   **Design**: The product is being architected, including defining specifications, features, and configurations. 
    -   **Chartered**: The product model has been formally approved for development or procurement. 
-   **Build &amp; Integrate life cycle stage**

    The product is being developed, tested, and prepared for operational deployment.

    -   **Build**: The product is being developed, covers the activities from code commit through compiled or packaged deliverables being ready for deployment to a lower \(non-production\) environment.
    -   **In Production**: Covers the final promotion and release of changes into the live, customer-facing environment, with all required governance.
-   **Operational life cycle stage**

    The product is actively available and used within the organization.

    -   **Available**: The product is fully developed and ready for procurement or deployment.
    -   **Pending Retirement**: The product is still operational but is scheduled to be phased out.
    -   **End of Support**: The product is no longer receiving updates, maintenance, or vendor support.

        **Note:** gggA CI might be in the **Operational** stage, but might no longer be supported by the vendor or publisher or third-party. That doesn’t mean, however, that it can be or should be retired.

-   **End of Life life cycle stage**

    The product is no longer in active use and is being retired.

    -   **Retired**: The product is no longer available for new purchases or deployments but may still exist in limited use.
    -   **Obsolete**: The product is completely phased out and is no longer supported or used.

**Parent Topic:**[Life cycle of product entities](../concept/csdm-lifecycle-product.md)

