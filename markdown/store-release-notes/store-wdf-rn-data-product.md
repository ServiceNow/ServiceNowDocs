---
title: Data Product release notes
description: Version history for the ServiceNow Data Product application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-wdf-rn-data-product.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Workflow Data Fabric release notes, ServiceNow Store release notes]
---

# Data Product release notes

Version history for the ServiceNow® Data Product application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.1 - June 2026**
    -   Data Interface editing is now available: Added full edit capabilities for published Data Interfaces, enabling modifications without recreating the interface.
    -   Supported changes include:
        -   -   Updating interface labels
-   Adding or removing source tables
-   Changing combination methods \(single table, JOIN, or UNION\)
-   Updating target field types and labels for existing columns
-   Adding new target columnsInterface names and existing target field names remain immutable to preserve stable contracts for downstream consumers. The Review Changes modal displays pending edits before save, with transactional application ensuring the interface returns to its last published state if any step fails.
-   **Version 1.0.9 - May 2026**
    -   This release introduces the first GA version of Workflow Data Fabric Data Products and Data Interfaces, enabling the following core capabilities:
        -   Dependencies, Installation, and Licensing
        -   Dependencies: Requires Zero Copy Connector Hub, Zero Copy Connectors, and ServiceNow Data Catalog store applications. These apps will automatically get installed as a result of installing Data Product app.
        -   Installation: Supported on instances running Australia Patch 1 or higher
        -   Licensing: Free to use in sub-production and development instances. Requires Workflow Data Fabric \(WDF\) Foundation or Advanced SKUs for production use
        -   Pre-requisite: For subproduction environments, please ensure AI Search is activated by following the instructions
        -   Features:
            -   Catalog-First Authoring Experience
                -   Discover and onboard data assets through Data Catalog
                -   Create Data Interfaces and Data Products directly from catalog assets
                -   Improve reuse and reduce duplication of data efforts
                -   Schema mappings and transformations during authoring\(coming soon\)
            -   Data Interfaces \(Stable Data Contracts\)
                -   Define durable, schema-based interfaces for consistent data access
                -   Support multi-source composition \(e.g., unions, joins via DBViews\)
                -   Provide a consistent access layer for analytics, workflows, and AI
                -   Late binding to underlying sources with backward-compatible schema evolution\(coming soon\)
            -   Data Products \(Governed Data Assets\)
                -   Create reusable, business-aligned data entities built on Data Interfaces
                -   Package, govern, and manage data with ownership, lifecycle, and metadata
                -   Enable discovery and consumption via Data Catalog
            -   Governance and Access Control
                -   Integrate with ServiceNow ACL and role-based access control
                -   Enable controlled, request-based access via catalog workflows
                -   Ensure governed exposure of underlying data assets
            -   Zero-Copy Data Access
                -   Access external data in place without replication using federated queries
                -   Support sources such as Snowflake, Databricks, and native ServiceNow data
                -   Optimize performance through pushdown query execution
                -   Enable near-real-time data access
-   **Version 1.0.8 - May 2026**
    -   Create governed, reusable data products with stable data interfaces that unify data across systems—so teams can discover, access, and act on trusted data without moving it.
    -   Business-entity–centric packaging \(Customer360, Billing, etc.\)
        -   Reusable, discoverable assets in the data catalog
        -   Clear ownership &amp; lifecycle management
        -   Multi-source composition \(external + ServiceNow + derived\)
        -   Interface-driven access \(no direct table coupling\)

**Parent Topic:**[ServiceNow Store - Workflow Data Fabric release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-workflow-data-fabric-highlights.md)

