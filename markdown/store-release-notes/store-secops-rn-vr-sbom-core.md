---
title: SBOM Core Response release notes
description: Version history for the Vulnerability Response SBOM Core application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-sbom-core.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# SBOM Core Response release notes

Version history for the Vulnerability Response SBOM Core application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.3.2 - June 2026**
    -   Fixed:
        -   SPDX entity-to-component relationships restored — An issue where the SPDX parser previously created relationships only from the explicit relationships block, so SPDX BOMs that rely on the package list to imply dependencies showed almost no "Depends on" data on the BOM entity record, for example, ~171 dependencies instead of the expected ~2500. The parser now performs an additional pass that creates an entity-to-component relationship for every non-root package, matching the existing CycloneDX behavior.
        -   Vendor SBOM upload errors  — Resolved errors raised during vendor SBOM uploads so SBOMs supplied by third parties can be ingested without manual intervention.
        -   VR BOM Entries deletion restored — The background-job configuration that drives VR BOM Entries deletion was packaged under a folder name that no longer matched the SBOM Sec Common plugin. The folder has been renamed so the background job is recognized again and BOM-entry deletion runs as expected.
        -   Localized failure messages — The CycloneDX parser's "failed components" message is now produced as complete translatable sentences with numbered parameters, so the message is fully translatable.
-   **Version 6.3.1 - April 2026**
    -   New:
        -   Automatic timeout handling for BOM records
            -   Implemented automatic timeout handling for BOM records that remain stuck in the processing state for more than an hour. The system now tracks processing metrics by populating processing\_startedtimestamp when BOM processing begins and calculating processing\_durationwhen processing completes, times out, encounters errors, or is skipped, providing better visibility into BOM processing performance and reliability.
    -   Fixed: An issue where BOM processing failures updated the queue record status but left the error message field empty or generic. Error reasons are now properly captured on BOM queue records, providing you with immediate visibility into failure causes without requiring you to analyze error logs.
-   **Version 6.2.2 - December 2025**
    -   Changed: Improved UI accessibility by rectifying heading hierarchy, updating the labels, and aligning components with the latest platform standards.
    -   Fixed
        -   Fixed CycloneDX v1.6 author parsing logic to ensure stable and compliant SBOM processing.
        -   Fixed SBOM import failures by rectifying the license-handling logic during SBOM processing.
-   **Version 6.1.1 - August 2025**
    -   New:
        -   Implemented caching improvements for frequently accessed data with optimized upsert operations for contacts, component relationships, BOM-component mappings, and license information.
        -   Added two new scheduled jobs: an hourly job to process components with non-empty unprocessed\_sbom\_data, parsing and storing the information in appropriate tables before clearing the field
        -   Enhanced BOM processing job that now handles all queued BOMs in a single execution instead of one at a time, significantly improving system throughput.
-   **Version 6.0.6 - May 2025**
    -   Fixed:
        -   Fixed issue with SBOM API upload throwing "Unsupported BOM format" error; SBOM files now upload successfully without content type issues.
        -   The CycloneDX parser is refactored to improve SBOM ingestion performance by reducing database transactions, implementing an LRU cache, and improving extensibility through modular parsing functions for different CycloneDX model properties.
-   **Version 6.0.3 - February 2025**
    -   New:
        -   Improvements to the Software Bill of Materials Workspace permit you to delete multiple BOM entity records and their related components from the Home \(landing\) page with bulk edit.
        -   Any Application Vulnerable Items \(AVIT\)s that are associated with the BOM entities you delete automatically transition to 'Closed'.
-   **Version 5.0.5 - December 2024**

    Minor fixes for this release.

-   **Version 5.0.4 - November 2024**
    -   New: SBOM parser and validation improvements for the SBOM file upload.
    -   Changed: Updates to the SBOM upload modal to include the "Business application" and "Product model" attributes.
-   **Version 4.0.4 - August 2024**
    -   New:
        -   Improvements to support SBOM files in CycloneDX format:
            -   Activate the \(sn\_sbom\_core.collect\_properties\) property to import information that is generally not supported.
            -   View imported component data for declared and concluded licenses for SBOM files in versions 1.4 and later of CycloneDX.
            -   SBOM parsing support is improved for the following CycloneDX versions and component types: Version 1.5 - Platform, Data, Device driver, Machine Learning model. Version 1.6 - Cryptographic.
            -   Use GitHub Actions in your GitHub environment to determine if SBOM files generated in your CI/CD \(continuous integration and continuous delivery/deployment\) pipelines have been successfully queued in your ServiceNow AI Platform instance.
-   **Version 3.0.3 - May 2024**
    -   New:
        -   Upload SBOM files for the CycloneDX and SPDX standards.
        -   XML and JSON formats are supported for CycloneDX for versions up to and including v1.4.
        -   JSON format is supported for SPDX for versions up to and including v2.3.
-   **Version 2.1.1 - February 2024**
    -   New:
        -   View the SBOM inventory in the SBOM Workspace.
        -   Component information displayed on the application vulnerable item \(AVIT\) record.
        -   PURL validation support.
-   **Version 2.0.2 - November 2023**
    -   New:
        -   Created the \[sn\_sbom\_pkg\_grp\] table for the Data Model.
            -   Package manager and name is the unique key for this table.
            -   Added ACLs on the table for the sn\_sbom\_dm.app\_read role.
            -   Records are created and updated by scripts, but you cannot create, write, or delete the data.
        -   Added a report view ACL with the sn\_sbom\_dm.app\_read role.
        -   Added a reference to the package group table on the BOM Component table.
        -   Updated the CycloneDX parser so it identifies the package group and populates its information into the \[sn\_sbom\_pkg\_grp\] table. For each component of the type, 'library' the parser:
            -   Determines and populates the package manager, name, and base PURL in the package group table.
            -   Updates the Package group reference on that component's record.
-   **Version 1.0.8 - September 2023**
    -   New: Added the BOM Entities related list on the component form. You can see all the BOM entities that the component is used in on this related list.
    -   Fixed: You can manually upload BOM documents as expected.
-   **Version 1.0.5 - August 2023**

    Initial release: SBOM Core helps organizations maintain the searchable inventory of all the open-source components used in their environment.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

