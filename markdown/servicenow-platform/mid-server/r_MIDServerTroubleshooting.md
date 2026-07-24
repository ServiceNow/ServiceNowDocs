---
title: Resolving MID Server issues
description: Troubleshoot problems with the MID Server to find solutions. Monitor the MID Server to receive alerts about issues as they occur. Troubleshooting procedures exist to resolve specific problems with the MID Server. The Knowledge Base on Hi contains several articles to help you troubleshoot MID Server issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/r\_MIDServerTroubleshooting.html
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

-   Review the following logs for warning, critical, and severe errors: `~\agent\logs\agent0.log.0` `~\agent\logs\wrapper.txt` See [Manage ECC Queue content for a MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/ecc-queue-mid-server.md) to see how to open log entries from the instance.

-   [Test MID Server connectivity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateNetworkConnectivity.md) to confirm that the MID Server host is able to communicate with the instance. Resolve any issues with the network connectivity such as conflicts with firewalls, access control lists, and routing errors.

-   From the MID Server instance, navigate to the **MID Servers** page, and review the status of the MID Server. For additional information, click a **Name**.

-   Set up email, SMS, and push notifications to alert you when issues occur with MID servers. The **MID Server Down** notification is enabled by default. See [Notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/notifications.md) for details.


## Java Flight Recorder

Java Flight Recorder \(JFR\) uses an articulate data model to analyze Java Virtual Machine \(JVM\) internal and application specific memory usage and thread related details. On hosts with Java 14 or later, Event Streaming enables analysis of specific JVM or application events.

The JFR file actions **Start JFR Recording**, **Stop JFR Recording**, or **Write JFR File**, are accessed on the instance in the MID Server's Related Links. By starting and stopping the JFR recording, you can dump JFR data to the disk on demand. While JFR recording is on, you can write to the JFR file from the MID Server instance page.

The JFR file is deleted by a scheduler to clean the data after 24 hours. This default behavior can be overridden by adding the following configuration parameter in the **config.xml**: `<parameter name="mid.jfr.data.clean.interval" value="<time in milisec>"/>`

Custom JFR events can be written to JFR file. To disable event writing, add the following configuration parameter to the **config.xml**: `<parameter name="mid.jfr.record.aprobe" value="false”/>`

## Troubleshooting procedures

The following procedures provide information on resolving specific problems with the MID Server. Knowledge Base articles also cover a wide range of issues. If you are encountering problems which are not covered in these procedures, search the Knowledge Base for related articles. For instance, if you are experiencing symptoms such as the MID Server going down or not responding, or CIs being duplicated during discovery, see [KB0597571](https://support.servicenow.com/kb_view.do?sysparm_article=KB0597571) for information and recommended solutions.

-   **[MID Server active issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-active-issues.md)**

    The ServiceNow® instance has a dedicated table that publishes active issues with MID Servers and alerts administrators when a MID Server is in danger of exceeding its resources.

-   **[Active MID Server post-cloning credential issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-post-clone-issue-resolution.md)**

    The system provides automatic processes to detect and notify you of possible MID Server credential issues after instance cloning.

-   **[MID Server resource threshold alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-resource-threshold-alerts.md)**

    The instance displays warnings when a MID Server breaches its resource thresholds for CPU and JVM memory usage, enabling users to create email notifications or custom scripts when a breach occurs.

-   **[MID Server user connectivity issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-connectivity-issues.md)**

    The instance writes issues involving MID Server user logins and network connectivity to the MID Server Issue \[ecc\_agent\_issue\] table and creates events you can use in custom scripts or to send email notifications.

-   **[Interpreting MID Server user debugging output](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-user-connectivity-debug-output.md)**

    Debugging output from the system log is available in either a summary or detailed view for MID Server user issues, but must be enabled manually.

-   **[MID Server Upgrade History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-upgrade-history.md)**

    Use this module to troubleshoot errors that occur during the MID Server upgrade process. The MID Server Upgrade Histories table contains a record of each instance upgrade. The MID Server Upgrade Stages table shows the status of each MID Server and its upgrade progress, including any errors encountered.


-   **[MID Server active issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-active-issues.md)**  
The ServiceNow® instance has a dedicated table that publishes active issues with MID Servers and alerts administrators when a MID Server is in danger of exceeding its resources.
-   **[MID Server fails to start](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-startup-fails.md)**  
When a newly installed MID Server fails to start or shuts down prematurely, improper configuration could be to blame.
-   **[Active MID Server post-cloning credential issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-post-clone-issue-resolution.md)**  
The system provides automatic processes to detect and notify you of possible MID Server credential issues after instance cloning.
-   **[MID Server resource threshold alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-resource-threshold-alerts.md)**  
The instance displays warnings when a MID Server breaches its resource thresholds for CPU and JVM memory usage, enabling users to create email notifications or custom scripts when a breach occurs.
-   **[MID Server user connectivity issues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-connectivity-issues.md)**  
The instance writes issues involving MID Server user logins and network connectivity to the MID Server Issue \[ecc\_agent\_issue\] table and creates events you can use in custom scripts or to send email notifications.
-   **[Interpreting MID Server user debugging output](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-user-connectivity-debug-output.md)**  
Debugging output from the system log is available in either a summary or detailed view for MID Server user issues, but must be enabled manually.
-   **[MID Server Upgrade History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-upgrade-history.md)**  
Use this module to troubleshoot errors that occur during the MID Server upgrade process. The MID Server Upgrade Histories table contains a record of each instance upgrade. The MID Server Upgrade Stages table shows the status of each MID Server and its upgrade progress, including any errors encountered.

**Parent Topic:**[MID Server reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements]()

[MID Server upgrades]()

[MID Server dashboard]()

[MID Server properties]()

[MID Server parameters]()

[MID Server Configuration Parameter settings and priority]()

[MID Server File Cleaner]()

[MID Server protected records and reserved characters]()

[MID Server privileged commands]()

[MIDSystem methods]()

[Manually start, stop, and restart a MID Server]()

[MID Server heartbeat]()

[Set the MID Server JVM memory size]()

[Pause the MID Server]()

