---
title: Data Catalog release notes
description: The ServiceNow Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-16"
reading_time_minutes: 3
---

# Data Catalog release notes

The ServiceNow® Data Catalog application is the self-service discovery layer within the Workflow Data Fabric application that enables teams to find, understand, and govern data assets across your organization. Data Catalog is a new application in the Australia release.

## Data Catalog highlights for the Australia release

-   Discover and search for data assets across your organization using a unified self-service interface.
-   View asset details including schema, descriptions, and data lineage across connected systems.
-   Define and maintain a business glossary to standardize data terminology across teams.
-   Collect and synchronize metadata from 14 or more external platforms using automated collectors.
-   Organize assets with tags and domains to improve discoverability and governance.

See Explore Data Catalog for more information.

**Important:** Data Catalog is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Data Catalog features

-   **Search and discovery**

    Find data assets across your organization using keyword search, filters, and faceted browsing in a unified self-service interface. Browse assets by type, domain, tag, or owner, and preview schema and sample data directly from search results to evaluate assets without opening each record.

-   **Asset details and relationships**

    View comprehensive details for each data asset including schema, field descriptions, ownership, data classifications, and data relationships, including lineage.

-   **Business glossary**

    Define and manage business terms and associate them with data assets to establish a shared vocabulary across teams. Link glossary terms to catalog assets so that business and technical users understand the meaning and context of data using consistent, organization-approved definitions.

-   **Metadata collectors**

    Automatically collect and synchronize metadata from external data platforms using metadata collectors. Collectors support 14+ platforms including Snowflake, BigQuery, Databricks, dbt Cloud, Tableau, Power BI, and Fivetran. Schedule collection runs or trigger them on demand to keep catalog content current as source systems evolve.

-   **Tags and domains**

    Organize and classify data assets using tags and domains to reflect your organization's structure and governance policies. Apply tags to individual assets or in bulk. Group assets into domains to control visibility and delegate stewardship to responsible teams.


## Activation information

Install Data Catalog by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Data Catalog UI \(sn\_dcg\_ui\): Provides the self-service search and discovery interface for browsing and viewing data assets in the catalog.
    -   Data Catalog Core \(sn\_dcg\_core\): Provides the core data model and business logic for catalog asset management, classifications, and lineage.
    -   Metadata Collectors \(sn\_meta\_collectors\): Enables automated metadata collection from external data platforms to populate and synchronize catalog content.
    -   Metadata Collectors Core \(sn\_dcg\_cc\): Provides connectivity services for integrating Data Catalog with external data sources and platforms.
    -   Workflow Data Fabric Connect Hub \(sn\_wdf\_connect\_hub\): Provides the central hub for managing external data source connections used by Workflow Data Fabric and Data Catalog.

## Related ServiceNow applications and features

-   **Workflow data fabric**

    The ServiceNow® Workflow Data Fabric application provides the foundational platform for creating and managing data interfaces and products. Data Catalog is installed as part of the Workflow Data Fabric application and surfaces assets created and published through it.

-   **Data Products**

    The ServiceNow® Data Products application enables teams to define, publish, and share governed data products. Published data products are discoverable in Data Catalog, where consumers can find, evaluate, and request access to organizational data.

-   **Mid server**

    The ServiceNow® MID Server provides secure bidirectional communication between your ServiceNow instance and external platforms. Metadata collectors use the MID Server to reach data sources in on-premises or private cloud environments not directly accessible from your instance.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

