---
title: Common Service Delivery release notes
description: Version history for the Common Service Delivery application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-psm-service-delivery-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Sourcing and Procurement Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Common Service Delivery release notes

Version history for the Common Service Delivery application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 14.0.0 - June 2026 \(Australia\)**

    Changed: Remediated non‑Glide Cobalt Raven ACLs in product code \(DIRS0000421\).

-   **Version 11.6.1 - June 2026 \(Zurich\)**

    New: AI‑driven user compliance tracking for Source‑to‑Pay and Finance Operations SKUs: Admins can now track user compliance using scripted definitions \(DEFNs\). Scripted DEFNs are implemented to count users for Source‑to‑Pay Operations Foundation, Source‑to‑Pay Operations Prime, Finance Operations Foundation, and Finance Operations Prime SKUs. The solution leverages existing scripted DEFNs with updated application mappings aligned to the relevant SKUs, enabling accurate user metering across both top‑level and child applications.

-   **Version 9.12.1 - June 2026**

    New: AI‑driven user compliance tracking for Source‑to‑Pay and Finance Operations SKUs: Admins can now track user compliance using scripted definitions \(DEFNs\). Scripted DEFNs are implemented to count users for Source‑to‑Pay Operations Foundation, Source‑to‑Pay Operations Prime, Finance Operations Foundation, and Finance Operations Prime SKUs. The solution leverages existing scripted DEFNs with updated application mappings aligned to the relevant SKUs, enabling accurate user metering across both top‑level and child applications.

-   **Version 11.4.0 - March 2026 \(Zurich\)**
    -   New: Enabled requestors to enter decimal quantities for service items when editing purchase requisitions or purchase orders in Shopping Hub or Employee Center, with configurable unit‑of‑measure support. Unit‑of‑measure decimal support is configurable through a decision table. Admins must update the Unit of Measure Decimal support decision table and set Support decimal quantity to true for the required units.
    -   Changed: Improved interaction with asset management and sourcing and procurement integration by simplifying swimlane text, enhancing no‑price items, redirecting submissions to ITAM PO tables, and adding notifications.
-   **Version 9.10.0 - March 2026**
    -   New: Enabled requestors to enter decimal quantities for service items when editing purchase requisitions or purchase orders in Shopping Hub or Employee Center, with configurable unit‑of‑measure support. Unit‑of‑measure decimal support is configurable through a decision table. Admins must update the Unit of Measure Decimal support decision table and set Support decimal quantity to true for the required units.
    -   Changed: Improved interaction with asset management and sourcing and procurement integration by simplifying swimlane text, enhancing no‑price items, redirecting submissions to ITAM PO tables, and adding notifications.
-   **Version 11.0.1 - December 2025 \(Zurich\)**

    New: Introduced a new Procurement Exception table as the parent for the Purchase Order Exception table. The Procurement Exception table stores all exception-related data for Procurement functionalities.

-   **Version 9.9.3 - December 2025 \(Yokohama\)**

    New: Introduced a new Procurement Exception table as the parent for the Purchase Order Exception table. The Procurement Exception table stores all exception-related data for Procurement functionalities.

-   **Version 10.3.0 - October 2025**

    New: Updated telemetry definitions to include additional roles.

-   **Version 9.9.0 - October 2025**

    New: Updated telemetry definitions to include additional roles.

-   **Version 9.6.5 - September 2025**

    Minor fixes.

-   **Version 10.0.0 - August 2025**

    New: Added a new capability for Case Resolution Acceptance Workflow. This improvement provides greater transparency and control over case resolution by involving the requestor in the final stage of the case lifecycle.

-   **Version 9.6.4 - May 2025**

    Minor fixes.

-   **Version 9.6.0 - February 2025**

    Minor bug fixes.

-   **Version 9.3.0 - November 2024**

    Updated scripted definitions and evaluated sandbox access for client-callable script.

-   **Version 9.1.5 - August 2024**

    Minor fixes.

-   **Version 9.1.1 - June 2024**
    -   Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.
    -   Defect fixes.
-   **Version 7.1.0 - June 2024 \(Vancouver\)**

    Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.

-   **Version 5.3.1 - June 2024 \(Utah\)**

    Starting with the June 2024 release, the legacy framework to integrate with ERPs is being removed, and will no longer be installed on new instances.

-   **Version 9.0.0 - May 2024**
    -   New: Introduced new actions and user pages to support Supplier Lifecycle Operations task management features.
    -   Changed: Minor fixes.
-   **Version 8.2.2 - March 2024**
    -   New:
        -   Introduced a Related DDR field to track DDR records.
        -   Configured all the respective activities for the due diligence playbook.
-   **Version 8.0.0 - February 2024**
    -   Changed:
        -   To provide alignment between all Source-to-Pay \(S2P\) products and expose more commonly used data points to the end user, the Supplier field has been rescoped to the Service Task \(sn\_spend\_sdc\_service\_task\) table. With this, all tables extending the Service Task table can pull in the Supplier field for a better task experience. Note: Existing customers will see the Supplier field deprecated from the Supplier Task table and made available in the Service Task table through a fixed script.
        -   Fulfillers can now assign procurement tasks with specific action types to an employee or shopper. The supported action types are Submit Form, Sign a document, and Upload a document. This helps shoppers understand what is expected of them to complete the task. Note: There is no impact on existing customers for tasks that are already created, and they will find these new changes in effect with the upgrade.
        -   Fulfillers can now see the integration error tasks that have been generated as part of the new integration framework structure.
-   **Version 7.0.4 - December 2023 \(Vancouver\)**

    Minor fixes.

-   **Version 7.0.1 - November 2023**

    New: Fulfillers can now assign a procurement task with an action type to an employee or shopper. The action types supported are Watch Video, View Link, and Mark Complete. This feature guides the shopper with what is expected from them to complete the task. Note: There is no impact on existing customers for any tasks already created, and they will find these new changes in effect with this upgrade.

-   **Version 6.0.0 - August 2023**

    Changed: Some of the existing ACLs were evaluated and rectified to ensure that the roles have the right level of access to the tables, that is, requester role versus fulfiller role. Note: This is a backend change and has no customer impact.

-   **Version 5.2.1 - May 2023**

    Changed: Renamed this application to Common Service Delivery. This application was formerly named Service Delivery Common.

-   **Version 5.1.0 - February 2023**

    Changed: Updated a fulfiller's ability to create new case records with case types which extend the Service Delivery Common parent table.

    **Note:** Existing customers will be impacted by this change, allowing them to create both supplier and procurement cases.

-   **Version 5.0.0 - November 2022**

    Minor fixes.

-   **Version 4.0.2 - August 2022**

    Minor fixes.

-   **Version 4.0.1 - May 2022**

    Minor fixes.

-   **Version 3.0.1 - February 2022**

    Service Delivery Common \(SDC\) is a base application with a request and task workflow framework. It provides a standard framework for Procurement Case Management.


