---
title: MID Server system requirements
description: Use these minimum system requirements to allocate resources for computers hosting MID Servers.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 16
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server system requirements

Use these minimum system requirements to allocate resources for computers hosting MID Servers.

<table id="table_mhj_csf_khb"><tbody><tr><td>

![Links to each of the MID Server sections](../image/MIDRefIconBar.png)

</td></tr></tbody>
</table>## MID Server supported systems

-   **Windows server**

    To discover Windows-based servers, run Service Mapping patterns, or execute Orchestration commands on Windows devices, the MID Server must be installed on a Windows server. The MID Server supports these Windows operating systems, including virtual machines and 64-bit systems:

    -   Windows Server 2012
    -   Windows Server 2016
    -   Windows Server 2019
    -   Windows Server 2022
    -   Windows Server 2025
-   **Linux**

    The MID Server is supported on these Linux versions for virtual machines and 64-bit systems:

    -   Linux Red Hat 6 and above
    -   Ubuntu 1404 \(Ubuntu 14\) and above
    -   CentOS 7 and above

**Note:** ServiceNow no longer supports new installations of 32-bit MID Servers or upgrades to version Rome. New MID Server installation are blocked through RPM and MSI installer on the following operating systems:

-   CentOS 7
-   Windows server 2008
-   Windows server 2008 R2
-   Windows 8
-   Windows 10

MID Servers can be manually installed to any operating system with the ZIP file, however Windows 10 is unsupported. Unsupported MID Servers auto-upgrading to Rome create an issue record in MID Server Issues \(ecc\_agent\_issue\). For more information, see [Supported platform changes for MID Server \[KB0863694\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0863694).

## Security requirements

To meet high security standards, the MID Server performs x.509 certificate validation on HTTPS traffic when connecting to ServiceNow®. If a network appliance or proxy exists between the MID Server and the instance, that appliance needs to present a digital certificate signed by a trusted CA. If you are using a self-signed certificate or a certificate signed by an internal CA, import the certificate to the MID Server trust store. For more information on adding SSL certificates, see [Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#).

## OCSP connectivity requirements

The Online Certificate Status Protocol \(OCSP\) is the protocol used to determine the revocation status of SSL/TLS certificates. When certificates are exchanged and validated, the MID Server needs to determine if the certificate has been revoked and shouldn't be trusted.

OCSP works by using a client, such as a MID Server, to receive a certificate from an HTTP website. The client sends a request to an OCSP responder: a server operated by the certificate authority \(CA\) that issued the certificate. The OCSP responder’s response to the client indicates whether the certificate is valid or has been revoked.

In order to connect, the MID Server requires access to:

-   \*.service-now.com or &lt;instance\_name&gt;.service-now.com
-   install.service-now.com
-   http://ocsp.entrust.net
-   http://ocsp.digicert.com \(or other CA OCSP Responder\)

While SSL/TLS certificates are always issued with an expiration date, there are certain circumstances in which a certificate must be revoked before it expires \(for example, if its associated private key may have been compromised\). Therefore, the current validity of a website’s certificate must always be checked by clients regardless of its expiry date.

Clients fail a connection when they can’t check the revocation status of a certificate. Firewalls and proxy configurations may block calls to the OCSP Entrust and DigiCert servers, which prevents the MID Server from working. You may need to change your firewall permissions so that the OCSP traffic goes through. For more information and resolutions, see the HI Knowledge Base article [\[KB1216223\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1216223).

## PowerShell requirements

The MID Server requires the minimum PowerShell version 3.0 and supports versions up to PowerShell 5.1. See Microsoft's documentation for more information about PowerShell requirements. To find your current PowerShell version using the instance, go to **ecc\_agent\_list.do**. Using the **Update Personalize List** gear icon, add **Host PowerShell Version** to the Selected column. Then sort the list of MID Servers by their PowerShell version to find outdated MID Servers. Alternatively, you can find the PowerShell version on the host machine by using the command **$Host.Version** in the host's PowerShell console. The PowerShell version is listed as PSVersion.

## Java version support

Java 17.0.12 is bundled with the MID Server installer package and is installed on the host for all new MID Servers. The installer automatically configures Java 17.0.12 to run in your environment. No additional configuration is required. This version supports both 64-bit Windows MID Servers and 64-bit Linux MID Servers. The MID Server requires a minimum JRE version 17.0.10, and recommended version 17.0.12. If you are using a lower version than 17.0.10, you may see encryption related issues.

Testing showed that the MID Server works as expected with Oracle Java 11 version 17.0.10. If you need to upgrade the JRE to a different version, then coordinate with the appropriate account representative for support.

Upgraded MID Servers might use different Java versions depending on their operating system versions.

-   MID Servers upgraded from earlier versions use the OpenJDK provided with the MID Server installer. This version of the OpenJDK was tested and certified for use with these MID Servers.
-   MID Servers upgraded on any other operating system versions also automatically upgrade the JRE to the version provided with the installation package.

**Note:** Linux MID Servers require glibC version 2.17. The library must be updated for JRE 11. On 64-bit Linux systems, you must install the 32-bit [GNU C library](http://www.gnu.org/software/libc/) \(glibc\). The installation command for CentOS is: `yum install glibc.i686`

## MID Server JRE downgrade support

If the ServiceNow® instance is downgraded from Quebec, then the MID Server is also downgraded. However, the JRE may not be downgraded unless the instance is downgraded to one of the following patches. ​

-   New York Patch 12
-   Orlando Patch 9
-   Paris Patch 3

If the MID Server is downgraded from Quebec to a different patch than specified, follow the instructions in [Install Java 11 on MID Servers \[KB0752451\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0752451).

## Java Service Wrapper

The MID Server installer includes the Tanuki Software Java Service Wrapper, version 3.5.40.

## Setting the JVM Memory size

The MID Server installs with 1 GB of JVM memory. If the suggested memory size for your product is greater than 1 GB, see [Set the MID Server JVM memory size](../task/t_MIDServerOptionalConfiguration.md) for the procedure to override the default setting.

## Deployment types

System requirements for your instance are determined by the needs of the individual products you use that require a MID Server. Some applications, such as [Health Log Analytics](https://www.servicenow.com/docs/access?context=hla-configuration-preferences&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), have additional system requirements listed in their documentation.

-   **Standard deployments**

    The following products are considered "standard" because their MID Servers share the same minimum disk space and memory requirements:

    -   Discovery
    -   Event Management
    -   Integrations
    -   Orchestration
    -   Service Mapping
    The minimum standard requirements pertain to both a single product and a combined product deployment. You can deploy a single MID Server for multiple standard products without significantly increasing the disk or memory requirements.

-   **High resource deployments**

    Cloud Management Platform \(CMP\) and Operational Intelligence are processing intensive and require more resources for each MID Server than the standard products. Install MID Servers for these products on dedicated hosts that do not support MID Servers for other products.


## Recommended MID Server minimum requirements

MID Server performance and system requirement are driven my multiple factors including but not limited to:

-   The size of the customer infrastructure and specific function \(Capability\) MID Server is configured to perform.
-   The number of MID Servers installed on the host.
-   The number of threads per MID Server.
-   The number and nature of other applications running on MID Server host.
-   Architectural and design enhancements over ServiceNow releases. For example, using PowerShell for Windows Discovery in Orlando or changing default Java Garbage Collection policy in Quebec.

As a result, there is no one size requirement that fits for all MID Server deployments. The following documented sizing guidelines can be a starting point for deployments. However, customers need to monitor MID Server performance and resource utilization continuously, then tune and scale up their MID Servers as needed.

-   **MID Server minimum system requirements**

    The minimum CPU configuration required for a MID Server is a quad core processor with a speed of 2+ GHz for a Windows Server 2012 R2 host with a single MID Server deployed and with standard configuration of 25 concurrent threads.

-   **MID Server CPU utilization**

    Most of the MID Server applications, such as Discovery, are designed for maximizing their performance which results in maximizing the resource utilization for the MID Server. As a result, some customers might observe very high CPU utilization segments in the range of 90-100% while the MID Server is running Discovery schedules or similar applications.

    The very high CPU utilization segments should not be a cause for concern because it aligns with architectural design of maximizing the throughput and does not have any negative impact on the Discovery performance. The MID Server host’s resource utilization automatically returns to normal after the Discovery execution successfully stops.

    Customers who notice frequent and long very high CPU utilization segments should avoid:

    -   Running more than one MID Server on same host when these MID Servers are expected to process active workloads at the same time, such as overlapping Discovery schedules.
    -   Sharing the MID Server host with other applications.
    -   Configuring performance alerts, which are purely based on CPU utilization, on MID Server host. If required, these alerts need to be used in conjunction with other performance monitors.
-   **Configuring additional performance monitoring on MID Server host**

    While CPU utilization on MID Server is a good indicator of load on the host, it gives only limited visibility. Additional monitoring with System Processor Queue Length on Windows Operating Systems and Load Averages on UNIX Operating Systems is crucial.

    -   **Processor Queue Length \(Windows OS\):** the number of threads that are ready but currently unable to run on the processor due to another active thread. A bottleneck on the processor may occur where the number of threads in the queue is more than twice the number of processor cores over a continuous period.
    -   **Load Averages \(Unix OS\):** the average system load on a Linux server for a defined period. It is the CPU demand on a server that includes sum of the running and the waiting threads. Typically, the top or the uptime command provides the load average of the server with output.

## MID Server CPU Performance Case Studies

-   **The impact of modifying number of MAX threads on MID Server CPU utilization**

    Based on internal benchmarking, the following is sample data for MID Server CPU utilization while running Cloud Discovery for 10,000 servers.![The average CPU utilization and maximum processor queue length are improved with additional threads.](../image/mid-system-req-cpu-use.png)

    In these tests, the maximum CPU utilization was observed to be 100% independent of number of threads and OS. The average CPU utilization was observed to be proportional to number of threads. Increasing number of threads did not necessarily result in immediate CPU pressure. Increasing the number of threads from the default 25 to 50 did not create additional CPU pressure, as shown by the max processor queue length. However, increasing the max threads value to 100 caused a significant increase in processor queue length, indicating CPU pressure.

-   **The impact of sharing MID Server with other applications or MID Servers on CPU utilization**

    Running Discovery is a CPU intensive operation for MID Server. Deploying other applications or MID Servers on same host creates additional CPU pressure on the host. This pressure results in a performance impact for running applications, including the MID Server. The following examples are sample CPU utilization data points for MID Server with different load patterns:

    **Dedicated host for a single MID Server:** the average CPU usage is 48%.![With a dedicated host for a single MID Server, the MID Server has an average CPU usage of 48%.](../image/mid-system-req-cpu-use-single.png)

    **Host shared between a MID Server and another application with moderate load:** the average CPU usage is 77%.![With a host sharing resources between a MID Server and an application with moderate load, the average CPU usage is 77%.](../image/mid-system-req-cpu-use-moderate.png)

    **Host shared between a MID Server and another application with heavy load:** the average CPU usage is 97%.

    ![With a host sharing resources between a MID Server and an application with heavy load, the average CPU usage is 97%.](../image/mid-system-req-cpu-use-heavy.png)

-   **Scaling up MID Server and its impact on MID Server CPU resource utilization**

    When the MID Server is heavily constrained on CPU resources, scaling up the MID Server host, by adding more CPUs, helps ease resource pressure. However, this may not necessarily eliminate the very high CPU usage segments. MID Server applications like Discovery, which are designed for maximizing the performance, will continue to use additional available CPU resources. The following examples are sample CPU utilization data points for a 4 CPU MID Server host and an 8 CPU MID Server host running same Discovery schedules:

<table id="table_dxh_shh_fqb"><tbody><tr><td>

**Parameter**

</td><td>

**4 CPU**

</td><td>

**8 CPU**

</td></tr><tr><td>

**Average CPU%**

</td><td>

48%

</td><td>

28%

</td></tr><tr><td>

**Max CPU %**

</td><td>

98%

</td><td>

98%

</td></tr></tbody>
</table>    **MID Server CPU utilization when deployed on a 4 CPU host:** ![The CPU utilization for a MID Server with a 4 CPU host.](../image/mid-system-req-cpu-use-4cpu.png)

    **MID Server CPU utilization when deployed on an 8 CPU host:** ![The CPU utilization for a MID Server with an 8 CPU host.](../image/mid-system-req-cpu-use-8cpu.png)


## Monitoring performance

To ensure that the MID Server resource allocations are sufficient for your environment, monitor performance during peak periods of product execution from the [MID Server dashboard](../concept/c_MIDServerDashboard.md).

**Parent Topic:**[MID Server reference](../concept/mid-server-reference-information.md)

**Related topics**  


[MID Server upgrades](../concept/c_UpgradeAndTestMIDServer.md)

[Resolving MID Server issues](r_MIDServerTroubleshooting.md)

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

