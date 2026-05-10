---
title: Application Dependency Mapping \(ADM\) for Discovery
description: Application Dependency Mapping \(ADM\) discovers CIs by detecting TCP connections between devices.Using properties, you can enable or disable ADM discovery, and you can set the location of the TCP tracking file for enhanced ADM.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Application Dependency Mapping \(ADM\) for Discovery

Application Dependency Mapping \(ADM\) discovers CIs by detecting TCP connections between devices.

When ADM discovery is enabled, Discovery always runs the ADM probes during the exploration stage to find the TCP traffic on your network. Using these TCP connections, Discovery can find additional CIs and create relationships between them.

IPv6 Is supported for ADM.

**Note:** Currently, ADM does not support multi-languages. If values returned are not in English, the returned data cannot be parsed properly and the discovery will fail.

## Standard and enhanced ADM discovery

-   **Standard ADM discovery**

    Triggers an ADM probe to take a single snapshot of TCP connections on target machines using `netstat` and `lsof` commands. However, it does not detect new TCP connections that occur between these 24-hour intervals.

    Standard ADM discovery is enabled by default.

-   **Enhanced ADM \(ADME\) discovery**

    Triggers an enhanced ADM probe that installs a script on host machines on which Discovery takes regular samples of active TCP connections. You can use a set of properties and probe parameters that control several aspects of enhanced ADM discovery.

    ADME discovery is not enabled by default.


Service Mapping uses the ADM probes for traffic-based discovery. See [Discovery based on Predictive Intelligence](../../service-mapping/concept/predictive-intelligence-discovery.md) for more information.

## Requirements

Both standard and enhanced ADM discovery support the following operating systems:

-   Windows
-   Unix
-   Solaris \(On Solaris machines, enhanced ADM is available in global zones. Only standard ADM is available for local zones.\)
-   AIX
-   HP-UX

To use the WMI protocol, [version 3.0 of PowerShell](r_PowerShellForDiscovery.md) is required.

**Note:**

If you set your Windows server Execution Policy to RemoteSigned or AllSigned, ADME can run PowerShell scripts. You must import the ServiceNow certificate to the trusted publisher in order for the scripts to execute properly.

## TCP tracking file for enhanced ADM

The first time that Discovery launches the enhanced probe, no TCP information is gathered. Rather, the enhanced probe only deploys the TCP tracking file, in which information about detected TCP connections is saved. After Discovery runs again, the enhanced probe relays the contents of the TCP tracking file back to the instance via the MID Server. The information is saved in the CMDB.

The TCP tracking file is saved in these locations by default:

-   Windows: `admin$\temp\{your_instance_name}`. While TCP connections are being monitored, the information is stored in memory and then later saved to the file.
-   Linux: `/tmp/{your_instance_name}`.

You can change the location and other aspects of the tracking file with ADM properties.

If you disable enhanced ADM, Discovery cleans up the folders from the host file system the next time Discovery runs, but the TCP tracking file remains.

## Requirements for Enhanced ADM on Linux machines

Modify the sudoers file to include these commands:

-   **Windows**
    -   Utility tool support: netstat
    -   Required sudoer commands: None
    -   Additional requirements: None
-   **AIX**
    -   Utility tool support:
        -   netstat
        -   lsof \(if netstat does not work\)
    -   Required sudoer commands:
        -   `Cmnd_Alias ADME_CMDS=/usr/bin/netstat -Aan, /usr/sbin/lsof -iTCP -n -P`
        -   `discoUser ALL=(root)NOPASSWD:ADME_CMDS`
        -   `Defaults:discoUser ! requiretty`
    -   Additional requirements: None
-   **Solaris**
    -   Utility tool support:
        -   netstat \(for Solaris version 11.2\)
        -   lsof \(for Solaris versions prior to 11.2\)
    -   Required sudoer commands:
        -   `Cmnd_Alias ADME_CMDS = /usr/bin/netstat,/opt/csw/bin/lsof -iTCP -n -P -zglobal`
        -   `discoUser ALL=(root) NOPASSWD:ADME_CMDS`
        -   `Defaults!ADME_CMDS !requiretty`
        -   `Cmnd_Alias ADME_PS = /usr/ucb/ps`
        -   `discoUser ALL=(root) NOPASSWD:ADME_PS`
        -   `Disco ALL=(root) /usr/bin/pfiles`
        -   `Disco ALL=(root) /usr/bin/pgrep`
        -   `Defaults!ADME_PS !requiretty`

            **Note:** You must add **-zglobal** for lsof to run.

    -   Additional requirements: Add the lsof path to the secure path. For example, if the path to lsof is `/opt/csw/bin`, the secure path should be `secure_path = /usr/bin:/usr/sbin:/bin:/sbin:/opt/csw/bin`

        **Note:** The commands with `PS` apply to standard ADM as well as enhanced ADM.

-   **HP-UX**
    -   Utility tool support: lsof
    -   Required sudoer commands:
        -   `Cmnd_Alias ADME_CMDS = /usr/local/bin/lsof -iTCP -n -P`
        -   `discoUser ALL=(root) NOPASSWD:ADME_CMDS`
        -   `Defaults!ADME_CMDS !requiretty`

            **Note:** Netstat is not supported.

    -   Additional requirements: None
-   **Centos and Ubuntu**
    -   Utility tool support: None
    -   Required sudoer commands:
        -   `Cmnd_Alias ADME_CMDS = /usr/sbin/lsof -iTCP -n -P, /usr/bin/netstat -antp, /sbin/ss -tlnp, /sbin/ss -tenp`
        -   `discoUser ALL=(root) NOPASSWD:ADME_CMDS`
        -   `Defaults!ADME_CMDS !requiretty`
    -   Additional requirements: None

Note the following for the sudo commands:

-   `ADME_CMDS` is a variable referring to a list of commands.
-   `/usr/bin/` is the directory where your lsof and netstat resides.
-   `discoUser` is a user that must have root access.

## Setup and use enhanced ADM

To set up and use enhanced ADM, perform these steps:

1.  [Enable enhanced ADM with the glide.discovery.enable\_adme Discovery property](r_ApplicationDependencyMapping.md#).
2.  Determine the base directory where the TCP tracking file is placed on the host computers. If you want to change the location, [specify it in these Discovery properties](r_ApplicationDependencyMapping.md#):
    -   `glide.discovery.adme.base_dir_unix`
    -   `mid.powershell.target_base_dir`
3.  Do either of the following based on the operating systems of the host computers:
    -   Linux: [modify the sudoers file](r_ApplicationDependencyMapping.md#sudoers) to include the necessary commands.
    -   Windows: Set the `mid.windows.management_protocol` parameter on the MID Server to use WinRM or WMI. This parameter sets the protocol that your MID Server uses to communicate with remote Windows hosts.
4.  [Create a schedule and run Discovery](../task/t_CreateADiscoverySchedule.md#).
5.  [View the results in the TCP tables](r_DataCollDiscoTCPConnections.md).
6.  Optionally control both the size of the TCP tracking file and the payload using parameters on the enhanced ADM probes. See [TCP connection discovery](r_DataCollDiscoTCPConnections.md) for the names of the probes and parameters.

**Parent Topic:**[Advanced Discovery configuration](../concept/c_DiscoveryExtendedCapabilities.md)

## Configure ADM discovery parameters and properties

Using properties, you can enable or disable ADM discovery, and you can set the location of the TCP tracking file for enhanced ADM.

### Before you begin

Role required: discovery\_admin or admin

### About this task

You can also control both the size of the TCP tracking file and the payload using parameters on the enhanced ADM probes. See [TCP connection discovery](r_DataCollDiscoTCPConnections.md) for the names of the probes and parameters.

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Discovery** to set the system properties.

2.  Navigate to **Discovery Definition** &gt; **Probes** to set the probe parameters.

3.  Configure the following properties and probe parameters.

    See the knowledge article [KB0822767](https://support.servicenow.com/kb_view.do?sysparm_article=KB0822767) for more information.

<table id="table_pg3_bfx_q1b"><thead><tr><th>

Probe parameter

</th><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

 

</td><td>

glide.discovery.enable\_adme

</td><td>

ADME: Enable enhanced ADM probe. If "yes", the ADM Enhanced probe is triggered and only fall back to the ADM probe as needed.-   Type: true \| false
-   Default value: false


</td></tr><tr><td>

 

</td><td>

glide.discovery.application\_mapping

</td><td>

Enable the application mapping feature. When this property is set to true, all discoveries trigger the relevant ADM probe during the exploration phase if Discovery finds a server.

 **Important:** Disabling this property disables the creation of relationships between applications but doesn’t disable the ADM probes and sensors, nor does it prevent process classification.

 -   Type: true \| false
-   Default value: true


</td></tr><tr><td>

sampling\_interval

</td><td>

glide.discovery.adme.sampling\_interval

</td><td>

ADME - Sampling interval \(sec\): How often to sample process and connection data in seconds. Must be a minimum of 5 seconds.-   Type: integer
-   Default value: 120


</td></tr><tr><td>

base\_dir

</td><td>

glide.discovery.adme.base\_dir\_unix

</td><td>

ADME - Unix Base Dir: An existing directory on the target UNIX machines to be used as a workspace. Must be an absolute path to the directory. The [UNIX and Linux credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_SSHCredentialsForm.md) that you use to connect to the device must also be able to access this folder.-   Type: string
-   Default value: /tmp


</td></tr><tr><td>

powershell\_param\_base\_dir

</td><td>

mid.powershell.target\_base\_dir

</td><td>

Powershell - Target Base Dir: A network share on the target Windows machines to be used as a workspace. If you change the directory, it must also be a network shared folder.-   Type: string
-   Default value: admin$\\temp


</td></tr><tr><td>

aggregation\_interval \(Unix\)powershell\_param\_aggregation\_interval \(Windows\)

</td><td>

glide.discovery.adme.aggregation\_interval

</td><td>

ADME - Aggregation interval \(sec\): How often to aggregate instantaneous data into chunks in seconds. It must be a minimum of 60 seconds and it must be a multiple of ADME Sampling interval.-   Type: integer
-   Default value: 3600


</td></tr><tr><td>

rolling\_window\_size \(Unix\)powershell\_param\_rolling\_window\_size \(Windows\)

</td><td>

glide.discovery.adme.rolling\_window\_size

</td><td>

ADME - Rolling window size: How many recently aggregated chunks to keep. An aggregated chunk consists of ADME Aggregation interval divided by ADME Sampling interval samples. Only the newest chunks are kept.-   Type: integer
-   Default value: 24


</td></tr><tr><td>

max\_total\_samples \(Unix\)powershell\_param\_max\_total\_samples \(Windows\)

</td><td>

glide.discovery.adme.max\_total\_samples

</td><td>

ADME - Max total samples: The limit of samples being taken by the script. The script will stop running after this number of samples are taken.-   Type: integer
-   Default value: 100


</td></tr></tbody>
</table>4.  Click **Save**.


