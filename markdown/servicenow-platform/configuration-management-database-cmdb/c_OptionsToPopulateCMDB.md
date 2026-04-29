---
title: Populating the CMDB
description: You can populate the CMDB by using Discovery, by using the IntegrationHub ETL or Import Sets to import and integrate data from a third-party source, by integrating with an external CMDB, or by manually creating CIs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Populating the CMDB

You can populate the CMDB by using Discovery, by using the IntegrationHub ETL or Import Sets to import and integrate data from a third-party source, by integrating with an external CMDB, or by manually creating CIs.

When you populate the CMDB with information, you create a record for each configuration item in the cmdb\_ci table or on one of the tables that extend that table.

Related ServiceNow® Store apps and reference information:

-   [CMDB schema model](c_ConfigurationManagementDatabase.md): A collection of class diagrams and class attributes for key CMDB classes.
-   [CMDB tables descriptions](../reference/cmdb-tables-details.md): Descriptions of key CMDB tables in the base system.
-   [CMDB CI Class Models](cmdb-ci-class-models.md): A ServiceNow Store app that adds class models that extend the base CMDB class hierarchy. This includes class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can then use the added classes as any other CMDB base class.
-   [Discovery patterns](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=australia&pubname=australia-it-operations-management&ft:locale=en-US): A ServiceNow Store app that provides a library of Discovery patterns for discovering specific devices and applications in the industry.
-   [Getting started with Service Graph Connectors](cmdb-sgc-intro.md): ServiceNow Store apps that provide pre-defined integrations for importing and integrating common third-party data into CMDB classes. Also includes the [IntegrationHub ETL](integrationhub-etl.md) wizard for creating new ETL transform maps.

## ITIL configuration management auto-discovery

The key to any configuration management business practice is the initial and on-going inventory or discovery of what you own. The ServiceNow platform provides three options for auto-discovery:

-   The separate and highly robust [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) product.
-   For organizations that want to leverage the discovery technologies they already have deployed \(SMS, Tally NetCensus, LanDesk, and so on\), the ServiceNow platform supports integrations to those technologies via web services. Scanned data can be mapped directly into the CMDB.

For further information on designing, constructing, and maintaining the CMDB, see the [CMDB Design &amp; Configuration](https://support.servicenow.com/kb_view.do?sysparm_article=KB0552861) white paper.

## Discovery

The Discovery product automatically populates the CMDB. Discovery searches the network for all attached computers and devices, then populates the CMDB with information on each computer/device's configuration, provisioning, and current status. Discovery uses probes, sensors, and patterns, to collect and process data about computers, servers, printers, a variety of IP-enabled devices, and the relationships between all the items found. Discovery also reports on any software which is running, and the TCP connections between computer systems, thereby establishing their relationships. This information is sent back to the instance and is used to populate the CMDB.

For more information about Discovery see:

-   [ITOM Visibility](https://www.servicenow.com/docs/access?context=itom-visibility-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)
-   [Discovery basics](https://www.servicenow.com/docs/access?context=c_GetStartedWithDiscovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

## Integrate third-party data using IntegrationHub ETL

Use the [IntegrationHub ETL](integrationhub-etl.md) to import and integrate data from a third party into the CMDB. Using IntegrationHub ETL, create ETL transform maps which are used for integrating data from specific data sources. IntegrationHub ETL guides you through importing source data, transforming any data if needed, and selecting target CMDB classes and attributes to map the data to. You then preview the integration results and adjust any configurations before scheduling recurring integrations.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view and download common integrations.

## Import data from another source using Import Sets

You can import data to the CMDB using Import Sets. [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) find files of information \(in formats such as XML, Excel, or CSV\), import them, and transform them onto the required table. This process can be scheduled or performed on demand.

To import relationships between CIs, use import sets to populate the table \[cmdb\_rel\_ci\] with information on the parent, the child, and the nature of the relationship. The \[cmdb\_rel\_ci\] table displays a list of all CI relationships and is useful when importing CI data.

![Import set overview.](../../../administer/managing-data/image/ImportSetOverview.png "Import Sets overview")

## CMDB instance API

Use the [CMDB instance API](https://www.servicenow.com/docs/access?context=cmdb-instance-api&version=australia&pubname=australia-api-reference&ft:locale=en-US) to populate the CMDB by creating or updating CMDB tables.

## Manually create a CI

Create a single CI for a specific class in CMDB Workspace,Service Graph Workspace, or in Core UI. The role required for this operation depends on the settings of the class table you select for the CI.

You can also manually create a CI while leveraging Identification and Reconciliation Engine \(IRE\) processes to ensure that the new CI complies with various class requirements and that it's unique.

1.  Use the CI Class Manager:
    1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
    2.  Select **Hierarchy** to display the list of CI Classes. Select the class to use for the CI.
    3.  In the class navigation bar, select **CI List** and then on the CI list view, select **New**.
    4.  Fill out the CI form and then select **Submit**.
2.  Or, manually create a CI while leveraging Identification and Reconciliation Engine \(IRE\) processes to ensure that the new CI complies with various class requirements and that it's unique. For more information, see [Create a CI manually in CMDB Workspace](../task/create-ci-manual-cmdb-workspace.md)or [Create a CI manually in Service Graph Workspace](../task/create-ci-manual-sg-workspace.md).
3.  Or, directly use a table:
    1.  Navigate to **All** &gt; **Configuration** and then elect the class to use for the CI, such as Business Services.
    2.  In the navigation filter of the application navigator, enter the table label \(such as 'Linux'\), or the table name in the format of &lt;table name&gt;.list \(such as 'cmdb\_ci\_linux\_server.list'\). Then, press Enter.
    3.  In the list view of the table, select **New** and fill out the form fields for the table.
    4.  Select **Submit**.

