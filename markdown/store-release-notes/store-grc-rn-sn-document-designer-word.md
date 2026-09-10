---
title: ServiceNow Document Designer with Word release notes
description: Version history for the ServiceNow Document Designer with Word application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-sn-document-designer-word.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance version history release notes, ServiceNow Store version history release notes]
---

# ServiceNow Document Designer with Word release notes

Version history for the ServiceNow Document Designer with Word application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 23.0.3 - September 2026 \(Brazil\)**
    -   New:
        -   Scripted HTML column type for document designer
            -   Authors can now create data columns that return HTML through scripts, enabling rich formatting and embedded images within repeater and table iterations. Scripted HTML columns are available in the Data Column form and render formatted content in generated documents.
    -   Changed
        -   Enhanced support for scripted HTML data columns
            -   Report generation now correctly handles special characters in HTML fields, ensuring successful output and proper character escaping.
-   **Version 22.3.2 - June 2026 \(Australia\)**
    -   Changed:
        -   Consolidated Document Designer plugin
            -   Manifest changes, backend logic updates, and repeater configuration adjustments to support the consolidation of the O365 and Document Designer add-ins into a unified Document Designer plugin with new business domain support.
        -   This release includes security enhancements that strengthen access controls across the application.
    -   Fixed:
        -   Office Add-in manifest corruption
            -   Fixed an issue where the sn\_office\_control for Create Claim was corrupting the Office Add-in manifest by duplicating the ExtensionPoint block.
-   **Version 21.1.3 - December 2025 \(Zurich\)**

    Fixed: Resolved an issue affecting localisation functionality

-   **Version 21.0.4 - August 2025**
    -   Document Generation
        -   Enhanced document generation with scripted variables support
        -   Improved handling of intermediate filters in document templates
        -   Fixed various document formatting issues
    -   Data Model
        -   Added support for scripted variables in templates
        -   A new role sn\_grc\_doc\_design.developer is added for creating scripted variables.
        -   Implemented intermediate filter functionality for content configuration
    -   Bug Fixes
        -   Resolved table formatting problems \(width truncation\)
        -   Fixed truncated image display in HTML content
-   **Version 20.0.1 - February 2025**
    -   Ability to add up to 20 columns in a table and in a content block
    -   Ability to choose and reorder columns from the add-in during template building
    -   Insert Content and Update Content from ServiceNow Reporting \(ESG add-in\) is merged with Document Designer add-in to insert data and reports into the document
    -   Data Relationship tab is added into the template configuration
    -   Template data relationship table is removed and deprecated Error handling \(Restrictions while template building\) Adding a Content block within other Content blocks is restricted Adding more than 10 images is restricted Adding more than one table inside the content block is restricted
-   **Version 19.1.2 - November 2024**

    The Document Designer for Microsoft Word enables you to extract metadata, including fields, related lists, reference fields, and their associated elements from ServiceNow tables. It also allows you to insert content blocks that repeat based on the number of records in a table, such as 10 blocks for 10 issues. When applied to specific records, the template generates a Word document.


**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

