---
title: IBM WebSphere Application Server discovery using patterns
description: The Discovery and Service Mapping Patterns application uses the Websphere On Windows and Websphere On Unix patterns to find IBM WebSphere Application Servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-02-16"
reading_time_minutes: 4
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM WebSphere Application Server discovery using patterns

The Discovery and Service Mapping Patterns application uses the Websphere On Windows and Websphere On Unix patterns to find IBM WebSphere Application Servers. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

The IBM WebSphere Application Server is a software framework with middleware that hosts Java-based web applications. Discovery identifies and classifies information about the IBM WebSphere Application Server on both Windows and Linux computers.

**Note:** Starting with Visibility Content version 6.1.0, pattern-based discovery is the default method for discovering IBM WebSphere Application Servers. The WebSphere probes are disabled by default. For more information, see [IBM WebSphere server discovery using probes](../../discovery/concept/c_DataCollDiscoWebSphereServers.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites for Windows discovery

-   **Verify that the following applications are up to date:**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Enable PowerShell on the MID Server**

    For more information, see [Set up MID Servers to use PowerShell](../../discovery/task/t_SetUpAMIDServerToUsePowerShell.md).

-   **Verify access to files and directories**

    Verify access to the following files and directories:

    -   Installation directory of the product
    -   Configuration directory of the product
    -   `versionInfo.bat`
    -   `WAS.product`
    -   `BASE.product`
    -   `profile.version`
    -   `Express.product`
    -   `application.xml`
    -   `server.xml`
    -   `cell.xml`
-   **Create Windows credentials**

    For more information, see [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md).


## Prerequisites for Linux discovery

-   **Verify that the following applications are up to date:**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Enable SSH on WebSphere Application Server**

    For more information, see the "Setting up SSH on Linux or UNIX servers" article in the "WebSphere Automation" section of the IBM documentation \([https://www.ibm.com/docs/en/products](https://www.ibm.com/docs/en/products)\).

-   **Verify access to files and directories**

    Verify access to the following files and directories:

    -   Installation directory of the product
    -   Configuration directory of the product
    -   `oeconsol`
    -   `WAS_HOME`
    -   `CONFIG_ROOT`
    -   `versionInfo.sh`
    -   `WAS.product`
    -   `BASE.product`
    -   `profile.version`
    -   `Express.product`
    -   `application.xml`
    -   `server.xml`
    -   `cell.xml`
-   **Create SSH credentials**

    For more information, see [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

-   **Verify elevated rights for IBM WebSphere Application Server commands**

    For more information, see IBM WebSphere Application Server \(on UNIX\) table in [Service Mapping commands requiring a privileged user](r_CommandsnCredentials.md).

-   **Schedule a horizontal discovery**

    For more information, see [Schedule a horizontal discovery](../../discovery/task/t_CreateADiscoverySchedule.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Websphere On Windows and Websphere On Unix patterns.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the WebSphere Application Server.|
|Version \[version\]|Current version of the WebSphere Application Server.|
|Node \[node\]|Name of the Node grouping the WebSphere Application Server or servers.|
|Cell \[cell\]|Name of the cell grouping one or more nodes of the WebSphere Application Server.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the enterprise application archive \(EAR\) file.|
|Installation directory \[install\_directory\]|Installation directory of the EAR file.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the web service.|
|Service ID \[service\_id\]|ID of the web service.|
|Attributes \[attributes\]|Additional attributes of the web service.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the WebSphere cell.|
|Cell ID \[cell\_id\]|ID of the WebSphere cell.|
|Cell type \[cell\_type\]|Type of the WebSphere cell.|
|Cell discovery protocol \[cell\_discovery\_protocol\]|Cell discovery protocol.|
|Description \[short\_description\]|Description of the cell, if one has been provided. This field is populated in Linux discovery only.|

## CI relationships

Discovery creates these relationships to support the WebSphere Application Server discovery for both Windows and Linux systems.

|CI|Relationship|CI|
|---|------------|---|
|IBM Websphere \[cmdb\_ci\_app\_server\_websphere\]|Contains::Contained by|Websphere Cell \[cmdb\_ci\_websphere\_cell\]|
|IBM Websphere \[cmdb\_ci\_app\_server\_websphere\]|Contains::Contained by|Websphere EAR \[cmdb\_ci\_app\_server\_ws\_ear\]|
|Web Service \[cmdb\_ci\_web\_service\]|Runs on::Runs|IBM Websphere \[cmdb\_ci\_app\_server\_websphere\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

