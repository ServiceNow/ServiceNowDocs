---
title: SAP Sybase ASE discovery
description: Discovery and Service Mapping uses the Sybase pattern to find SAP Sybase Adaptive Server Enterprise \(ASE\) databases and catalogs in your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Patterns, Discovery, Service, Mapping, Sybase, database, catalog]
breadcrumb: [Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# SAP Sybase ASE discovery

Discovery and Service Mapping uses the Sybase pattern to find SAP Sybase Adaptive Server Enterprise \(ASE\) databases and catalogs in your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date.**

    Discovery and Service Mapping Patterns

    CMDB CI Class Models

    Visibility Content

    For details on the product discovered see [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md)

    **Note:** Discovery finds Sybase Catalog that run on Linux only.

-   **Verify the configuration of OS server credentials.**
-   **Verify the configuration of the Applicative Credentials**

    When configuring the Applicative Credentials, make sure you specify `Sybase Instance [cmdb_ci_db_syb_instance]` as the CI type.

    For more information on Applicative Credentials, see Applicative credentials

-   **Verify that the user have permission to run the following commands**

    Execute the `isql` command.

    Have the Sybase environment run one of the commands:

    -   `"echo -ne 'set nocount on select name from sysdatabases\ngo\n' | " + $isql_path + " -U $$username$$ -P '$$password$$' -S " + $instance + " -w 999 -b -y " + $process.environmentVariables.SYBASE.value`
    -   `"export SYBASE=" + $process.environmentVariables.SYBASE.value + " && . " + $process.environmentVariables.SYBASE.value + "/SYBASE.sh && echo -ne 'set nocount on select name from sysdatabases\ngo\n' | " + $isql_path + " -U $$username$$ -P '$$password$$' -S " + $instance + " -w 999 -b -y " + $process.environmentVariables.SYBASE.value`
-   **Verify the configuration of a Discovery schedule**

    For detailed information, see [Running discoveries in your network](../concept/running-discoveries.md)


## Data collected during Horizontal discovery

Discovery populates the following data in the CMDB when running the Sybase pattern.

|Sybase instance \[cmdb\_ci\_db\_syb\_instance\]|
|Label|Field Name|
|-----------------------------------------------|
|-----|----------|
|Name|name|
|Version|version|
|Installation directory|install\_directory|
|Instance name|Instance|
|Configuration file|config\_file|

|Sybase Catalog \[cmdb\_ci\_db\_syb\_catalog\]|
|Label|Field Name|
|---------------------------------------------|
|-----|----------|
|Name|name|

## CI relationships

These relationships are created to support the Sybase ASE discovery.

|CI|Relationship|CI|
|---|------------|---|
|\[cmdb\_ci\_db\_syb\_instance\]|Contains::Contained by|\[cmdb\_ci\_db\_syb\_catalog\]|

**Parent Topic:**[Database discovery](../concept/database-discovery.md)

