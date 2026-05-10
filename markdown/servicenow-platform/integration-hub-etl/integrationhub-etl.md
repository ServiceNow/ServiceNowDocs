---
title: IntegrationHub ETL
description: Use the IntegrationHub ETL store app to create and manage ETL transform maps, which integrate third-party data into the CMDB or into non-CMDB tables without compromising the integrity of data. IntegrationHub ETL provides a simplified user interface that guides you through the integration process end-to-end, including a test integration run of sample data.
locale: en-US
release: australia
product: Integration Hub ETL
classification: integration-hub-etl
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# IntegrationHub ETL

Use the IntegrationHub ETL store app to create and manage ETL transform maps, which integrate third-party data into the CMDB or into non-CMDB tables without compromising the integrity of data. IntegrationHub ETL provides a simplified user interface that guides you through the integration process end-to-end, including a test integration run of sample data.

The IntegrationHub ETL \(sn\_int\_studio\) plugin provides the IntegrationHub ETL functionality.

-   Use the CMDB Integrations Dashboard to track progress, results, and errors associated with using custom integrations created in IntegrationHub ETL. The CMDB Integrations Dashboard is included in the [Integration Commons for CMDB](integration-commons-for-cmdb.md) store app.
-   Watch the [IntegrationHub ETL \| Importing resources into the CMDB](https://www.youtube.com/watch?v=YvsCY0M7JLw) video for an introduction and walk through of the IntegrationHub ETL tool.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Roles required

Users with the cmdb\_inst\_admin role can use IntegrationHub ETL to create integrations, or customize a pre-existing integration provided by ServiceNow or a vendor at the ServiceNow Store. A vendor can create a new integration and provide it as an application for anyone to use.

## Support for non-CMDB tables

Starting with the Australia release, IntegrationHub ETL supports the integration of third-party data into some non-CMDB tables. IntegrationHub ETL supports those non-CMDB tables that are supported by Identification and Reconciliation \(IRE\). For details about which non-CMDB tables are supported and any needed configuration, see [IRE support for non-CMDB tables](ire-support-non-cmdb-tables.md).

Supported non-CMDB tables are available in IntegrationHub ETL when specifying classes, conditional classes, class associations, and reference sources in mapping definitions. However, there are some differences between using CMDB classes and non-CMDB tables in IntegrationHub ETL:

-   Specifying class associations isn't mandatory for non-CMDB tables.
-   Adding relationships doesn't apply to non-CMDB tables.
-   Class associations for a non-CMDB table is based on a reference field instead of a CMDB relationship.

**Note:** Although the IntegrationHub ETL user interface and accompanying documentation references CMDB and CMDB elements, most of those references also apply to supported non-CMDB tables.

## Process

The two key components that IntegrationHub ETL uses for processing are:

-   [Robust Transform Engine \(RTE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/robust-import-set-transformers.md): Used to transform raw source data that is stored in staging tables, into the data that is mapped and integrated into the CMDB. RTE uses ETL transform maps that were created for the integration during data transformation.
-   [Identification and Reconciliation Engine \(IRE\)](ire.md): Used as a centralized framework for identification and reconciliation processes across different data sources. IRE processes help maintain data integrity in the CMDB and in supported non-CMDB tables.

IntegrationHub ETL uses RTE and IRE which work together to process and integrate data. Data is first imported from a data source, and is then stored in temporary staging tables in Import Sets systems. Using the data in the staging tables and the ETL transform map created by IntegrationHub ETL, RTE creates IRE payloads which are then processed by IRE. IRE applies reconciliation processes to avoid potential problems such as duplicate CIs, ensuring that the CMDB or non-CMDB tables remain healthy, and then integrates the resulting data.

When you create an integration, you import source data, transform data if needed, and select target CMDB classes \(or non-CMDB tables\) and attributes to map the data to. Eventually, you run an integration test of the sample data, using your settings in the IntegrationHub ETL. You can then preview the integration test results and adjust any settings before scheduling recurring integration runs for large data sets. If you develop and test the ETL transform map on a development instance, then you can test and adjust the configuration before implementation on a production instance.

For example, you can integrate data from SCCM \(Microsoft System Center Configuration Manager\).

Refer to the community page [IntegrationHub-Extract Tranform Load \(IH-ETL\) is GA in ServiceNow store](https://community.servicenow.com/community?id=community_blog&sys_id=3efdcd51dbf4d09013b5fb243996190a) for an overview of IntegrationHub ETL, including its components and workflow.

## Guided Setup

A guided setup organizes all the tasks in the correct order, tracks the completion of tasks, and enforces any task dependencies. Tasks that depend on the completion of other tasks, are enabled or disabled as you step through the tool and complete tasks.

## Read-only mode

When opening a Service Graph Connector in which IntegrationHub ETL isn't detecting any incoming data from the data source, the integration is available in read-only mode. In read-only mode you can access all the guided setup tasks on the ETL Transform Map Assistant page. You can examine all the settings and definitions in the integration even though it isn't populated with actual data. However, you can't make any updates to a read-only connection.

Read-only mode is useful for studying an existing connection for the purpose of creating a new connection that is similar to the read-only connection. The read-only mode can also assist in troubleshooting issues with the connection.

## IntegrationHub ETL and Import Sets

Using IntegrationHub ETL and ETL transform maps has the following advantages over using Import Sets and transform maps:

-   Identification and Reconciliation Engine \(IRE\) processes are incorporated into the IntegrationHub ETL so all data is automatically processed by IRE as part of the integration. Using Import Sets and transform maps does not provide a simple way to apply IRE processes.
-   IntegrationHub ETL uses guided setup which provides guidance and a simple user interface for the entire process of integrating third-party data.
-   IntegrationHub ETL includes an integration test for a small data set using the new ETL transform map. This test lets you review the results and adjust configuration settings before scheduling recurring integrations.

## Terms

The following terms are associated with the IntegrationHub ETL:

-   **CMDB application**

    Name of the third-party vendor such as SCCM 2019. A CMDB application has two associated attributes: **Name** and **Discovery Source**. When creating a new integration, ensure to configure a discovery source for the CMDB application that you plan to use, before using the IntegrationHub ETL.

-   **Data source**

    The source feed, such as SCCM 7.0 Computer Identity, where the raw source data is imported from. If you use various REST endpoints for different types of data, then each REST endpoint is associated with its own data source and an ETL transform map.

-   **ETL transform map**

    The output generated by IntegrationHub ETL. You can integrate third-party data into the CMDB or into non-CMDB tables using an ETL transform map which is configured for the respective integration.

-   **Source data**

    Original, raw data that have been imported into IntegrationHub ETL. Source data can be used in its original form, or you can transform the data before mapping and integration.

-   **Transform**

    An operation, that you can apply to a specific data column to transform the data values. For example, to transform the format of the data values. Use transforms to standardize data formats and meet other system requirements.

-   **Transformed data**

    Some of the source data might not be compliant with the requirements of its target CMDB attributes and classes or non-CMDB tables. In those cases, you can apply various types of transforms to the source data, before mapping the data to the target CMDB classes and attributes or non-CMDB tables. Transforms, can for example convert data format, replace values, and concatenate values from multiple data columns.


Each CMDB application can have multiple connections for retrieving raw data. Each connection that is used to retrieve a certain type of data, has its own pair of data source and an ETL transform map. Therefore, one CMDB application can have multiple ETL transform maps, and each of those ETL transform maps is associated with a single Data Source.

For example:

|CMDB Application|ETL Transform Map|Data Source|
|----------------|-----------------|-----------|
|SCCM|SCCM Computer Identify|/sccm/2019/comp|
|SCCM Disk|/sccm/2019/disk|
|SCCM Application|/sccm/2019/appl|

## Nested data payloads

To process nested data payloads, you must first ensure that the data source that is used for the integration, is set with the [Data in single column](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/r_DataSourceFileTypeFields.md) option. With that setting, you can correctly represent nested data in a JSON payload which IntegrationHub ETL then processes as nested data, rather than as flat data.

Sample of nested data:

```
{
            "u_computer_fqdn": "computer2-fqdn",
            "u_computer_id": 2,
            "u_computer_ip": "computer2-ip",
            "u_computer_location": "PDX",
            "u_computer_mac": "computer2-mac",
            "u_computer_name": "nested-payload-computer2",
            "u_computer_os": "computer2-os",
            "interfaces": [
                {
                    "u_interface_ip": "computer2-eth1-ip",
                    "u_interface_mac": "computer2-eth1-mac",
                    "u_interface_name": "computer2-eth1",
                    "ip": ""
                },
                {
                    "u_interface_ip": "computer2-eth2-ip",
                    "u_interface_mac": "computer2-eth2-mac",
                    "u_interface_name": "computer2-eth2",
                    "ip": {
                        "u_ip_address": "computer2-eth2-ip",
                        "u_mac_address": "computer2-eth2-mac"
                    }
                }
            ],
            "software": [
                {
                    "u_software_name": "computer2-software2",
                    "u_software_version": "computer2-software2-1.0",
                    "instance": {
                        "u_software_instance_name": "computer2-software1-instance"
                    }
                },
                {
                    "u_software_name": "computer2-software2",
                    "u_software_version": "computer2-software2-2.0",
                    "instance": {
                        "u_software_instance_name": "computer2-software2-instance"
                    }
                }
            ]
        },

```

You can view the layers of nested data in a separate panel in IntegrationHub ETL, apply transforms, map, and integrate that data into the CMDB.

When creating a nested data JSON payload, the following restrictions apply:

-   Field names must start with a letter \(between A-Z or a-z\) or with ‘\_’, and must only contain letters \(between A-Z or a-z\), digits \(0-9\), or the ‘\_’ character.

    For example, a field name can't contain special characters such as \*, \[,\], \#, $, spaces, and dot.

-   Field names can't be “temp” or “object”, which are reserved for internal use.
-   Consistently throughout the payload, you must use an array or an object to represent data in a specific level, regardless of the number of items in the level. If you use an array for multiple items in one object, you must also use an array to represent a single item in other objects.

For a demo about working with nested payload data, watch the [Integration Hub - ETL nested payload feature demo](https://youtu.be/jonkMkFiNaQ) video on the ServiceNow YouTube channel.

**Related topics**  


[Teams related list](../reference/r_RelatedListsOfCIComponents.md)

