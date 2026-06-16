---
title: Service Builder release notes
description: Version history for the Service Builder application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-service-builder.html
release: store
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Service Builder release notes

Version history for the Service Builder application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 202601.0.1 - March 2026 \(Zurich+\)**
    -   Fixed:
        -   PRB1961526 -The current user was being incorrectly added to the delegate related list on publish
        -   PRB1972256 - When publishing a service in service builder with asset tags, when deleting the DRAFT record, the published record would also get deleted because of a cascade delete rule on asset tags.
-   **Version 202601.0.0 - January 2026 \(Yokohama+\)**

    Updated version to fix the issue where newer versions weren't showing up in the store because of the version convention change.

-   **Version 3.6.1 - December 2025 \(Yokohama+\)**
    -   Changed: Security enhancements
    -   Fixed: PRB1939935 - Fixed an issue that could cause the Lifecycle status of an offering to update to 'none' in service builder.
-   **Version 202507.0.0 - August 2025**
    -   New: Renaming application service to service instance per updated CSDM naming conventions.
    -   Fixed:
        -   PRB1897752 - Removed outdated lifecycle business rules. In particular ones required operational status to only more forward or required parent services to be operational.
        -   PRB1818579 - fixed an issue where the "Create New Business/Technology management Service Button" wasn't showing up for the service admin role.
-   **Version 3.5.0 - May 2025**
    -   New: Added Managed by, Department, and Company fields to the business service, technical service, and service offering flows to help with DORA compliance.
    -   Fixed
        -   PRB1840840 - Fixed an issue where service\_classification was getting a non-value for non English installs.
        -   PRB1844774 - Fixed an issue where the 'internal and external' option for the 'consumer' field was showing up. This option is not appropriate for offerings.
        -   PRB1872006 - Fixed an issue where the 'managed by' field wasn't getting saved when editing a Draft service.
-   **Version 3.3.0 - February 2025**

    Fixed PRB1790283: Fixed a case where service offerings that are in the 'waiting for approval' state don't show up in service builder, which made it seem like the service offerings never got created.

-   **Version 3.2.6 - December 2024**

    Fixed: PRB1804842 - Error when submitting service: Status can only move forward to retiring or retired or obsolete from operational.

-   **Version 3.2.2 - November 2024**

    Fixed: Accessibility issues across Service Builder.

-   **Version 3.1.3 - August 2024**
    -   New: Added the word \[DRAFT\] before the names of service and offering draft records to easily distinguish them from published items.
    -   Fixed: Fixed a defect where duplicate service offerings were causing a business rule to fire that prevented a draft offering to be successfully published.
-   **Version 3.0.3 - February 2024**
    -   New: Cancel check out of a service or offering. When viewing a service or offering in Service Builder, click the Cancel button to cancel the check out of the service and/or offering and any changes you made. This action deletes the draft version and reverts the service or offering to its original state.
    -   Changed:
        -   Service Builder now uses the standard app shell and will not open in a new tab.
        -   View Service Builder in the Next Experience theme.
-   **Version 2.2.2 - August 2023**
    -   New:
        -   New approval process for services and service offerings
            -   Improved checkout experience to edit services and offerings. Check out a service or a single child offering one at a time. When you check out the service, you don't have to check out all its child offerings.
            -   Use updated fields, tooltips, and guidance text to help you to:
                -   Define service teams for offerings.
                -   Define the technical service relationships to application services.
    -   Fixed:
        -   Fixed an issue where when publishing a service with a very large number of DRAFT offerings, the publish would time out and offerings could be lost.
        -   Fixed an 'internal server error \(500\)' that could happen when viewing the list of services in certain cases.
-   **Version 2.1.4 - February 2023**
    -   Changed:
        -   Reverse the relationship on business service to business capability relationship
        -   Make Service Builder and its related components as part of Shared Platform Capability and should not require any ITSM license starting Utah and this release
        -   Removed com.snc.sla.contract2 explicit plugin dependency, installing the Service Portfolio Management depenecy should install the com.snc.sla.contract2 plugin
    -   Fixed:
        -   Documentation link goes to correct release
        -   When using Service Builder to edit a Service Offering record, 'Selected groups' was not getting updated/saved resulting in data loss
-   **Version 2.0.7 - July 2022**

    Fixed: Fixed the KPI group mappings in Service Builder when Digital Portfolio Management is enabled.

-   **Version 2.0.6 - May 2022**

    Changed: The Service Builder application route \(in the URL\) changed to now/builder to better integrate with the DPM 2.1 Workspace application route \(which changed to now/dpm\).

-   **Version 1.1.3 - April 2022**

    Changed: Service Level Management - Contract Management Integration - com.snc.sla.contract2 was added as a dependency for Service Builder.

-   **Version 2.0.5 - March 2022**

    Minor fixes.

-   **Version 1.1.2 - February 2022**

    New: Users are allowed to add KPIs to their services and offerings

-   **Version 1.0.0 - September 2021**

    Use Service Builder to create services and their corresponding offerings quickly and easily in a guided, step-by-step flow. Helpful hints and descriptions explain the critical fields and values, and their purposes.


