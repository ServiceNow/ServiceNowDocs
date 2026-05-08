---
title: Telecom Discovery Builder framework
description: The Telecom Discovery Builder framework ETL \(Extract, Transform, Load\) is a reusable and schema-aligned component delivered with the Telecommunications Service Operations Management \(TSOM\) Core application. It provides a consistent and extensible method for ingesting telecom inventory data into the ServiceNow configuration management database \(CMDB\) across multiple Service Graph Connectors \(SGCs\).
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Telecom Discovery, Explore, Telecommunications Service Operations Management]
---

# Telecom Discovery Builder framework

The Telecom Discovery Builder framework ETL \(Extract, Transform, Load\) is a reusable and schema-aligned component delivered with the Telecommunications Service Operations Management \(TSOM\) Core application. It provides a consistent and extensible method for ingesting telecom inventory data into the ServiceNow configuration management database \(CMDB\) across multiple Service Graph Connectors \(SGCs\).

The Telecom Discovery Builder framework ETL serves as a baseline data ingestion utility to handle telecom-specific configuration item \(CI\) data. It enables connector development teams to avoid building ETLs from scratch by offering a standardized transform logic that can be duplicated and customized for each connector. It provides a standardized, reusable foundation that promotes consistency across implementations.

Once the TSOM Core plugin is activated, the generic ETL is auto-provisioned and becomes available in the Integration Hub ETL Studio, ready to be reused and adapted to connector-specific needs.

## Why and when to use the Telecom Discovery Builder framework

Use the Telecom Discovery Builder framework when you want to do the following:

-   Deploy a new Service Graph Connector in a telecom environment and want to avoid building the ETL from scratch.
-   Maintain schema-aligned consistency across multiple connectors and platform instances.
-   Discovery payloads and CI relationships compliant with TNI \(Telecommunications Network Inventory\). For more information, see Telecommunications Network Inventory.
-   Work within an SGC \(Service Graph Connector\) application scope and want to customize ETL behavior without modifying core logic.
-   Benefit from predefined mappings, validated JSON schema support, and a UI-driven configuration interface.

## Key capabilities and features

-   Auto-provisioned with TSOM core: Installs automatically and is ready to use across telecom connectors.
-   Generic schema-based ingestion: Supports a unified data schema for telecom CIs.
-   Supports duplication and customization: Duplicate the Telecom Discovery Builder ETL framework into your application scope using Integration Hub ETL Studio.
-   TNI support: Aligned to the TNI data model and the ETL logic can be extended to generate and link TNI entities.
-   Flexible field-mapping interface: Configure import sets, data sources, targets, and transformation logic through a UI-driven experience.

## Key user roles

The tsom\_visibility\_admin and tsom\_assurance\_admin roles provide granular access control across TSOM Visibility and Assurance application scopes, supporting stronger security and compliance in line with the Granular Admin directive.

-   The tsom\_assurance\_admin role provides full operational and administrative access to TSOM Assurance application scopes.
-   The tsom\_visibility\_admin role manages the operational tasks for the TSOM visibility application.

These roles control access to the TSOM Visibility and Assurance application scopes listed in the following table.

|Scope name|Description|
|----------|-----------|
|`sn_tsom_core` \(Telecom Service Operations Core\)|Includes the audit application and various system properties within that app scope.|
|`sn_tsom_em_core`\(Event Management Core\)|Includes the monitoring and analysis of telecommunications network alerts and performance metrics from SD-WAN infrastructure.|
|`sn_tsom_em_connect`\(Event Management Connectors\)|Include push connectors and connector definitions used to ingest alerts from external telecommunications network sources.|
|`sn_tsom_patterns`\(Telecom Discovery Patterns \)|Include the MID Server and system IP Service properties.|
|`sn_sgc_aliplano`\(Service Graph Connector for Nokia Altiplano\)|Includes the application properties.|
|`sn_sgc_meraki`\(Service Graph Conenctor for Cisco Meraki\)|Includes the application properties.|
|`sn_sgc_fortinet`\(Service Graph Connector for Fortinet\)|Includes the application properties.|

The following table lists the roles contained in the tsom\_visibility\_admin role.

<table id="table_vjs_1b3_jhc"><thead><tr><th>

Role name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`import_admin`

</td><td>

-   Monitors scheduled data import executions, including viewing the hierarchy and flow of chained imports, accessing execution contexts, and diagnosing import issues.
-   Manages all aspects of import set records and imports.

</td></tr><tr><td>

`connection_admin`

</td><td>

-   Responsible for managing connections and credentials, especially for Integration Hub.
-   Create and configure HTTP and HTTPS connections, which are used by custom actions or activities to connect to external endpoints. These actions include setting up connection details such as credentials, connection aliases, URLs, MID Server options, and additional attributes.

</td></tr><tr><td>

`sn_cmdb_admin`

</td><td>

-   Highest-level administrative role for CMDB privileges.
-   Grants full access to CMDB data, tools, and user interfaces, and enables administrators to configure policies such as class management and application service requirements that aren’t available to editors.

</td></tr><tr><td>

`discovery_admin`

</td><td>

-   Grants access to the tables in the Discovery application.
-   Essential for configuring and executing discovery in your network.
-   Includes setting up MID Servers, managing credentials, defining discovery schedules, and validating results.

</td></tr><tr><td>

`usage_admin`

</td><td>

-   For instances using Discovery, this role enables users to track the number of active users and hardware configuration items \(CIs\) discovered.
-   Monitors instance usage through dashboards, providing information to help your organization understand application adoption and usage patterns.

</td></tr><tr><td>

`cmdb_inst_admin`

</td><td>

-   Enables users to create and customize integrations using Integration Hub ETL, including integrating third-party data into CMDB or supported non-CMDB tables.
-   Necessary to use the Integration Hub ETL store app and access CMDB Integrations.

</td></tr><tr><td>

`certification_admin`

</td><td>

-   Enables users to manage certification filters for auditing subsets of records.
-   Create, update, delete, and run certification audits, compare records against expected values, and assign follow-on tasks to remediate discrepancies.
-   Manage and reassign follow-on tasks from compliance audits and view all such tasks. Users with the certification role can access only tasks assigned to them.

</td></tr><tr><td>

`agent_admin`

</td><td>

-   Responsible for downloading and administering the system's built-in MID Server agent.
-   Enables users to manage scripts and properties related to the MID Server.

</td></tr></tbody>
</table>## Key benefits

Benefits of the Telecom Discovery Builder framework ETL include:

-   Consistency in how telecom configuration items \(CIs\) are structured and loaded into the CMDB.
-   Reusability through duplication and customization across connectors.
-   Compliance with TNI schemas and discovery model requirements.
-   Flexibility to extend and tailor data transformations without compromising the base schema.

**Related topics**  


[Configuring the Telecom Discovery Builder framework ETL in a connector](configuring-the-telco-generic-schema-etl.md)

[Extend TNI entity support for duplicated ETLs](../task/configuring-tni-entiry-support-for-duplicated-etls.md)

