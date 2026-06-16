---
title: Hardware Asset Management release notes
description: Version history for the Hardware Asset Management application on the ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hardware-mgnt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - IT Asset Management release notes, ServiceNow Store release notes]
---

# Hardware Asset Management release notes

Version history for the Hardware Asset Management application on the ServiceNow®.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 15.0.2 - June 2026**

    Fixed an issue where clicking View records on the Important action card in the Hardware Asset Workspace returned a blank list instead of the expected results.

-   **Version 15.0.1 - May 2026**

    Defect fixes: Automated test failures.

-   **Version 15.0.0 - March 2026**
    -   Gain insight into the approximated life cycle dates for hardware and consumable products.
    -   Streamline inventory asset management with the expanded and efficient inventory auditing process.
    -   Streamline and improve the asset management process for retired assets with the expanded asset disposal workflow.
    -   Streamlined Advanced Shipment \(ASN\) import process with support for users with specific functional roles.
    -   Save time and effort by copying a model from the Content lookup portal to create a record in your ServiceNow instance.
-   **Version 14.0.1 - February 2026**

    In this version, the issue where resource counts were not deleted when all resource categories were opted out has been resolved.

-   **Version 14.0.0 - December 2025**
    -   This release resolves integration challenges between IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\) caused by differences in data models and user experiences.
    -   A new Asset Management Integration for Sourcing and Procurement Operations plugin \(com.snc.sn\_spend\_asset\) plugin provides SPO users with read-only access to Hardware Asset Management \(HAM\) shipment tables, improving visibility without impacting existing HAM, EAM, or SPO functionalities.
    -   These enhancements ensure smoother collaboration between ITAM and SPO processes while maintaining system integrity and performance.
-   **Version 13.0.0 - August 2025**
    -   Benefit from improved asset attestation features, including a guided attestation creation process, a mobile-friendly interface for confirming assets, and automated remediation tasks to address non-compliant assets.
    -   Achieve real-time tracking of assets that are in transit and maintain asset data accuracy by enabling employees to confirm receipt of assets through the Employee Center portal.
    -   Receive shipment assets at a stockroom from any workflow through the streamlined and unified receiving process.
    -   Track asset movement from the receiving bay to an aisle and space in the stockroom using the asset putaway task.
    -   Evaluate how effectively your assets are functioning and being used through reports based on asset key performance indicators in the Asset analytics view. Also, manage supply and demand in your stockrooms effectively with inventory demand reports.
-   **Version 12.1.1 - June 2025**

    Fixed: To prevent sensitive data leakage from range queries accessed by unauthenticated users, the following Access Control List \(ACL\) has been added: HAMP Success Activity \[sn\_hamp\_success\_activity\] table: Only users with the ham\_admin and asset roles can perform the query\_range operation on the Description, Short description, and Success goals columns.

-   **Version 12.1.0 - February 2025**

    New: Asset Attestation.

-   **Version 11.0.2 - October 2024**

    Fixed: Opt-in mechanism for ITSM-HAM integration is fixed for the mandatory validation around asset action using system properties.

-   **Version 11.0.1 - September 2024**
    -   Fixed:
        -   Uptake of custom licensing for users on old HAM SKU is provisioned.
        -   The issue of the Mobile Device resource category being opted out when upgrading from HAM versions 9.0.0 or 10.0.0 is fixed.
        -   The issue with the Asset incident frequency report filter condition in the Asset estate view of the Hardware Asset Workspace is fixed.
-   **Version 11.0.0 - August 2024**
    -   New:
        -   Asset picking with indoor maps
        -   Zero touch request
        -   Asset repair flow
-   **Version 10.1.1 - July 2024**

    Fixed: The licensing extension point implementation was made non-protected.

-   **Version 8.0.2 - July 2024**

    Fixed: Thenorm\_license\_opt\_in value on the hardware model is not set to "Y" after opting in the HAM resource categories.

-   **Version 10.1.0 - May 2024**
    -   New:
        -   Hardware Asset Management for Zero Touch Mobility
        -   Licensing support for new resource categories
-   **Version 10.0.1 - March 2024**

    In this version, minor issues related to the Total cost of ownership \(TCO\) feature are fixed.

-   **Version 10.0.0 - February 2024**
    -   This version includes the following features:
        -   Asset Total Cost of Ownership \(TCO\)
        -   Hardware Asset Management Maturity
        -   Asset Warranty integration with Lenovo
-   **Version 8.1.0 - November 2023**

    New: Indoor Mapping capability for Hardware Asset.

-   **Version 8.0.0 - August 2023**
    -   This version includes the following features:
        -   HAM Success Portal
        -   Zero Touch Asset Refresh flow
        -   HAM Content Expansion
        -   Advanced Inventory &amp; Distribution
        -   Stockroom Form Update
        -   Asset Integration - Shipping Carrier
-   **Version 5.1.1 - July 2023**

    In this release, Model normalization issues are fixed.

-   **Version 4.0.3 - July 2023**

    In this release, Model normalization issues are fixed.

-   **Version 7.1.0 - May 2023**

    The following fields are added to the Mobile section of the Hardware Asset form:

    -   Last enrolled
    -   Pre-enrollment ID
    -   Enrollment state
    -   Enrollment ID
    -   Ownership
    -   Enrollment name
    -   Platform
-   **Version 5.1.0 - May 2023**
    -   New:
        -   Following fields are added on Mobile section of Hardware Asset form:
            -   Last enrolled
            -   Pre-enrollment ID
            -   Enrollment state
            -   Enrollment ID
            -   Ownership
            -   Enrollment name
            -   Platform
-   **Version 5.0.2 - March 2023**

    Report View ACLs are enabled for out-of-box HAM reporting tables.

-   **Version 7.0.0 - February 2023**
    -   New: This version includes the following features:
        -   Asset donation
        -   Asset pallets
        -   Workspace support for procurement
-   **Version 5.0.1 - November 2022**

    This version includes exclusion of EAM Assets from HAM flows, as we will be supporting EAM assets through EAM store app.

-   **Version 5.0.0 - August 2022**

    The following new features are part of the Hardware Asset Management \(5.0.0\) release:

    -   Contract Renewal Workflow
    -   HAM Content Portal search
    -   HAM Guided setup
    New User Experience - Contract Management, Procurement - Sourcing support on workspace.

-   **Version 4.0.2 - March 2023**

    Report View ACLs are enabled for out-of-box HAM reporting tables.

-   **Version 4.0.1 - February 2022**

    New: New User Experience - Asset Estate, Inventory, Asset Operations, Model Management

-   **Version 3.0.3 - November 2021**

    Fixed: This version includes fixes for the Loaner Asset Reservation feature

-   **Version 3.0.2 - September 2021**
    -   Fixed:
        -   Bundle Asset
        -   Hardware Normalization
-   **Version 3.0.1 - August 2021**
    -   New: This version includes fixes for the following features:
        -   Asset Look up in Agent Mobile App
        -   Bundle Asset
        -   Asset Audit in Agent Mobile App
-   **Version 3.0.0 - July 2021**
    -   New:
        -   Perspective process workflows for Return Mercandise Authorization \(RMA\) and Asset Reservations
        -   Asset Health Dashboard with reports focused on health and compliance of hardware asset records
        -   Mobile device asset attributes
-   **Version 2.0.2 - March 2021**
    -   Fixed:
        -   HAM - Loaner Asset Request Flow ATF test.
        -   Bundle Asset form view.
        -   ASN - Import set stuck in loading when an empty ASN template is imported.
        -   ASN - Asset not created in Consumable table when Asset tracking strategy is set to Create consumable asset.
-   **Version 2.0.1 - January 2021**

    New: Hardware Asset Management v2.0.1 is new in the Quebec release. Refer to the Quebec release documentation for additional information.

-   **Version 1.0.2 - November 2020**

    Fixed: This version of the Hardware Asset Management app provides an update to fix the automated updates against an audited asset where the scanned location or stockroom does not match the record. The update occurs upon submitting of asset batch scanned using the Agent app.

-   **Version 1.0.1 - October 2020**

    New: Expanded license classes for Hardware Asset Management product licensing to include IP Router and IP Switch model categories.

-   **Version 1.0.0 - July 2020**
    -   New: Hardware Asset Management 1.0 is new in the Paris release
    -   Refer to Paris release documentation for additional information.

