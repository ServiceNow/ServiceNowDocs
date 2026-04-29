---
title: Agent Client Collector Log Analytics default policies and checks
description: Agent Client Collector Log Analytics provides various default policies and checks.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Agent Client Collector log policies, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector Log Analytics default policies and checks

Agent Client Collector Log Analytics provides various default policies and checks.

Streaming log data from Windows hosts is supported in Agent Client Collector Log Analytics Version 3.1.0 and later.

## Default ACC-L policies

<table id="table_pgg_n1h_drb"><thead><tr><th>

Name

</th><th>

OS

</th><th>

Description

</th><th>

Check

</th></tr></thead><tbody><tr><td>

Apache on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from Apache servers running on a Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Apache on Windows Logs

</td><td>

Windows

</td><td>

Collects logs from Apache servers running on a Windows OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

IIS logs

</td><td>

Windows

</td><td>

Collects logs from Microsoft IIS web servers and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

JBoss/WildFly Application Server on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from JBoss/WildFly application servers running on a Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

JBoss/WildFly Application Server on Windows Logs

</td><td>

Windows

</td><td>

Collects logs from JBoss/WildFly application servers running on a Windows OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Linux OS Logs

</td><td>

Linux

</td><td>

Collects logs from the Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

MSSQL on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from MSSQL DBs running on Linux and sends them to the MID Server for further analysis.

</td><td>

log\_shipper

</td></tr><tr><td>

MSSQL on Windows Logs

</td><td>

Windows

</td><td>

Collects logs from MSSQL DBs running on a Windows OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

MySQL DB on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from MySQL DBs on a Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

MySQL DB on Windows Logs

</td><td>

Windows

</td><td>

Collects logs from MySQL DBs running on a Windows OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Nginx on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from Nginx servers running on a Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Tomcat on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from Tomcat servers running on a Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Tomcat on Windows Logs

</td><td>

Windows

</td><td>

Collects logs from Tomcat servers running on a Windows OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Oracle WebLogic

</td><td>

Windows and Linux

</td><td>

Collects logs from Oracle WebLogic servers and sends them to the MID Server for further analysis.**Note:**

-   The log path that WebLogic uses has two environment variables, as described in the WebLogic documentation. For more information, see [Environment variables](acc-log-analytics-policies-checks.md#section_twh_3vd_nzb).
-   On both Windows and Linux, Agent Client Collector Log Analytics adds a default environment variable from the WebLogic documentation to the log path. You can either use this default environment variable to get the full directory, or change it manually if you prefer to use a known direct directory. For information about customizing the environment variable, see [Edit log path configurations](../task/accl-edit-log-path.md).

</td><td>

log shipper

</td></tr><tr><td>

WebSphere Application Server on Linux Logs

</td><td>

Linux

</td><td>

Collects logs from WebSphere application servers running on a Linux OS and sends them to the MID Server for further analysis.

</td><td>

log shipper

</td></tr><tr><td>

Windows OS Event Logs

</td><td>

Windows

</td><td>

Collects Windows event logs from Windows servers and sends them to the MID Server for further analysis.

</td><td>

log shipper for win events

</td></tr></tbody>
</table>## Environment variables

The log path used for collecting logs from certain servers may contain environment variables. It’s important to note that on Linux systems, the ACC Agent can only access environment variables that reside in the `/etc/environment` file. Add the environment variables that the agent must access to the `/etc/environment` file using the format **&lt;NAME&gt;='&lt;VALUE&gt;'**. On Windows systems, you can create environment variables in the usual manner.

## Default ACC-L checks

Agent Client Collector Log Analytics \(ACC-L\) provides the following default **Type=Log** checks.

-   The **log shipper** check launches a background process that sends logs from servers to an agent data input, according to the check's configured log path. When access permissions are lacking or the log path is configured incorrectly, the system sends an alert to the instance. For proper log configuration, ensure that the **servicenow** user has permissions to access the configured log path on the machine that is hosting the agent, and that the log path is configured correctly.
-   The **log shipper for win events** check is similar to the **log shipper** check, but sends event logs from Windows OS servers to the agent data input.

    **Note:** To collect Security Windows event logs, **servicenow** users on an agent hosting machine must have admin privileges.


