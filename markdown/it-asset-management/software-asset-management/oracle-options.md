---
title: Oracle Database options and management packs
description: You can use the Software Asset Management publisher pack for Oracle to track licensing positions for your Oracle Database options and management packs. The Licensable Oracle Options \[samp\_oracle\_option\_set\] table provides the complete list of database options and management packs that you can create software models for.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Software Asset Management publisher pack for Oracle, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Oracle Database options and management packs

You can use the Software Asset Management publisher pack for Oracle to track licensing positions for your Oracle Database options and management packs. The Licensable Oracle Options \[samp\_oracle\_option\_set\] table provides the complete list of database options and management packs that you can create software models for.

You must manage licensing for your Oracle Database options and management packs separately from your Oracle Database servers. Separate software models and entitlements are required for each of your database servers, database options, and management packs, thereby providing a more comprehensive view of your Oracle license compliance position.

For example, Oracle DB Server 12c R1 Enterprise with the Partitioning option requires two separate software models and entitlements.

<table id="table_bpl_1qn_4lb"><thead><tr><th>

Purpose

</th><th>

Software model

</th><th>

Software entitlement

</th></tr></thead><tbody><tr><td>

Track licensing for Oracle DB Server 12c R1 Enterprise.

</td><td>

Oracle DB Server 12c R1 Enterprise

 No value selected for the **Database option** field.

</td><td>

Record your purchased rights for Oracle DB Server 12c R1 Enterprise.

</td></tr><tr><td>

Track licensing for the Partitioning option.

</td><td>

Oracle DB Server 12c R1 Enterprise Partitioning

 **Partitioning** selected for the **Database option** field.

</td><td>

Record your purchased rights for the Partitioning option.

</td></tr></tbody>
</table>To track and measure usage for your Oracle Database options and management packs, request and install the Data Collection for Oracle Global Licensing and Advisory Services application from the ServiceNow Store. See [Request Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)](../task/request-data-collection-oracle-glas-app.md) for detailed instructions.

**Important:** If you are activating the Software Asset Management application for the first time in the San Diego and later releases, the Data Collection for Oracle Global Licensing and Advisory Services application is required for discovering and measuring the usage of your database options and management packs.

If you are activating the Software Asset Management application for the first time in the Rome and earlier releases or you are upgrading an existing instance of the Software Asset Management application from the Rome and earlier releases to the San Diego and later releases, you can continue using the existing patterns for discovering and measuring the usage of your database options and management packs. However, ServiceNow recommends that you use the Data Collection for Oracle Global Licensing and Advisory Services application instead, as the application provides enhanced capabilities that address additional use cases.

After you install the application, the SAM - Evaluate database option usage from Oracle GLAS data scheduled job runs weekly or on-demand to retrieve usage data for both the Oracle database options and management packs that are installed in your Oracle environment and the Oracle features that are associated with them. The Software Asset Management application can then include this data in the Oracle reconciliation process to help you determine the license compliance positions of your database options and management packs, which are reported separately from the license compliance positions of your Oracle Database servers.

**Note:** For more information on how usage data for your Oracle features can help you determine the license compliance of your database options and management packs, see [Feature mapping for Oracle Database options and management packs](../concept/oracle-feature-option-mapping.md#).

Oracle Database options and management packs follow the Oracle Database server lifecycle and are displayed in the License usage view \(Software Asset Workspace\) or License Workbench \(Software Asset Management classic application\). However, the following remediation options are not available for database options and management packs:

-   Remove Unallocated Installs
-   Remove Unlicensed Installs

## Supported Oracle Database options and management packs

The Software Asset Management publisher pack for Oracle supports the following database options and management packs based on whether you are using the existing discovery and usage measurement patterns or the Data Collection for Oracle Global Licensing and Advisory Services application to track and measure usage for your database options and management packs.

<table id="table_bcy_yqz_zlb"><thead><tr><th>

Oracle Database option or management pack

</th><th>

Supported by existing discovery and usage measurement patterns

</th><th>

Supported by the Data Collection for Oracle Global Licensing and Advisory Services application

</th></tr></thead><tbody><tr><td>

Active Data Guard

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Advanced Compression

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Advanced Security

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Change Management Pack**Note:** If your database is running Oracle Database 12c or later, the Change Management Pack, Configuration Management Pack for Oracle Database, and Provisioning and Patch Automation Pack for Database are consolidated into the Oracle Database Lifecycle Management Pack for Oracle Database. To use the Change Management Pack, you must license the Oracle Database Lifecycle Management Pack for Oracle Database.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Configuration Management Pack for Oracle Database**Note:** If your database is running Oracle Database 12c or later, the Change Management Pack, Configuration Management Pack for Oracle Database, and Provisioning and Patch Automation Pack for Database are consolidated into the Oracle Database Lifecycle Management Pack for Oracle Database. To use the Configuration Management Pack for Oracle Database, you must license the Oracle Database Lifecycle Management Pack for Oracle Database.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Content Database Suite**Note:** Content Database Suite is available only on databases that are running Oracle Database 11g Release 1 and earlier.

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Data Masking Pack

</td><td>

Yes

</td><td>

No**Note:** If you are using the Data Collection for Oracle Global Licensing and Advisory Services application, you can track and measure usage for Oracle Data Masking and Sub-setting Pack instead.

</td></tr><tr><td>

Data Mining**Note:** Data Mining requires separate licensing only if your database is running Oracle Database 11g Release 1 or earlier. If your database is running Oracle Database 11g Release 2 or later, Data Mining is already included in the database license.

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Database In-Memory

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Database Vault

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Diagnostics Pack

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Label Security

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Multitenant

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

OLAP

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Oracle Cloud Management Pack for Oracle Database

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Oracle Data Masking and Sub-setting Pack

</td><td>

No**Note:** If you are using the existing discovery and usage measurement patterns for your database options and management packs, you can track and measure usage for Data Masking Pack instead.

</td><td>

Yes

</td></tr><tr><td>

Oracle Database Lifecycle Management Pack for Oracle Database**Note:** If your database is running Oracle Database 12c or later, the Change Management Pack, Configuration Management Pack for Oracle Database, and Provisioning and Patch Automation Pack for Database are consolidated into the Oracle Database Lifecycle Management Pack for Oracle Database. You can access all three packs by licensing only the Oracle Database Lifecycle Management Pack for Oracle Database.

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Oracle Spatial and Graph**Note:** Oracle Spatial and Graph requires separate licensing only if your database is running Oracle Database 11g Release 1 or earlier. If your database is running Oracle Database 11g Release 2 or later, Oracle Spatial and Graph is already included in the database license.

</td><td>

No**Note:** If you are using the existing discovery and usage measurement patterns for your database options and management packs, you can track and measure usage for Spatial and Graph instead.

</td><td>

Yes

</td></tr><tr><td>

Partitioning

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Provisioning and Patch Automation Pack for Database**Note:** If your database is running Oracle Database 12c or later, the Change Management Pack, Configuration Management Pack for Oracle Database, and Provisioning and Patch Automation Pack for Database are consolidated into the Oracle Database Lifecycle Management Pack for Oracle Database. To use the Provisioning and Patch Automation Pack for Database, you must license the Oracle Database Lifecycle Management Pack for Oracle Database.

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Real Application Clusters

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Real Application Clusters One Node

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Real Application Testing

</td><td>

Yes

</td><td>

Yes

</td></tr><tr><td>

Records Database**Note:** Records Database is available only on databases that are running Oracle Database 10g Release 2 or earlier.

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Spatial and Graph**Note:** Spatial and Graph requires separate licensing only if your database is running Oracle Database 11g Release 1 or earlier. If your database is running Oracle Database 11g Release 2 or later, Spatial and Graph is already included in the database license.

</td><td>

Yes

</td><td>

No**Note:** If you are using the Data Collection for Oracle Global Licensing and Advisory Services application, you can track and measure usage for Oracle Spatial and Graph instead.

</td></tr><tr><td>

Total Recall**Note:** Total Recall is available only on databases that are running Oracle Database 11g and earlier.

</td><td>

No

</td><td>

Yes

</td></tr><tr><td>

Tuning Pack**Note:** Tuning Pack is supported only on databases that are running Oracle Database Enterprise Edition. If Tuning Pack is discovered on any database that is running Oracle Database Standard Edition or Express Edition, the Software Asset Management application generates a removal candidate for that Tuning Pack installation. To maintain compliance with Oracle, you must either uninstall Tuning Pack from the database or upgrade the database to Oracle Databse Enterprise Edition.

</td><td>

Yes

</td><td>

Yes

</td></tr></tbody>
</table>-   **[Request Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)](../task/request-data-collection-oracle-glas-app.md)**  
Request the Data Collection for Oracle GLAS application from the ServiceNow Store so that you can track and measure usage for your Oracle Database options and management packs.
-   **[Feature mapping for Oracle Database options and management packs](../concept/oracle-feature-option-mapping.md#)**  
The Software Asset Management application automatically maps discovered Oracle features to the Oracle Database options and management packs that they are associated with. These mappings can help you determine the usage and license compliance of your database options and management packs.
-   **[Unreported Database Options Usage report](oracle-unreported-database-options-usage-report.md)**  
You can use the Unreported Database Options Usage report to gain visibility into the Oracle Database options and management packs that are being used on undiscovered database instances. Although you cannot track usage for these database options and management packs, this report can help you determine any potential licensing implications that are associated with them.

**Parent Topic:**[Software Asset Management publisher pack for Oracle](../concept/oracle-publisher-pack.md)

