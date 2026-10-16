---
title: ServiceNow Data Catalog release notes
description: Version history for the ServiceNow Data Catalog application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-plat-admin-sn-data-catalog.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - Admin version history release notes, ServiceNow Store version history release notes]
---

# ServiceNow Data Catalog release notes

Version history for the ServiceNow® Data Catalog application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.1 - October 2026**
    -   New
        -   Enrich your catalog with AI—use Otto to accelerate catalog curation with AI-powered enrichment. Enrich asset names and descriptions across multiple assets in a single request, review AI-generated recommendations, and publish richer metadata to your catalog faster and with less manual effort.
        -   Understand your sensitive data—a new Sensitivity tab on asset pages shows how your assets are classified for ServiceNow, Snowflake, and JDBC sources.
            -   You can also find and run the Vault classification agent from the Now Assist panel in Workflow Data Fabric - This feature is only available in Brazil version
        -   More ways to work with lineage—a new "Has lineage" search facet shows how much of your catalog has lineage and which assets have a lineage view in Graph Explorer. You can also download your current lineage view to CSV to analyze and use the data in other tools.
        -   More collector option—new Microsoft Fabric collector bring more metadata into the catalog. You can also choose whether a connection runs in the Servicenow hosted cloud infrastructure \(the default\) or through a MID Server to reach the data sources.
            -   Note: ServiceNow-hosted cloud collection is only available for the dcg-app in the Commercial Cloud environment.
        -   When a collector run completes or fails, the platform sends an email notification to the collector owner and any subscribers. Notifications use the ServiceNow Notification framework — no custom setup is required
        -   When a collector is configured to run on a MID Server, three routing models control how the system assigns a MID Server to the collection job
        -   Data Classification - Enable a metadata collector to classify harvested columns using ServiceNow Vault. The following metadata collector types support Vault classification:
            -   Snowflake
            -   Amazon Redshift
            -   Databricks
            -   Oracle
            -   PostgreSQL
            -   Teradata
            -   MySQL
            -   Microsoft SQL Server
            -   SAP HANA
    -   Changed
        -   Graph Explorer—lineage views open faster by showing the nearest upstream and downstream connections first instead of waiting for the full diagram to load.
        -   Runtime lineage for Snowflake—the Snowflake collector now captures lineage from stored procedures, MERGE statements, tasks, and scripts sent by orchestration tools. Your transformation chains now show up end to end.
        -   Refreshed bulk import/export for glossary terms—there's an updated Excel template with clearer instructions, and the import and preview screens now use standard ServiceNow components.
        -   Interface polish—the About sidebar now docks as a full-height panel. Asset and search page headers and classification tags also have consistent styling. More collector configuration fields now have better helper text.
        -   ServiceNow collector will harvest lineage edges based on platform's native Import Set Transform Map framework
    -   Fixed
        -   Installation and processing—the ServiceNow Data Catalog app now installs the required com.glide.rdf.api dependency. Catalog processing runs successfully in Regulated Market environments, and governance updates now apply to assets from tables with names longer than 40 characters.
        -   Bulk glossary import and export—the Status dropdown now appears on new rows, and invalid Status values are rejected. The preview shows the correct failed-record count when you re-upload a file, and exports made with the data steward role show the actual instance name. Submitting twice or retrying after a timeout no longer creates duplicate terms.
        -   Graph Explorer icons - related assets now show the correct type and icon.
        -   Collector runs—overlapping runs now finish reliably, and several source-specific issues are resolved:
            -   Snowflake keeps lineage when the harvesting role can't read some objects.
            -   Databricks harvests TIMESTAMP\_NTZ columns and retrieves the Unity Catalog metastore without authorization errors.
            -   SSIS connects to msdb on case-sensitive SQL Server instances.
        -   Faster responses for the Vault classification agent—catalog performance improvements reduce timeouts when the agent looks up assets.
-   **Version 2.0.5 - September 2026**

    The ServiceNow Data Catalog gives you one place to discover, search, and understand all your data assets—whether they live in your data warehouse, BI platform, or ServiceNow instance. Connect to your data sources automatically, build a shared business language with your team, and visualize how your data flows across systems. Start governing your data today.Built withinWorkflow Data Fabric, this new catalog integrates natively with theServiceNow AI Platform capabilities you already rely on, such as AI-driven insights, workflows, and process automation. Find, trust, and govern your data assets, whether they live in ServiceNow or beyond, by leveraging this unified solution for end-to-end data governance.


**Parent Topic:**[ServiceNow Store - Admin version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-plat-admin.md)

