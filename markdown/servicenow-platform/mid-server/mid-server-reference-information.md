---
title: MID Server reference
description: MID Server reference information includes system requirements and other information you need to configure a MID Server for your specific needs.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server reference

MID Server reference information includes system requirements and other information you need to configure a MID Server for your specific needs.

-   **[MID Server system requirements](../reference/r_MIDServerSystemRequirements.md)**  
Use these minimum system requirements to allocate resources for computers hosting MID Servers.
-   **[MID Server upgrades](c_UpgradeAndTestMIDServer.md)**  
Upgrade MID Servers manually, or automatically through the instance. MID Server automatic upgrade is triggered when the instance upgrades and the MID Server no longer has the same version. The new MID Server package is downloaded from install.service-now.com, replaces the old one, and the MID Server starts with the new version.
-   **[Resolving MID Server issues](../reference/r_MIDServerTroubleshooting.md)**  
Troubleshoot problems with the MID Server to find solutions. Monitor the MID Server to receive alerts about issues as they occur. Troubleshooting procedures exist to resolve specific problems with the MID Server. The Knowledge Base on Hi contains several articles to help you troubleshoot MID Server issues.
-   **[MID Server dashboard](c_MIDServerDashboard.md)**  
The MID Server dashboard is a central place for MID Server users to monitor ongoing operations. The dashboard consists of reports and gauges that display information from the MID Server Status table.
-   **[MID Server properties](../reference/r_MIDServerProperties.md#)**  
Properties control the behavior of all MID Servers or a particular MID Server.
-   **[MID Server parameters](../reference/mid-server-parameters.md#)**  
Parameters control the behavior of a particular MID Server and have lower precedence than MID Server properties.
-   **[MID Server Configuration Parameter settings and priority](../reference/mid-config-param-priority.md)**  
The MID Server's settings reside in multiple tables and the MID Server prioritizes them in a set order. MIDConfigParameter must be defined with the correct type-style builders.
-   **[MID Server File Cleaner](mid_file_cleaner.md)**  
A monitor thread runs in the MID Server to clean up old files, to keep the size and quantity of files within the install folder manageable, and to prevent performance issues with the MID Servers.
-   **[MID Server protected records and reserved characters](../reference/mid-server-reserved-characters.md)**  
Some MID Server records cannot be altered. Certain special characters are pre-defined in XML and cannot be used in passwords.
-   **[MID Server privileged commands](c_PrivilegedCommandsForMIDServer.md#)**  
To discover certain information on a host server, the MID Server must run SSH commands with higher privileges. The platform provides default privileged commands for the MID Server to use and the ability to add additional commands to the system.
-   **[MIDSystem methods](../reference/r_MIDSystemMethods.md)**  
MIDSystem variables \(referred to by the variable name ms.\) provide a variety of methods to get information about the MID Server.
-   **[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)**  
If you did not start the MID Server at the end of the installation procedure, you can manually start the MID Server.
-   **[MID Server heartbeat](../reference/r_MIDServerHeartbeat.md)**  
The instance checks the MID Server for a response every 5 minutes, using a synthetic transaction monitoring system.
-   **[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)**  
The MID Server starts with a default JVM memory allocation, but you can modify this setting in the configuration file.
-   **[Pause the MID Server](../task/t_PauseTheMIDServer.md#)**  
Pause the MID Server to temporarily prevent it from polling the ECC Queue for work or sending Discovery results back to the instance.

**Parent Topic:**[Manage instance data sources](../../../administer/general/concept/manage-data-sources.md)

