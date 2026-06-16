---
title: Data Model for SBOM release notes
description: Version history for the Vulnerability Response Data Model for SBOM application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-vr-data-model-SBOM.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Data Model for SBOM release notes

Version history for the Vulnerability Response Data Model for SBOM application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.2.4 - June 2026**
    -   The following enhancements and changes support internal security directives:
        -   Updates for the SBOM Data Model tables to align with ServiceNow Platform Security guidance.
        -   Read-only dictionary fields for SBOM Data Model tables.
        -   Renamed fix script to a per-plugin name to avoid update-set conflicts with sibling Security Operations plugins.
-   **Version 4.2.2 - April 2026**
    -   New:
        -   Added "Timeout" status option to the BOM document status field to help you better track BOMs that exceed their processing time limits.
        -   Introduced new tracking fields on BOM document records, including processing\_started\(timestamp when processing begins\) and processing\_duration\(total time spent in processing\), enabling you to better monitor and analyze BOM processing workflows.
-   **Version 4.2.1 - December 2025**
    -   Fixed:
        -   Fixed an issue where the Activity tab in SBOM License records failed to persist historical state changes.
        -   Enabled the “Depends on” related list for intermediate SBOM entities and removed duplicate active filters for accurate dependency navigation.
-   **Version 4.1.1 - August 2025**

    New:Added new indexes to improve query performance on key tables: unique indexes for contact information \(phone/email/name\), build-component relationships, component dependencies, external references, and component hashes. Enhanced the sn\_sbom\_component table with two new fields: unprocessed\_sbom\_data to store non-critical attributes as JSON for asynchronous processing, and hash\_sha256 for direct storage of the component's SHA-256 hash value.

-   **Version 4.0.0 - February 2025**

    Improvements to support deleting BOM entity records and their related components from the Software Bill of Materials Workspace with bulk edit.

-   **Version 3.0.5 - December 2024**

    Fixed: Minor fix for this release.

-   **Version 3.0.4 - November 2024**

    New: Data model improvements to support the License administration module.

-   **Version 2.0.2 - August 2024**

    New: Table improvements to support new features in SBOM Response and SBOM Core.

-   **Version 1.4.3 - May 2024**

    New: Data model and framework enhancements to support DevOps use cases that require unique SBOMs for the multiple builds of a BOM Entity.

-   **Version 1.3.1 - February 2024**

    Updated data model to support PURL validation and author of the BOM document.

-   **Version 1.1.2 - November 2023**
    -   Changed:
        -   Added Report View ACL to the \[sn\_sbom\_m2m\_bom\_comptable\] table.
        -   Added New Roles and ACL to the \[sn\_sbom\_doc\] table.
-   **Version 1.0.4 - September 2023**

    New: Display name is a new field on the BOM Component table. The Display name field uses the name and version as the displayed value of a component.

-   **Version 1.0.3 - August 2023**

    Initial release: This application includes the tables, ACLs, and roles that are required to upload, parse, and ingest SBOM data.


**Parent Topic:**[ServiceNow Store - Vulnerability Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-vr.md)

