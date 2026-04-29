---
title: Microsoft SCCM integration
description: The Microsoft SCCM integration is a one direction import of SCCM data into the ServiceNow Configuration Management Database \(CMDB\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Microsoft SCCM integration

The Microsoft SCCM integration is a one direction import of SCCM data into the ServiceNow Configuration Management Database \(CMDB\).

Scheduled imports bring relevant SCCM data into the ServiceNow instance from an SQL Server database and map it to tables in the CMDB. You can configure either a full or incremental data import. The import is achieved using a JDBC connection via the MID Server. The integration keeps the ServiceNow CMDB synchronized with the SCCM SQLServer database, so that only relevant data is imported from the SCCM database to the CMDB. The SCCM database is considered an authoritative source and is not written to.

## Supported versions

The Microsoft SCCM legacy plugin is deprecated and no longer supported or available for new activation. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base. Recommendation for all customers to migrate to the new [Service Graph connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

These are the plugins for the currently supported SCCM versions, all of which support Asset Intelligence and Incremental Software Reconciliation:

-   Microsoft SCCM 2007
-   Microsoft SCCM 2012 v2
-   Microsoft SCCM 2016

**Note:** If you upgrade your instance to a version of the Now Platform that does not provide support for your version of SCCM, you can continue to use that version. However, all new instances require the use of a supported SCCM version.

The Integration - Microsoft SCCM 2016 \(com.snc.integration.sccm2016\) plugin is compatible with SCCM versions 1606, 1906, 1910, and 2002.

## Service Graph connector for Microsoft SCCM

To import SCCM data into the CMDB, you can use the [Service Graph connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) instead of using the legacy SCCM connector.

Using the Service Graph SCCM connector provides these advantages:

-   Adherence to the [Common Service Data Model \(CSDM\)](https://www.servicenow.com/docs/access?context=csdm-landing-page&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) data model.
-   Use of [Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) to avoid duplicate records.
-   Support for removed software detection and delta detection.
-   Use of the [IntegrationHub ETL \(2.2.1\)](https://www.servicenow.com/docs/access?context=integrationhub-etl&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) which allows for easy data mapping and customizations.
-   Higher performance during data processing.

For information on how to update from using the Microsoft SCCM connector plugin to using the Service Graph connector for Microsoft SCCM, see [Update Microsoft SCCM 2016 plugin for Service Graph connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Available modules

-   **Setup**:
    -   Configure the data sources.
    -   Specify database server settings and the MID Server.
    -   Test the configuration.
-   **Scheduled Import**: Schedule the import or execute the import immediately.
-   **Data Sources**: A list of the pre-configured data sources defining the external CMDB database.
-   **Progress**: The progress log for scheduled imports.
-   **Transform History**: A log of transformations performed by scheduled imports.
-   **CI Identification**: Identifiers used by SCCM to match import set data with the CMDB.
-   **Import Set Data**: Tables that store imported SCCM data.
-   **Web Services**: List of web services used to add or remove fields in the transform maps.

## Asset intelligence

Asset Intelligence is an SCCM feature that can filter, normalize and clean up software records. When enabled, it populates normalized software data in a separate table within the SCCM database. You can target this separate table instead of the raw software data table. When you import software records into the CMDB with this feature enabled, you get a cleaner set of software data. To use this feature, you must [Activate SCCM Asset Intelligence scheduled imports](../task/activate-ai-scheduled-imports.md) in the target ServiceNow instance, as well as in the source SCCM database.

-   **[Activate a supported Microsoft SCCM plugin](../task/activate-microsoft-sccm-plugin.md)**  
The SCCM plugins can be activated by an administrator and requires the Integration - JDBC and CI Identification plugins. These dependent plugins are activated automatically with SCCM activation.
-   **[SCCM data import process and source tables](../reference/how-sccm-integration-works.md)**  
The Microsoft SCCM versions supported in the ServiceNow® platform offer identical features and the same imported data.
-   **[Configure the SCCM integration and schedule an import](../task/configure-sccm-data-import.md)**  
Importing data from Microsoft SCCM requires a connection to the SCCM database via a JDBC data source and a schedule that tells the MID Server when to fetch the data.
-   **[Activate SCCM Asset Intelligence scheduled imports](../task/activate-ai-scheduled-imports.md)**  
To prevent duplicate software imports, activate either the Asset Intelligence \(AI\) or the non-AI scheduled import.
-   **[Upgrade the SCCM integration version](../../../product/discovery/task/t_UpgradeSCCMIntegrationVersion.md)**  
If you're using an earlier version of an System Center Configuration Manager\(SCCM\) plugin, you can switch over to a later version to take advantage of new features.

**Parent Topic:**[ServiceNow provided integrations](../../vendor-specific-integrations/reference/r_ServiceNowProvidedintegrations.md)

