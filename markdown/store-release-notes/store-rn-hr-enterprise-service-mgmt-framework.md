---
title: Enterprise Service Management Integrations Framework release notes
description: Version history for the Enterprise Service Management Integrations Framework integrations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-enterprise-service-mgmt-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - HR Service Delivery release notes, ServiceNow Store - Employee Service Management release notes, ServiceNow Store release notes]
---

# Enterprise Service Management Integrations Framework release notes

Version history for the Enterprise Service Management Integrations Framework integrations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.9.2 - June 2026**
    -   Changed: Access control lists \(ACLs\) have been updated to align with current platform security standards.
    -   Fixed: The sn\_hr\_integr\_fw.admin role hierarchy did not resolve as expected due to incorrect role containment.
-   **Version 3.8.2 - August 2025**
    -   Problem: The RCA privilege status was incorrectly reported as 0 instead of the expected 2 for the "Pulled Integration To-do" table sourced from the "My Items" widget, causing test failures in RCAPrivilegesIT.testRCAPrivilegesStatus.
        -   New: Introduced validation logic to ensure real RCA types are correctly flagged and shipped from the "My Items" widget.
        -   Changed: Adjusted the RCA privilege evaluation to align with expected status values during integration.
        -   Fixed: Corrected the RCA privilege status mapping to prevent false negatives in automated test validations.
        -   Removed: Eliminated outdated logic that misclassified RCA entries during transformation.
    -   Problem: The RCA privilege status was incorrectly set to "Requested" for RCAs sourced from the "Employee Center Header" widget, targeting the "Enterprise Service Management Integrations Framework" table, leading to test failures in RCAPrivilegesIT.testRCAPrivilegesStatus.
        -   New: Added support for validating RCA privileges from the "Employee Center Header" widget source.
        -   Changed: Updated the privilege evaluation logic to correctly interpret widget-to-table RCA mappings.
        -   Fixed: Resolved incorrect status assignment by aligning privilege checks with the RCA inclusion list.
        -   Removed: Removed legacy privilege handling that conflicted with the new RCA source-target structure.
-   **Version 3.8.1 - February 2025**
    -   Contains common components for integrating your ServiceNow applications with third-party systems.
    -   The framework leverages the Flow Designer capability to communicate with external instances and third-party systems.
-   **Version 3.7.2 - November 2024**

    Bug fixes.

-   **Version 3.7.1 - August 2024**

    Fixed minor bugs/internal observation.

-   **Version 3.7.0 - May 2024**
    -   New:
        -   Common components used to integrate your ServiceNow applications with third-party systems.
        -   Leveraging the flow-designer capability to communicate with external instances and third-party systems.
-   **Version 3.6.0 - August 2023**

    This version delivers to-do filters such as overdue, due soon, approvals and priority for Enterprise Service Management Integrations Framework.

-   **Version 3.5.0 - May 2023**

    New: The todo\_inbound table has been updated to support external approvals.

-   **Version 3.4.0 - February 2023**
    -   New: Included fixes to support usage of HR Mobile based on features of Now Mobile. Mobile list card views and Mobile input form screens have been upgraded.
        -   A script action reverts old card views with new card views. If there are customisations done on legacy cards, the script retains the legacy cards and does not replace them with new cards.
        -   A script action inactivates new function instances if customisations are done on legacy function instances or its related records. If no customisations are done, then existing function instances will be inactivated.
-   **Version 3.3.11 - November 2022**

    Fixes related to Employee terminated date handling.

-   **Version 3.3.10 - October 2022**

    Fixed: Includes fixes for SAP SuccessFactors

-   **Version 3.3.9 - September 2022**

    Support for SAP SuccessFactors integration with HRSD.

-   **Version 3.3.8 - June 2022**
    -   Fixed:
        -   RCA error when accessing To-do page
        -   Fix for Process External Interface - State is not populated
-   **Version 3.3.6 - April 2022**
    -   Fixed:
        -   Modification to Employee Number
        -   Refactoring in onBefore script of HR profile
        -   Update to User derivation to be from HR profile's table
-   **Version 3.3.5 - February 2022**

    Fixed: Fix for Primary job is not synced with HR Profile when Job active is false for inactive workers


**Parent Topic:**[ServiceNow Store - HR Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-hr.md)

