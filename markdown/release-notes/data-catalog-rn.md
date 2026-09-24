---
title: Data Catalog release notes
description: Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Brazil release.The September 2026 release adds bulk glossary management, cloud-based metadata collectors, rich text editing for data assets, and SAP HANA and Salesforce collectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/data-catalog-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [data catalog, glossary, metadata collectors, SAP HANA, Salesforce, lineage]
breadcrumb: [App development and low-code release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Data Catalog release notes

Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Brazil release.

## About Data Catalog

-   Discover and search for data assets across your organization using a unified self-service interface.
-   View asset details including schema, descriptions, and data lineage across connected systems.
-   Define and maintain a business glossary to standardize data terminology across teams.
-   Collect and synchronize metadata from 14 or more external platforms using automated collectors.
-   Organize assets with tags and domains to improve discoverability and governance.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Install Data Catalog by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/build-automate-rn-landing.md)

## September 2026 store

The September 2026 release adds bulk glossary management, cloud-based metadata collectors, rich text editing for data assets, and SAP HANA and Salesforce collectors.

### What's new

-   **Bulk import and export glossary terms**

    Manage large volumes of glossary terms by importing and exporting them in bulk through XLSX files. Preview changes before committing, and get detailed feedback on any rows that fail so you can correct and re-upload. Reduce glossary enrichment time significantly.

-   **Cloud collectors for metadata collection**

    Collect metadata from your data sources without hosting and maintaining a MID Server.

-   **Rich text editing and image embedding in data assets**

    Document your data assets with rich text formatting and embedded images. Use bold, italics, lists, and links to format content, and embed images directly into catalog fields and resize them as needed.

-   **[SAP HANA metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/sap-hana-metadata-collector.md)**

    Automatically collect and synchronize metadata from SAP HANA using metadata collectors.

-   **[Salesforce metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/salesforce-metadata-collector.md)**

    Automatically collect and synchronize metadata from Salesforce using metadata collectors.


### What's changed

-   **Data assets lineage improvements**

    Transform nodes now display transformations and processing steps in your lineage diagram with enhanced visualizations. Interact with transform nodes to view additional details about what data transformations occur at each step, to help you understand your data flow more clearly. Lineage graphs now load progressively by level, to reduce timeout risk when viewing large graphs. The system displays lineage in stages, allowing you to explore relationships without waiting for the entire graph to load, which improves overall responsiveness and performance.


### Plugin information

-   **New plugins**

    ServiceNow Data Catalog \(sn\_dcg\_app\): Provides a self-service search and discovery interface for browsing data assets. Manages the core data model and business logic for catalog asset governance and enables automated metadata collection and integration connectivity with external data platforms.

-   **Deprecated plugins**

    Data Catalog UI \(sn\_dcg\_ui\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).

    Data Catalog Core \(sn\_dcg\_core\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).

    Metadata Collectors \(sn\_meta\_collectors\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).

    Metadata Collectors Core \(sn\_dcg\_cc\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).


