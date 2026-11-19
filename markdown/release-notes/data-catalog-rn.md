---
title: Data Catalog release notes
description: Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Brazil release.This release adds Data Catalog Analytics dashboards, an SSRS metadata collector, and Databricks Unity Catalog metric view support. It also includes Salesforce OAuth authorization code flow and the ability to download lineage nodes and edges as CSV.The October 2026 release adds AI-powered catalog enrichment, lineage enhancements, a Microsoft Fabric collector, MID Server routing, collector notifications, and data classification with Vault.The September 2026 release adds bulk glossary management, cloud-based metadata collectors, rich text editing for data assets, and SAP HANA and Salesforce collectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/data-catalog-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [data catalog, analytics dashboards, SSRS collector, Databricks, Salesforce, lineage, CSV download, data catalog, metadata collectors, Microsoft Fabric, MID Server, Vault, lineage, AI enrichment, data catalog, glossary, metadata collectors, SAP HANA, Salesforce, lineage]
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

## November 2026 store

This release adds Data Catalog Analytics dashboards, an SSRS metadata collector, and Databricks Unity Catalog metric view support. It also includes Salesforce OAuth authorization code flow and the ability to download lineage nodes and edges as CSV.

### What's new

-   **Data Catalog Analytics dashboards**

    Track catalog adoption and collector health from dashboards inside Workflow Data Fabric. The Adoption overview tab shows how many users have access to Data Catalog, how many are active, and how activity changes over time. The Collector health tab shows how many collector runs succeeded or failed, which collectors are active, and which collectors have not run recently.

-   **SQL Server Reporting Services \(SSRS\) metadata collector**

    Collect and catalog metadata from your SSRS environment. The collector harvests datasets, data sources, folders, KPIs, reports, and linked reports, including lineage between datasets, data sources, and reports.

-   **Databricks Unity Catalog metric views**

    The Databricks collector harvests Unity Catalog metric views, including dimensions, measures, YAML definition, source table, filter, and materialization status. Lineage from a metric view to its source table is available even if the metric view has never been queried.

-   **Salesforce OAuth authorization code flow**

    The Salesforce collector supports OAuth authorization code flow using a refresh token, alongside the existing username and password and OAuth client ID and secret options.

-   **Download lineage nodes and edges as CSV**

    Download the nodes, edges, or both from your current lineage view to a CSV file to analyze dependencies in other tools.


### What's changed

-   **ServiceNow collector includes application short descriptions**

    The ServiceNow metadata collector harvests the short description field from system application assets. Catalog users get more context when browsing or searching for ServiceNow application metadata.

-   **Metadata Enrichment AI Agent display updates**

    Review enrichment suggestions with a more consistent interface. Labels, fonts, and formats are standardized, asset type is now visible in the enrichment view, and terminology uses "data asset" consistently.


## October 2026 store

The October 2026 release adds AI-powered catalog enrichment, lineage enhancements, a Microsoft Fabric collector, MID Server routing, collector notifications, and data classification with Vault.

### What's new

-   **Metadata enrichment with ServiceNow Otto**

    Accelerate catalog curation using AI-powered enrichment. Enrich asset names and descriptions across multiple assets in a single request, review AI-generated recommendations, and publish richer metadata to your catalog with less manual effort.

-   **Lineage search facet and CSV export**

    A new "Has lineage" search facet shows how much of your catalog has lineage and which assets have a lineage view in Graph Explorer. Download your current lineage view to CSV to analyze and use the data in other tools.

-   ****

    Automatically collect and synchronize metadata from Microsoft Fabric using metadata collectors.

-   **MID Server routing for metadata collectors**

    Choose whether a connection runs in the ServiceNow hosted cloud infrastructure \(the default\) or through a MID Server to reach your data sources. When a collector is configured to run on a MID Server, three routing models control how the system assigns a MID Server to the collection job.

-   **Email notifications for collector runs**

    When a collector run completes or fails, the platform sends an email notification to the collector owner and any subscribers. Notifications use the ServiceNow Notification framework.

-   **Data classification with Vault**

    Enable a metadata collector to classify harvested columns using ServiceNow Vault. The following metadata collector types support Vault classification:

    -   Snowflake
    -   Amazon Redshift
    -   Databricks
    -   Oracle
    -   PostgreSQL
    -   Teradata
    -   MySQL
    -   Microsoft SQL Server
    -   SAP HANA

### What's changed

-   **Graph Explorer performance improvements**

    Lineage views open faster by showing the nearest upstream and downstream connections first instead of waiting for the full diagram to load.

-   **ServiceNow collector lineage from Import Set Transform Maps**

    The ServiceNow collector harvests lineage edges based on the platform's native Import Set Transform Map framework.


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


