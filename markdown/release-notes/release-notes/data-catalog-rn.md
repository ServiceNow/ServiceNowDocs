---
title: Data Catalog release notes
description: The ServiceNow Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Australia release.The September 2026 release adds bulk glossary management, cloud-based metadata collectors, rich text editing for data assets, and SAP HANA and Salesforce collectors.The ServiceNow Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-04-16"
reading_time_minutes: 6
---

# Data Catalog release notes

The ServiceNow® Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Australia release.

## About Data Catalog

-   Discover and search for data assets across your organization using a unified self-service interface.
-   View asset details including schema, descriptions, and data lineage across connected systems.
-   Define and maintain a business glossary to standardize data terminology across teams.
-   Collect and synchronize metadata from 14 or more external platforms using automated collectors.
-   Organize assets with tags and domains to improve discoverability and governance.

See [Explore Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/explore-data-catalog.md) for more information.

## Activation and other requirements

**Important:** Data Catalog is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Data Catalog by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## September 2026

The September 2026 release adds bulk glossary management, cloud-based metadata collectors, rich text editing for data assets, and SAP HANA and Salesforce collectors.

### What's new

-   **Bulk import and export glossary terms**

    Quickly manage large volumes of glossary terms by importing and exporting them in bulk through XLSX files. Preview changes before committing, and get detailed feedback on any rows that fail so you can correct and re-upload. Skip manual entry and reduce glossary enrichment time significantly.

-   **Rich text editing and image embedding in data assets**

    Document your data assets with rich text formatting and embedded images. Edit with bold, italics, lists, and links, then embed images directly into catalog fields and resize them as needed.

-   **Cloud collectors for metadata collection**

    ****

    Collect metadata from your data sources without hosting and maintaining a MID Server.

-   **SAP HANA metadata collector**

    Automatically collect and synchronize metadata from SAP HANA using metadata collectors.

-   **Salesforce metadata collector**

    Automatically collect and synchronize metadata from Salesforce using metadata collectors.


### What's changed

-   **Data assets lineage improvements**

    Transform nodes now display transformations and processing steps in your lineage diagram with enhanced visualizations. Interact with transform nodes to view additional details about what data transformations occur at each step, helping you understand your data flow more clearly.Lineage graphs now load progressively by level, reducing the risk of timeouts when viewing large graphs. The system displays lineage in stages, allowing you to explore relationships without waiting for the entire graph to load, which improves overall responsiveness and performance.


### Plugin information

-   **New plugins**

    ServiceNow Data Catalog \(sn\_dcg\_app\): Provides a self-service search and discovery interface for browsing data assets. Manages the core data model and business logic for catalog asset governance and enables automated metadata collection and integration connectivity with external data platforms.

-   **Deprecated plugins**

    Data Catalog UI \(sn\_dcg\_ui\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).

    Data Catalog Core \(sn\_dcg\_core\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).

    Metadata Collectors \(sn\_meta\_collectors\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).

    Metadata Collectors Core \(sn\_dcg\_cc\): Replaced by ServiceNow Data Catalog \(sn\_dcg\_app\).


## Australia

The ServiceNow® Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Australia release.

### What's new

-   **[Search and discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/explore-data-assets-in-data-catalog.md)**

    Find data assets across your organization using keyword search, filters, and faceted browsing in a unified self-service interface. Browse assets by type, domain, tag, or owner, and preview schema and sample data directly from search results to evaluate assets without opening each record.

-   **[Asset details and relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/view-data-asset-details.md)**

    View comprehensive details for each data asset including schema, field descriptions, ownership, data classifications, and data relationships, including lineage.

-   **[Business glossary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-glossary-term.md)**

    Define and manage business terms and associate them with data assets to establish a shared vocabulary across teams. Link glossary terms to catalog assets so that business and technical users understand the meaning and context of data using consistent, organization-approved definitions.

-   **[Metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)**

    Automatically collect and synchronize metadata from external data platforms using metadata collectors. Collectors support 14+ platforms including Snowflake, BigQuery, Databricks, dbt Cloud, Tableau, Power BI, and Fivetran. Schedule collection runs or trigger them on demand to keep catalog content current as source systems evolve.

-   **[Tags and domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-tags-dc.md)**

    Organize and classify data assets using tags and domains to reflect your organization's structure and governance policies. Apply tags to individual assets or in bulk. Group assets into domains to control visibility and delegate stewardship to responsible teams.


-   ****

    Automatically collect and synchronize metadata from Amazon S3 using metadata collectors.

-   ****

    Automatically collect and synchronize metadata from Teradata using metadata collectors.

-   **Data quality for data assets**

    Review data quality information for table and column assets directly in the Data Catalog. The Overview tab surfaces a quality summary — overall status, rule count, passed rules, and last evaluation time — and the new Quality tab lists each rule with its source, asset type, category, status, and last run time. External data quality tools submit rule results through the Data Quality API.

-   **Classifier field for columns**

    View column-level classification directly from a data asset's Columns tab. The new Classifier field shows the classification assigned to each column by the ServiceNow collector, or displays null if classification hasn't run on the table. Access to this feature depends on your entitlements.

-   **Email notifications for owner and steward assignments for data assets**

    When you add or remove an owner or steward on a data asset, the system sends an email notification to that user.

-   **[Clone metadata collector connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)**

    Clone an existing metadata collector connection to create data source connection faster. When you clone a connection, the system copies the connection type, collection settings, filters, and advanced parameters to a new connection record with an auto-generated name. Sensitive information is not carried over. Update credentials and any other environment-specific details before activating the new connection.

-   **[Data quality for data assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/view-data-asset-details.md)**

    Review data quality information for table and column assets, including the overall data quality status, the total number of rules, the number of passed rules, and any quality badges awarded to the resource. View each rule with its source, asset type, asset name, category, status, and last run time, and filter or search to locate a specific rule. External data quality tools submit rule results through the Data Quality API.

-   **[Azure Data Factory metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/azure-data-factory-metadata-collector.md)**

    Automatically collect and synchronize metadata from Azure Data Factory using metadata collectors.


### What's changed

-   **[ServiceNow metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/servicenow-metadata-collector.md)**

    Control how the collector harvests metadata. Enable an API size limit to cap the volume of data retrieved per request, exclude Glide artifacts from harvesting, and harvest Platform Analytics artifacts.


### Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   ServiceNow Data Catalog \(sn\_dcg\_app\): Provides a self-service search and discovery interface for browsing data assets. Manages the core data model and business logic for catalog asset governance and enables automated metadata collection and integration connectivity with external data platforms.
    -   Graph Explorer \(sn\_hexplorer\): Provides visualization of data flow and business context relationships across systems with column-level lineage tracking. Enables interactive catalog navigation with upstream and downstream data flows and dependency insights.
    -   Workflow Data Fabric Connect Hub \(sn\_wdf\_connect\_hub\): Provides the central hub for managing external data source connections used by Workflow Data Fabric and Data Catalog.

