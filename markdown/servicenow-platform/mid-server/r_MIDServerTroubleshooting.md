---
title: Resolving MID Server issues
description: Troubleshoot problems with the MID Server to find solutions. Monitor the MID Server to receive alerts about issues as they occur. Troubleshooting procedures exist to resolve specific problems with the MID Server. The Knowledge Base on Hi contains several articles to help you troubleshoot MID Server issues.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Resolving MID Server issues

Troubleshoot problems with the MID Server to find solutions. Monitor the MID Server to receive alerts about issues as they occur. Troubleshooting procedures exist to resolve specific problems with the MID Server. The Knowledge Base on Hi contains several articles to help you troubleshoot MID Server issues.

## Monitor the MID Server

Monitoring a MID Server involves verifying entries in log files, confirming network connectivity, and checking MID server status.

-   If the MID Server is on a Windows host, navigate to the Windows Services console, locate the service name that matches the name that appears from the `wrapper-override.conf` file. If the MID Server process is the only Java process running on the host, monitor the memory used by java.exe and alert on less than the maximum configured memory defined in the `~\agent\conf\wrapper-override.conf` folder.

-   Ensure that the `agent0.log.0.lck` file appears in the `~\agent\logs` folder to confirm that the MID Server running and logging system activity in the `agent0.log.0` file.

-   Review the following logs for warning, critical, and severe errors: `~\agent\logs\agent0.log.0` `~\agent\logs\wrapper.txt` See [Manage ECC Queue content for a MID Server](../concept/ecc-queue-mid-server.md#) to see how to open log entries from the instance.

-   [Test MID Server connectivity](../task/t_ValidateNetworkConnectivity.md) to confirm that the MID Server host is able to communicate with the instance. Resolve any issues with the network connectivity such as conflicts with firewalls, access control lists, and routing errors.

-   From the MID Server instance, navigate to the **MID Servers** page, and review the status of the MID Server. For additional information, click a **Name**.

-   Set up email, SMS, and push notifications to alert you when issues occur with MID servers. The **MID Server Down** notification is enabled by default. See Notifications for details.


## Java Flight Recorder

Java Flight Recorder \(JFR\) uses an articulate data model to analyze Java Virtual Machine \(JVM\) internal and application specific memory usage and thread related details. On hosts with Java 14 or later, Event Streaming enables analysis of specific JVM or application events.

The JFR file actions **Start JFR Recording**, **Stop JFR Recording**, or **Write JFR File**, are accessed on the instance in the MID Server's Related Links. By starting and stopping the JFR recording, you can dump JFR data to the disk on demand. While JFR recording is on, you can write to the JFR file from the MID Server instance page.

The JFR file is deleted by a scheduler to clean the data after 24 hours. This default behavior can be overridden by adding the following configuration parameter in the **config.xml**: `<parameter name="mid.jfr.data.clean.interval" value="<time in milisec>"/>`

Custom JFR events can be written to JFR file. To disable event writing, add the following configuration parameter to the **config.xml**: `<parameter name="mid.jfr.record.aprobe" value="false”/>`

## Troubleshooting procedures

The following procedures provide information on resolving specific problems with the MID Server. Knowledge Base articles also cover a wide range of issues. If you are encountering problems which are not covered in these procedures, search the Knowledge Base for related articles. For instance, if you are experiencing symptoms such as the MID Server going down or not responding, or CIs being duplicated during discovery, see [KB0597571](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597571) for information and recommended solutions.

-   **[MID Server active issues](../concept/mid-server-active-issues.md)**

    The ServiceNow® instance has a dedicated table that publishes active issues with MID Servers and alerts administrators when a MID Server is in danger of exceeding its resources.

-   **[Active MID Server post-cloning credential issues](mid-post-clone-issue-resolution.md)**

    The system provides automatic processes to detect and notify you of possible MID Server credential issues after instance cloning.

-   **[MID Server resource threshold alerts](mid-resource-threshold-alerts.md)**

    The instance displays warnings when a MID Server breaches its resource thresholds for CPU and JVM memory usage, enabling users to create email notifications or custom scripts when a breach occurs.

-   **[MID Server user connectivity issues](mid-server-connectivity-issues.md#)**

    The instance writes issues involving MID Server user logins and network connectivity to the MID Server Issue \[ecc\_agent\_issue\] table and creates events you can use in custom scripts or to send email notifications.

-   **[Interpreting MID Server user debugging output](mid-user-connectivity-debug-output.md)**

    Debugging output from the system log is available in either a summary or detailed view for MID Server user issues, but must be enabled manually.

-   **[MID Server Upgrade History](../concept/mid-server-upgrade-history.md)**

    Use this module to troubleshoot errors that occur during the MID Server upgrade process. The MID Server Upgrade Histories table contains a record of each instance upgrade. The MID Server Upgrade Stages table shows the status of each MID Server and its upgrade progress, including any errors encountered.


-   **[MID Server active issues](../concept/mid-server-active-issues.md)**  
The ServiceNow® instance has a dedicated table that publishes active issues with MID Servers and alerts administrators when a MID Server is in danger of exceeding its resources.
-   **[MID Server fails to start](mid-startup-fails.md)**  
When a newly installed MID Server fails to start or shuts down prematurely, improper configuration could be to blame.
-   **[Active MID Server post-cloning credential issues](mid-post-clone-issue-resolution.md)**  
The system provides automatic processes to detect and notify you of possible MID Server credential issues after instance cloning.
-   **[MID Server resource threshold alerts](mid-resource-threshold-alerts.md)**  
The instance displays warnings when a MID Server breaches its resource thresholds for CPU and JVM memory usage, enabling users to create email notifications or custom scripts when a breach occurs.
-   **[MID Server user connectivity issues](mid-server-connectivity-issues.md#)**  
The instance writes issues involving MID Server user logins and network connectivity to the MID Server Issue \[ecc\_agent\_issue\] table and creates events you can use in custom scripts or to send email notifications.
-   **[Interpreting MID Server user debugging output](mid-user-connectivity-debug-output.md)**  
Debugging output from the system log is available in either a summary or detailed view for MID Server user issues, but must be enabled manually.
-   **[MID Server Upgrade History](../concept/mid-server-upgrade-history.md)**  
Use this module to troubleshoot errors that occur during the MID Server upgrade process. The MID Server Upgrade Histories table contains a record of each instance upgrade. The MID Server Upgrade Stages table shows the status of each MID Server and its upgrade progress, including any errors encountered.

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements](r_MIDServerSystemRequirements.md)

[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[MID Server dashboard](../concept/c_MIDServerDashboard.md)

[MID Server properties](r_MIDServerProperties.md#)

[MID Server parameters](mid-server-parameters.md#)

[MID Server Configuration Parameter settings and priority](mid-config-param-priority.md)

[MID Server File Cleaner](../concept/mid_file_cleaner.md)

[MID Server protected records and reserved characters](mid-server-reserved-characters.md)

[MID Server privileged commands](../concept/c_PrivilegedCommandsForMIDServer.md#)

[MIDSystem methods](r_MIDSystemMethods.md)

[Manually start, stop, and restart a MID Server](../task/t_InstallMIDServerAsWinService.md)

[MID Server heartbeat](r_MIDServerHeartbeat.md)

[Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md)

[Pause the MID Server](../task/t_PauseTheMIDServer.md#)

