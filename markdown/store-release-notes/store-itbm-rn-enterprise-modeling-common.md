---
title: Enterprise Modeling Common release notes
description: Version history for the Enterprise Modeling Common application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-enterprise-modeling-common.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Enterprise Architecture release notes, ServiceNow Store release notes]
---

# Enterprise Modeling Common release notes

Version history for the Enterprise Modeling Common application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.8.0 - June 2026**
    -   New:
        -   Replace an existing shape in a modeling diagram with a different shape type
        -   The width of the right side panel on the modeling diagram canvas is saved as a user preference and persists across sessions
-   **Version 3.6.1 - March 2026**
    -   New: Added support for Architecture Analyzer.
    -   Fixed:
        -   Fixed a bug where the user was allowed to modify the details of shapes for read-only diagrams.
        -   Supports up to 400% zoom level on the right side panel of the Enterprise Modeling and Visualization diagram page.
-   **Version 3.5.0 - December 2025**
    -   New: Streamlined entity creation: The Create new workflow for entities has been improved. You can now create entities by providing only the name while adding the entity to the diagram. The remaining fields can be filled in before committing the diagram. This simplifies and accelerates the entity creation process. Added Relationship tab for grouped AWS entities: A Relationship tab is added for entities grouped within an AWS group shape. Since these entities are connected through the grouped behavior rather than individual connector lines, this tab allows you to view and manage relationships.
    -   Enhanced right side panel: Right-hand side panel on the diagrams page can be resized as required.
-   **Version 3.4.0 - August 2025**
    -   New:
        -   Drag and drop shapes from the shapes palette to the canvas
        -   Delete diagrams directly from the Enterprise Modeling and Visualization home page. It removes the artifact and all associated versions
    -   Changed: Add description, label, and target date while creating new versions
-   **Version 3.3.2 - June 2025**

    Fixed: Issue where a business capability did not appear on the canvas when creating a business hierarchy map when both value stream and project entities were related to the same capability.

-   **Version 3.2.0 - February 2025**
    -   New: Read level access is granted to the "sn\_apm.apm\_read" role
    -   Fixed:
        -   Security fixes
        -   i18n/translation fixes
-   **Version 3.1.0 - November 2024**
    -   New:
        -   Support for business capability map.
        -   Support for ArchiMate type relationships \(ArchiMate is a registered trademark of The Open Group\).
-   **Version 2.0.0 - August 2024**

    Data model for Enterprise Modeling and Visualization app and Lucid chart integration.


