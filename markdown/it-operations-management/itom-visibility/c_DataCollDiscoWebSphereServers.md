---
title: IBM WebSphere server discovery using probes
description: The IBM WebSphere application server is a software framework with middleware that hosts Java-based web applications. Discovery creates or updates a CMDB record when it detects an instance of a WebSphere application server running on a Windows or Linux system.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM WebSphere server discovery using probes

The IBM WebSphere application server is a software framework with middleware that hosts Java-based web applications. Discovery creates or updates a CMDB record when it detects an instance of a WebSphere application server running on a Windows or Linux system.

**Note:** Starting with Visibility Content version 6.1.0, pattern-based discovery is the default method for discovering IBM WebSphere Application Servers. The WebSphere probes are disabled by default. For more information, see [IBM WebSphere Application Server discovery using patterns](../../service-mapping/reference/ibm-websphere-server-pattern.md).

## Websphere discovery on Windows

Requirements for discovery:

For WebSphere application servers running on Windows systems, enable [PowerShell](../task/t_SetUpAMIDServerToUsePowerShell.md) on the MID Server.

## Websphere discovery on Linux

Requirements for discovery:

-   Enable SSH on the WebSphere Application Server.
-   Set execute privileges to enable the following probes to run commands:
    -   WebSphere - Get serverindex.xml: cat/read permissions on the `serverindex.xml` file
    -   WebSphere - Get cell.xml: cat/read permissions on the `cell.xml` file
    -   WebSphere - Get server.xml: cat/read permissions on the `server.xml` file

For a list of privileged commands that you need for Discovery and Service Mapping, see [Service Mapping commands requiring a privileged user](../../service-mapping/reference/r_CommandsnCredentials.md). This list includes commands that require elevated rights to discover and map Unix-based hosts in your organization.

## Probes and sensors

Discovery uses this process to identify Linux WebSphere application servers:

1.  The Unix - Active Processes probe detects a running process that matches the **com.ibm.ws.runtime.WsServer**. For example, the **...com.ibm.ws.bootstrap.WSLauncher com.ibm.ws.runtime.WsServer** process output has a parameter of **/opt/IBM/WPS/profiles/ccmdb/config localhostNode01Cell ccmdb01 server1**. The values are:
    -   last parameter = server\_name = server1
    -   last parameter - 1 = node\_name = ccmdb01
    -   last parameter - 2 = cell\_name = localhostNode01Cell
    -   last parameter - 3 = config\_path = ‘/opt/IBM/WPS/profiles/ccmdb/config’
2.  If there is a match, a record is created in the IBM Websphere \[cmdb\_ci\_app\_server\_websphere\] table. The following probes are triggered:
    -   WebSphere - Cell
    -   WebSphere - Web Applications
    -   WebSphere –Web Services
3.  The WebSphere - Cell probe searches for the `cell.xml` file for the instance by using the parameters in the running process, and then searching in the related `<config_path>\cells\<cell_name>\` directory.
4.  If the probe successfully finds the `cell.xml` file, the sensor reads its contents and populates additional Websphere Cell \[cmdb\_ci\_websphere\_cell\] table records as necessary.
5.  If the probe successfully finds the `serverindex.xml` file, the sensor reads its contents and populates additional Web Application \[cmdb\_ci\_web\_application\] table records as necessary.
6.  If the probe successfully finds the `server.xml` file, the sensor reads its contents and populates additional Web Service \[cmdb\_ci\_web\_service\] table records as necessary.

Discovery uses this process to identify Windows WebSphere application servers:

1.  The Windows - Active Processes probe detects a running process that matches the **com.ibm.ws.runtime.WsServer**. For example, the **...com.ibm.ws.bootstrap.WSLauncher com.ibm.ws.runtime.WsServer** process output has a parameter of **/opt/IBM/WPS/profiles/ccmdb/config localhostNode01Cell ccmdb01 server1**. The values are:
    -   last parameter = server\_name = server1
    -   last parameter - 1 = node\_name = ccmdb01
    -   last parameter - 2 = cell\_name = localhostNode01Cell
    -   last parameter - 3 = config\_path = ‘/opt/IBM/WPS/profiles/ccmdb/config’
2.  If there is a match, a record is created in the IBM Websphere \[cmdb\_ci\_app\_server\_websphere\] table. The following probes are triggered:
    -   Windows - WebSphere - Cell
    -   Windows - WebSphere - Web Applications
    -   Windows - WebSphere –Web Services
3.  The Windows - WebSphere - Cell probe searches for the `cell.xml` file for the instance by using the parameters in the running process, and then searching in the related `<config_path>\cells\<cell_name>\` directory.
4.  If the probe successfully finds the `cell.xml` file, the sensor reads its contents and populates additional Websphere Cell \[cmdb\_ci\_websphere\_cell\] table records as necessary.
5.  The Windows - WebSphere - Web Applications probe searches the `serverindex.xml` file for the instance by using the parameters in the running process, and then searching in the related `<config_path>\cells\<cell_name>\nodes\<node_name>` directory.
6.  If the probe successfully finds the `serverindex.xml` file, the sensor reads its contents and populates additional Web Application \[cmdb\_ci\_web\_application\] table records as necessary.
7.  The Windows WebSphere - Web Services probe searches for the `server.xml` file for the instance by using the parameters in the running process, and then searching in the related`<config_path>\cells\<cell_name>\nodes\<node_name>\servers\<server_name>` directory.
8.  If the probe successfully finds the `server.xml` file, the sensor reads its contents and populates additional Web Service \[cmdb\_ci\_web\_service\] table records as necessary.

## Data collected

|Table|Field|Source|
|-----|-----|------|
|cmdb\_ci\_app\_server\_websphere|Name \(name\)|Running process|
|cmdb\_ci\_websphere\_cell|Name \(name\)|cell.xml|
|cmdb\_ci\_websphere\_cell|Cell ID \(cell\_id\)|cell.xml|
|cmdb\_ci\_websphere\_cell|Cell type \(cell\_type\)|cell.xml|
|cmdb\_ci\_websphere\_cell|Cell discovery protocol \(cell\_discovery\_protocol\)|cell.xml|
|cmdb\_ci\_web\_service|Name \(name\)|server.xml|
|cmdb\_ci\_web\_service|Service ID \(service\_id\)|server.xml|
|cmdb\_ci\_web\_application|Name \(name\)|serverindex.xml|

|Label|Table Name|Field Name|Source|
|-----|----------|----------|------|
|Name|cmdb\_ci\_websphere\_cell|name|server.xml|
|App server|cmdb\_ci\_web\_service|app\_server|Internal reference|
|Name|cmdb\_ci\_web\_service|name|server.xml|
|Name|cmdb\_ci\_web\_application|name|serverindex.xml|
|App server|cmdb\_ci\_web\_application|app\_server|serverindex.xml|

## Relationships

These relationships are created in the CI Relationship \[cmdb\_rel\_ci\] table.

|Parent class|Relationship type|Child class|
|------------|-----------------|-----------|
|cmdb\_ci\_app\_server\_websphere|Runs on::Runs|cmdb\_ci\_linux\_server|
|cmdb\_ci\_win\_server|Runs on::Runs|cmdb\_ci\_win\_server|
|cmdb\_ci\_app\_server\_websphere|Contains::Contained by|cmdb\_ci\_web\_application|
|cmdb\_ci\_web\_service|Runs on::Runs|cmdb\_ci\_app\_server\_websphere|
|cmdb\_ci\_websphere\_cell|Contains::Contained by|cmdb\_ci\_app\_server\_websphere|

**Parent Topic:**[Software discovery](c_Software.md)

