---
title: Configuration file tracking
description: The horizontal discovery process can find configuration files that belong to certain applications and add those configuration files to the CMDB. You can track the changes to these files by comparing them to previous versions.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 7
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Configuration file tracking

The horizontal discovery process can find configuration files that belong to certain applications and add those configuration files to the CMDB. You can track the changes to these files by comparing them to previous versions.

**Warning:** Configuration files contain sensitive system information. To prevent unauthorized access, ensure that access control lists \(ACL\) are placed on the Tracked Configuration file table \[cmdb\_ci\_config\_file\_tracked\]. Only allow authorized users to view this table or uncheck the **Save Content** setting.

## Components for configuration file tracking

-   **CI type**

    All applications and hosts in your organization must have a corresponding configuration item \(CI\) type, which is necessary for discovering and processing applications and hosts correctly. In a base system, many CI types have configuration file paths defined for them. You can add new or modify existing definitions for tracking configuration files. See [Modify tracking changes in configuration files](../task/track-configuration-files.md) for instructions.

-   **Patterns**

    Configuration file tracking is available for patterns that discover applications. On the pattern, you can create tracked file definitions that specify the CI type to which the application CI belongs and the path of the configuration file. Specify as many tracked file definitions as needed. You can also specify whether you want to save the contents of configuration files so you can view and compare the contents of different versions.

    **Note:**

    Configuration file tracking is not available for discoveries performed by traditional probes and sensors.

    The classifier that triggers the pattern must specify the Horizontal Pattern probe, which in turn, must specify the pattern. If you upgrade your instance to the current version, not all classifiers are configured to use patterns for discovery by default.

-   **CMDB**

    All configuration files are saved as a CI in the Tracked Configuration file \[cmdb\_ci\_config\_file\_tracked\] table. If you enable the content to be saved, these CI records provide the contents of the configuration files, including previous versions. From the configuration file CI record, you can compare different versions.


## Dependency maps and application service maps

Both dependency maps and service instance maps display tracked configuration files. The relationship between a configuration file and its host is a contains relationship. The application contains the configuration file.

For example, this IIS web server contains three tracked configuration files:

![CI containing racked configuration files](../image/tracked-config-file.png)

Sometimes you organize CI types as a main CI type and its related CI types. On a service instance map, Service Mapping shows changes to configuration files of related CIs for the main CIs in inclusions. In inclusions, the system treats applications hosted on a server as independent objects. For example, the Tomcat WAR CI appears separate from its host, the Tomcat CIs. In this case, Service Mapping shows changes to configuration files of Tomcat WAR when you select Tomcat. In addition, Service Mapping displays changes to configuration files of the hardware server hosting inclusions. In this example, it is a Linux server:

![Map showing an inclusion with a host](../../service-mapping/image/MapInclusionTomcat.png "Map showing an inclusion with a host")

## Deletion strategy

You can specify what you want to do with tracked configuration file CI records when discovery can no longer find them. You can keep the configuration file CI record, automatically delete it, delete only the CI relationships to it, or mark it absent.

## Discovery patterns that support configuration file tracking by default

These patterns provide tracked file definitions by default:

<table id="table_zgv_4qq_tz"><thead><tr><th>

Classifier

</th><th>

Pattern

</th><th>

CI Type

</th><th>

File path of tracked file

</th></tr></thead><tbody><tr><td>

[Apache Server](../reference/r_DataCollDiscoApacheWebServers.md#)

</td><td>

Apache On Unix Pattern Apache On Windows Pattern

</td><td>

Apache Web Server \[cmdb\_ci\_apache\_web\_server\]

</td><td>

`$config_file`

</td></tr><tr><td>

[MySQL Server](c_MySQLDiscovery.md)

</td><td>

MySQL server On Windows and Linux Pattern

</td><td>

MySQL Instance \[cmdb\_ci\_db\_mysql\_instance\]

</td><td>

`$config_file`

</td></tr><tr><td rowspan="2">

[Microsoft IIS Server](../reference/r_DataCollDiscoMicrosoftIISServers.md)

</td><td rowspan="2">

IIS

</td><td>

Microsoft iis Web Server \[cmdb\_ci\_microsoft\_iis\_web\_server\]

</td><td>

`EVAL(javascript: var rtrn = '';var winDir = CTX.getCommandManager().shellCommand("echo %WinDir%", false, null, null, CTX);rtrn = winDir.trim() + '\\System32\\Inetsrv\\Config\\*.config';)`

</td></tr><tr><td>

IIS Virtual Directory \[cmdb\_ci\_iisdirectory\]

</td><td>

`$install_directory + "\*.config"`

</td></tr><tr><td rowspan="2">

[TIBCO BusinessWorks and EMS](../../service-mapping/concept/mapping-services-tibco.md#)

</td><td>

ActiveMatrix BusinessWorks

</td><td>

ActiveMatrix Business Works \[cmdb\_ci\_appl\_tibco\_matrix\]

</td><td>

`$config_file`

</td></tr><tr><td>

Enterprise Message Service

</td><td>

Tibco Enterprise Message Service \[cmdb\_ci\_appl\_tibco\_message\]

</td><td>

`$config_file`

</td></tr><tr><td rowspan="4">

[Oracle](c_OracleDatabaseDiscovery.md)

</td><td rowspan="2">

Oracle DB on Windows Pattern

</td><td>

Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]

</td><td>

`$install_directory + "\network\admin\*.ora"`

</td></tr><tr><td>

Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]

</td><td>

`$install_directory + "\dbs\*.ora"`

</td></tr><tr><td rowspan="2">

Oracle DB on Unix Pattern

</td><td>

Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]

</td><td>

`$install_directory + "/dbs/*.ora"`

</td></tr><tr><td>

Oracle Instance \[cmdb\_ci\_db\_ora\_instance\]

</td><td>

`$install_directory + "/network/admin/*.ora"`

</td></tr><tr><td rowspan="2">

[Tomcat](../reference/r_DataCollDiscoTomcatServers.md)

</td><td rowspan="2">

Tomcat

</td><td>

Tomcat \[cmdb\_ci\_app\_server\_tomcat\]

</td><td>

`$install_directory + "/conf/server.xml"`

</td></tr><tr><td>

Tomcat WAR \[cmdb\_ci\_app\_server\_tomcat\_war\]

</td><td>

`$install_directory + "/WEB-INF/web.xml"`

</td></tr><tr><td rowspan="2">

[WMB](../reference/r_IBMWMB.md)

</td><td>

WMB On Unix Pattern

</td><td>

IBM WebSphere Message Broker \[cmdb\_ci\_appl\_ibm\_wmb\]

</td><td>

`$install_directory + "/*/etc/config/*/*.prop"`

</td></tr><tr><td>

WMB On Windows Pattern

</td><td>

IBM WebSphere Message Broker \[cmdb\_ci\_appl\_ibm\_wmb\]

</td><td>

`$install_directory + "\*\etc\config\*\*.prop"`

</td></tr><tr><td rowspan="2">

[WMQ](../reference/r-IBMWebsphereMQ.md)

</td><td>

WMQ On Windows Pattern

</td><td>

IBM MQ Manager \(formerly IBM WebSphere MQ\) \[cmdb\_ci\_appl\_ibm\_wmq\]

</td><td>

`$install_directory + "\*\config\*"`

</td></tr><tr><td>

WMQ On Windows Pattern

</td><td>

IBM MQ Manager \[cmdb\_ci\_appl\_ibm\_wmq\]

</td><td>

`$install_directory + "/bin/*.sh"`

</td></tr></tbody>
</table>## What to do

1.  Enable configuration file tracking by setting the `glide.discovery.enable_file_tracking` Discovery property to true.

    You can also configure other properties to control the size and number of tracked configuration files, the time window during which changes to configuration files are tracked for a given version, and the number of changes allowed on a configuration file during that time window. See [Discovery properties](../reference/r_DiscoveryProperties.md) for details.

2.  To prevent unauthorized access to the sensitive information from configuration files, perform the following steps:
    1.  Ensure that access control rules \(ACL\) are placed on the Tracked Configuration file table \[cmdb\_ci\_config\_file\_tracked\]. Only allow authorized users to view this table or uncheck the **Save Content** setting.
    2.  Ensuring that the tracked\_file\_reader role that controls access to configuration file data is assigned to correct users and user groups. By default, the itil role contains the tracked\_file\_reader role giving all users with the itil role access to the configuration file information.
3.  Verify that the Horizontal Discovery probe is active on the classifier for the software that you want to discovery. If not, you can enable it, specify the pattern, and then disable the other probes. See [Add the Horizontal Pattern probe to a classifier](c-UsingPatternsForHorizontalDiscovery.md#) for instructions.
4.  [Add or modify tracked file definitions](../task/track-configuration-files.md) to change the CI type or file path.
5.  [Set the tracked files deletion strategy](../task/set-config-file-deletion-strategy.md) to specify what you want to do with tracked configuration file CI records when pattern discovery can no longer find them.
6.  [Run horizontal discovery](../task/t_CreateADiscoverySchedule.md#) on the hosts that are running the applications you want to discover with patterns, open the application CI record, and check the Tracked Configuration Files related list.
7.  [Compare two versions](../../service-mapping/task/compare-configuration-files.md) of tracked CI configuration files to see the actual changes made to them.

