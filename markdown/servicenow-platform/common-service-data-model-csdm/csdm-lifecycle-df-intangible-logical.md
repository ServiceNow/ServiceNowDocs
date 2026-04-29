---
title: Definitions of life-cycle values for intangible/logical entities
description: The intangible/logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products. A logical or software asset includes items like applications, services, and licenses. The life cycle stage and life cycle stage status values of logical items are visible only in tables related to intangible/logical items in Asset Management and the CMDB.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Intangible/logical life cycle, Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Definitions of life-cycle values for intangible/logical entities

The intangible/logical life-cycle value pairs represent the overall life cycle of logical assets and CIs as related to their products. A logical or software asset includes items like applications, services, and licenses. The life cycle stage and life cycle stage status values of logical items are visible only in tables related to intangible/logical items in Asset Management and the CMDB.

## Definitions

![Relationships between CSDM stages and life cycle values.](../image/csdm-lifecycle-vp-intangible-logical.png)

-   **Ideation life cycle stage**

    In this stage, new software or service products are evaluated and tested before they are approved for use.

    -   **Under Evaluation**: The software is being assessed for business fit, licensing implications, and technical feasibility.
    -   **Pilot**: The software is deployed in a limited way to test its functionality and usability before full-scale implementation.
-   **Purchase life cycle stage**

    After the software is approved, the organization procures the necessary licenses or subscriptions.

    -   **On Order**: Licenses or software subscriptions have been purchased but are not yet available for use.
    -   **Preallocated**: Licenses are assigned to users or departments before they are officially deployed. 
-   **Inventory life cycle stage**

    The software licenses are now available for assignment and deployment.

    **Available**: The software licenses are ready for allocation but have not yet been assigned to a specific system or user.

-   **Design life cycle stage**

    For software development or major configurations, this phase defines the logical and architectural structure.

    -   **Design**: The logical architecture and system requirements are being defined.
    -   **Chartered**: A project is initiated to design or configure software solutions. 
    -   **Build**: The software is being developed, customized, or configured for deployment.
-   **Deploy life cycle stage**

    Software and services are prepared for operational use and are tested before full implementation.

    **Test**: The software is installed in a test environment for validation before production deployment.

-   **Operational life cycle stage**

    The software is actively in use by the organization.

    -   **In Use**: The software is deployed and functioning on production systems.
    -   **End of Support**: The software vendor or internal IT team no longer provide updates or technical support, but the software might still be in use.

        **Note:** A CI might be in the **Operational** stage, but might no longer be supported by the vendor or publisher or third party. That doesn’t mean, however, that it can be or should be retired.

    -   **Pending Retirement**: The software is scheduled for decommissioning but remains operational until a replacement is implemented.
-   **End of Operation life cycle stage**

    End of Operation is an intermediate stage between Operational and the next stage. Operations of the product have ended, but the product instance might transition to a new life cycle stage and life cycle status.

    **On Hold**: Operation of the asset is halted for one of the following reasons:

    -   Suspended: service, subscription, and so on.
    -   Blocked: credit card, account, and so on.
    -   Paused: subscription, lease, and so on.
-   **End of Life life cycle stage**

    The software is no longer in active use and is being decommissioned.

    -   **Retired**: The software is no longer used and its licenses might have been revoked or reassigned.
    -   **Obsolete**: The software is no longer relevant due to security risks, incompatibility, or technological advancements.

**Parent Topic:**[Life cycle of intangible/logical entities](../concept/csdm-lifecycle-logical.md)

