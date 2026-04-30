---
title: Legacy: Altiris integration 2.0
description: The Altiris integration is deprecated in the Istanbul release.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Legacy: Altiris integration 2.0

The Altiris integration is deprecated in the Istanbul release.

The Altiris integration a one direction import of the Altiris data into ServiceNow CMDB \(Configuration management database\). The integration keeps the ServiceNow CMDB up to date with Altiris SQLServer database.

## Data Import

Relevant data is imported from the Altiris database to the CMDB. The Altiris database is not written to, it is considered an authoritative source. The import is achieved using a JDBC connection via the [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

![](../image/AltirisIntegrationApplication.png "Altiris integration application")

Information pulled from Altiris includes:

-   PC Hardware \(Model, Manufacturer, memory, clock speed, number of CPUs, etc.\)
-   Operating System Information \(Name, Service Pack\)
-   Printers
-   Disk information \(physical, network, and logical\)
-   Network \(IP Address, Netmask\)

## Configuration and Operational Modules

Enabling this integration will create the Integration - Altiris application.

The following are the configuration and operational modules for this integration.

<table id="table_ryr_qpl_nsb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Setup

</td><td>

-   Configure the data sources from one form
    -   Provide the Database Server IP Address
    -   Provide the Database Name
    -   Provide the Database User ID and Password \(this will need to be created on SQL DB side, see this article for help with this step: [http://technet.microsoft.com/en-us/library/aa337562.aspx](http://technet.microsoft.com/en-us/library/aa337562.aspx)
    -   Find and select the MID Server
-   Specify Database server settings and MID server
-   Test configuration

</td></tr><tr><td>

Scheduled Import

</td><td>

Schedule the execution of the import or import immediately

</td></tr><tr><td>

Data Sources

</td><td>

A list of the pre-configured data sources defining the external CMDB database

</td></tr><tr><td>

Progress

</td><td>

A historical list of progress on scheduled imports

</td></tr><tr><td>

Transform History

</td><td>

A historical list of transformations performed during scheduled imports

</td></tr></tbody>
</table>**Warning:** If you have activated an existing integration of the previous version:

1.  Activating the 2.0 plugin does not "add to" or "remove" anything from the existing integration.
2.  If transitioning from the old integration to this new one, considerations need to be given to customizations already done eg. mapping enhancements or using different coalesce values, these will have to be re-implemented.
3.  Both plugins could run at the same time, provided data is coalescing the same way - until there is no need for the older plugin at which time it can be turned off.

## Supported Versions

The Altiris integration only supports Altiris version 6.5. The integration does not currently Altiris version 7.0.

-   **[Legacy Import set data for Altiris](../reference/r_ImportSetData.md)**  
Learn the module names displayed by the Altiris import set data.
-   **[Legacy: Web services import set tables for Altiris](../reference/r_WebServiceImportSetTables.md)**  
This topic will list the modules that define the web service import set tables - the schema for the import set tables that are receiving the JDBC import.

**Parent Topic:**[ServiceNow provided integrations](../../vendor-specific-integrations/reference/r_ServiceNowProvidedintegrations.md)

