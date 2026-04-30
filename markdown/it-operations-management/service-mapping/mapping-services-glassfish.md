---
title: Mapping application services containing Oracle GlassFish Servers
description: Service Mapping can discover application services containing Oracle GlassFish Servers.Map an service instance containing an Oracle GlassFish Server correctly.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Mapping application services containing Oracle GlassFish Servers

Service Mapping can discover application services containing Oracle GlassFish Servers.

## Discovered components

<table id="table_str_3pr_rgb"><thead><tr><th>

Name

</th><th>

Platform

</th><th>

Version

</th><th>

Protocol

</th><th>

Discovery type

</th><th>

Pattern \(or probe if indicated\)

</th></tr></thead><tbody><tr id="glassfish-supported-app"><td>

[Oracle GlassFish Server](mapping-services-glassfish.md#)

</td><td>

Windows

 UNIX

</td><td>

3.1, 4.0, 4.1

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

GlassFish Server

</td></tr><tr><td>

Oracle GlassFish WAR file

</td><td>

Windows

 UNIX

</td><td>

3.1, 4.0, 4.1

</td><td>

WMI

 WinRM

 SSH

</td><td>

Horizontal and top-down

</td><td>

GlassFish WAR

</td></tr></tbody>
</table>**Parent Topic:**[Map a single application service using classic Service Mapping](../task/t_DefineNewBusinessService.md)

## Map application services containing Oracle GlassFish Servers

Map an service instance containing an Oracle GlassFish Server correctly.

### Before you begin

-   \(If hosted on a Windows server\) On the ServiceNow AI Platform, configure [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   \(If hosted on a Linux or UNIX server\) \(Optional\) on the ServiceNow AI Platform, configure [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).
-   \(Optional\) For discovering using the WinRM protocol, see [Configure WinRM trusted hosts on MID Server](https://www.servicenow.com/docs/access?context=enable-winRM-MID-servers&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

Role required: service\_mapping\_admin

### Procedure

1.  Create a service instance.

    1.  Navigate to **All** &gt; **Service Mapping** &gt; **Service Instances**.

    2.  Click **New**.

        The **Discoverable by Service Mapping** option is selected by default.

    3.  In the **Name** field, enter a descriptive name for the service instance.

2.  Define the entry point for this application service:

    1.  Select the **Other Application** tile.

        The **Discoverable by Service Mapping** option is selected by default.

    2.  Define the entry point by filling in the fields.

<table id="table_dr1_ktx_ygb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select Entry Point Type

</td><td>

Entry point type: -   HTTP\(S\) Endpoint
-   TCP Endpoint
-   Tibco BW Endpoint


</td></tr><tr><td>

URL

</td><td>

The URL of the process that correlates with the GlassFish Server, for example, `http://10.196.xx.xx:28080/hello/`.This field appears when **HTTP\(S\) Endpoint** is selected in **Select Entry Point Type**.

</td></tr><tr><td>

Host

</td><td>

The server that hosts the GlassFish Server.This field appears when **Tibco BW Endpoint** or **TCP Endpoint** is selected in **Select Entry Point Type**.

</td></tr><tr><td>

Host Name

</td><td>

The host name of the server that hosts the GlassFish Server. This field appears when **HTTP\(S\) Endpoint** is selected in **Select Entry Point Type**.

</td></tr><tr><td>

Port

</td><td>

The port, which the process correlating with the GlassFish Server uses.This field appears when **Tibco BW Endpoint**o r **TCP Endpoint** is selected in **Select Entry Point Type**.

</td></tr><tr><td>

Process Name

</td><td>

The name of the process that correlates with the GlassFish Server.This field appears when **Tibco BW Endpoint** is selected in **Select Entry Point Type**.

</td></tr><tr><td>

Comments

</td><td>

Free text comment to provide information on the endpoint.This field appears when **HTTP\(S\) Endpoint** or **TCP Endpoint** is selected in **Select Entry Point Type**.

</td></tr></tbody>
</table>    3.  Click **Add**.

    4.  Click **Save**.

3.  Click **Additional Info** on the left and clear the **Traffic based discovery** check box.

4.  Click **Update**.

5.  Verify that the mapping result is satisfactory:

    1.  Click **View Map** and wait until the mapping is complete.

        It may take a few minutes.

    2.  Review the application service map and make sure that the service layout is as in the following example.

        ![Application service including a GlassFish server.](../image/GlassFish-components.png)

    In addition, verify that the GlassFish Server CIs are inclusions, each of which contains a WAR file.


If the mapping result is not as you expected, perform basic troubleshooting.

<table id="table_glassfish_troubleshooting"><thead><tr><th>

Symptom

</th><th>

Cause

</th><th>

Solution

</th></tr></thead><tbody><tr><td>

Service Mapping fails to discover the GlassFish Server CI. The discovery log displays the following message: Process is not running or port is not correctFailed to identify CI due to the host 10.196.xx.xx lacking an application running on port 28080. Make sure that the application is running and run quick discovery on the host.

</td><td>

There is no process running on the port that is part of the entry point.

</td><td>

1.  Make sure that the entry point is correct.
2.  If the entry point is correct, check that here is a process running on the port by running a quick discovery on the host.

</td></tr></tbody>
</table>