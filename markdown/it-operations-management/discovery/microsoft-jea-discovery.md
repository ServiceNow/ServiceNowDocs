---
title: Microsoft Just Enough Administration \(JEA\) for Discovery
description: Using Microsoft JEA with Discovery improves security by forcing the MID Server to run remote Windows commands through a constrained endpoint, which validates commands on the target before execution. To configure the ServiceNow instance for Discovery with Microsoft Just Enough Administration \(JEA\), define the Windows credential with the domain name and set the MID Server configuration parameters appropriately.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Microsoft Just Enough Administration \(JEA\) for Discovery

Using Microsoft JEA with Discovery improves security by forcing the MID Server to run remote Windows commands through a constrained endpoint, which validates commands on the target before execution.

Microsoft JEA enables role-based administration through PowerShell Remoting, which uses Windows Remote Management \(WinRM\) to manage communication and authentication. This framework provides a secure and reliable method for managing computers that use the HTTP protocol. PowerShell Remoting uses two total ports \(5985, 5986\) for HTTP and HTTPS, which is easier to secure than the multiple ports used in WMI dynamic port mapping. For more information about Microsoft JEA, see [Just Enough Administration](https://docs.microsoft.com/en-us/powershell/scripting/learn/remoting/jea/overview).

## Requirements for Discovery with JEA

-   A ServiceNow instance running on the Rome release or later.
-   The MID Server and target server must be part of a Windows domain.
-   The JEA credentials with non-administrator rights must be domain level credentials.
-   PowerShell 5.0 or Windows Management Framework 5.1 must be installed on the target Windows machines.
-   PowerShell Remoting must be enabled on the target Windows machines.

**Note:** For security enhancement, starting from Rome there’s a new profile called JEA v2. Microsoft doesn’t recommend specifying any other language mode than **NoLanguage** in the JEA profile. JEA v2 explicitly sets the session type to **RestrictedRemoteServer** and the language mode to **NoLanguage** to help prevent users running arbitrary scripts at the endpoint and bypassing security restrictions. ServiceNow no longer supports the existing sample profile in KB0782125. Follow the instructions in [KB0965705](https://support.servicenow.com/kb_view.do?sysparm_article=KB0965705) to set up and deploy JEA v2 profiles.

## JEA Profiles

Discovery with JEA requires profiles composed of a PowerShell Sessions Configuration and one or more PowerShell Role Capabilities files. You can create multiple PowerShell Role Capability files and multiple user groups to assign the roles to different groups as necessary. A sample profile is provided in [KB0965705](https://support.servicenow.com/kb_view.do?sysparm_article=KB0965705) as a reference implementation and to serve as a starting point. The configuration file in the KB supports all out-of-the-box horizontal Windows patterns at the time that it was created. ServiceNow isn’t responsible for the JEA profile deployment and setup on remote machines.

The following sample profile improves security by blocking attackers if a Windows service account becomes compromised by restricting the MID Server user to execute only scripts signed by a trusted MID Server. After the profile is deployed, the connection between a MID Server and a Windows target is secured by script and parameter signatures created by the MID Server. This provides one layer of security; but monitoring on the ServiceNow instance and the MID Server itself also essential to promoting a secure deployment.

Microsoft has detailed documentation at the following links:

-   [JEA Role Capabilities](https://docs.microsoft.com/en-us/powershell/scripting/learn/remoting/jea/role-capabilities)
-   [JEA Session Configuration](https://docs.microsoft.com/en-us/powershell/scripting/learn/remoting/jea/session-configurations)

## Basic Discovery with the sample JEA Profile

The sample JEA profile provided in [KB0965705](https://support.servicenow.com/kb_view.do?sysparm_article=KB0965705) was configured to discover many basic configuration items \(CIs\) and attributes. The profile can be modified and should only serve as a baseline for Discovery with JEA.

Basic Discovery finds the following key attributes of Windows servers \(cmdb\_ci\_win\_server\) or Windows desktops \(cmdb\_ci\_computer\):

-   Hostname
-   DNS Name
-   Serial Number
-   Operating System
-   OS Version
-   OS Service Pack
-   Disk Space
-   RAM
-   CPU Core Count
-   CPU Count
-   CPU Manufacturer
-   CPU Type

It includes the following CIs:

-   Network Adaptors \(cmdb\_ci\_network\_adapter\)
-   File System \(cmdb\_ci\_file\_system\)
-   Storage Devices \(cmdb\_ci\_disk\)
-   Software Installed \(cmdb\_software\_instance\)
-   Running Processes \(cmdb\_running\_process\)
-   Memory Modules \(cmdb\_ci\_memory\_module\)
-   Serial Numbers \(cmdb\_serial\_numbers\)
-   TCP/IP Connections \(cmdb\_tcp\)
-   CI IPs \(cmdb\_ci\_ip\_address\)
-   DNS Names for CIs \(cmdb\_ci\_dns\_name\)
-   Windows Clusters \(cmdb\_ci\_win\_cluster, cmdb\_ci\_win\_cluster\_node, cmdb\_ci\_win\_cluster\_resource\)
-   Tracked Configuration Files \(cmdb\_ci\_config\_file\_tracked\)

The following application CIs can also be discovered:

-   MSSQL DB on Windows \(cmdb\_ci\_db\_mssql\_instance\)
-   MySQL DB on Windows \(cmdb\_ci\_db\_mysql\_instance\)
-   Oracle DB on Windows \(cmdb\_ci\_db\_ora\_instance\)
-   WebSphere on Windows \(cmdb\_ci\_app\_server\_websphere\)

The following probes and patterns are used for Discovery with the sample profile:

-   Windows - Classify \(probe\)
-   Windows OS - Servers \(pattern\)
-   Windows OS - Desktops \(pattern\)
-   Windows - Installed Software \(probe\)
-   Windows - ADM \(multiprobe\)
-   MySQL server On Windows \(pattern\)
-   MS SQL DB On Windows \(pattern\)
-   Oracle DB on Windows \(pattern\)
-   Windows - WebSphere - Cell \(probe\)
-   Windows - WebSphere - Web Applications \(probe\)
-   Windows - WebSphere - Web Services \(probe\)

## Prepare the instance for Discovery with JEA

To configure the ServiceNow® instance for Discovery with Microsoft Just Enough Administration \(JEA\), define the Windows credential with the domain name and set the MID Server configuration parameters appropriately.

### Before you begin

Role required: discovery\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Credentials** and click **New**.

2.  Select **Windows Credentials** from the list of available credential types.

3.  Create the credentials for the non-administrator, using this format for the **User name**: **domain\\user name**.

4.  Submit the record.

5.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

6.  Select a **MID Server** to configure from the list of MID Servers.

7.  Select the **Configuration Parameters** related list.

8.  Set the following MID Server config parameters as indicated:

    1.  **mid.windows.management\_protocol:** This parameter is required for Discovery with JEA.

        Its default value is WMI, but it must be set to WinRM on MID Servers using Discovery with JEA.

    2.  **mid.powershell.jea.endpoint**: This parameter is required for Discovery with JEA.

        This parameter specifies a JEA endpoint name which the MID Server connects to on remote hosts. The endpoint name is created when registering a configuration file, and should not be confused with the name of the configuration file itself. The setting affects the entire MID Server, including any WinRM remote sessions created by Discovery on the MID Server which go to that endpoint.

        For example, the PowerShell command **Register-PSConfiguration -name JEA\_DISCO\_V2 -path &lt;session\_configuration\_file&gt;** sets the endpoint name to JEA\_DISCO\_V2. In that case, **mid.powershell.jea.endpoint** must be updated to JEA\_DISCO\_V2.

9.  Use the following MID Server property and System property to troubleshoot issues:

    1.  **mid.probe.collect\_debug\_info**: This is an optional MID Server property to collect debug information.

        When this property is set to true, the MID Server collects credential debug info and puts it in the payload of ECC input message. It doesn't affect how JEA works.

    2.  **glide.discovery.log\_debug\_info**: This is an optional system property to collect debug information.

        When this property is set to true, the discovery sensor extracts the debug info from ECC input message and writes it to the discovery log table, so the debug information is visible when inspecting discovery status.


