---
title: Application Dependency Mapping \(ADM\) for Discovery
description: Application Dependency Mapping \(ADM\) discovers CIs by detecting TCP connections between devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/r\_ApplicationDependencyMapping.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
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


Service Mapping uses the ADM probes for traffic-based discovery. See [Discovery based on Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/service-mapping/predictive-intelligence-discovery.md) for more information.

## TCP tracking file for enhanced ADM

The first time that Discovery launches the enhanced probe, no TCP information is gathered. Rather, the enhanced probe only deploys the TCP tracking file, in which information about detected TCP connections is saved. After Discovery runs again, the enhanced probe relays the contents of the TCP tracking file back to the instance via the MID Server. The information is saved in the CMDB.

The TCP tracking file is saved in these locations by default:

-   Windows: `admin$\temp\{your_instance_name}`. While TCP connections are being monitored, the information is stored in memory and then later saved to the file.
-   Linux: `/tmp/{your_instance_name}`.

You can change the location and other aspects of the tracking file with ADM properties.

If you disable enhanced ADM, Discovery cleans up the folders from the host file system the next time Discovery runs, but the TCP tracking file remains.

## Supported operating systems

Both standard and enhanced ADM discovery support the following operating systems:

-   Windows Server 2012 R2 and later
-   CentOS and Ubuntu
-   Solaris \(On Solaris machines, enhanced ADM is available in global zones. Only standard ADM is available for local zones.\)
-   AIX
-   HP-UX

## Requirements for enhanced ADM

Before you enable enhanced ADM, make sure that each target host meets the requirements for its operating system.

|Operating system|Network tools|Sudoer entries required|Additional requirements|
|----------------|-------------|-----------------------|-----------------------|
|AIX|`netstat` with `rmsock`. `lsof` is used if netstat doesn't work.|Yes: `ADME_CMDS`|rmsock must be in the system PATH. AIX netstat doesn't output process IDs, so rmsock resolves the socket addresses in `netstat -Aan` output to process IDs. rmsock is part of the base AIX installation.|
|CentOS and Ubuntu|`netstat`. `lsof` is used if netstat isn't available, and `ss` is used if neither is available.|Yes: `ADME_CMDS`|At least one of lsof, netstat, or ss must be in the system PATH. If none of these tools is found, ADME logs an error and fails.|
|HP-UX|`lsof` only. netstat isn't supported.|Yes: `ADME_CMDS`|lsof must be installed and in the system PATH, and its path must match the sudoer entry. Without lsof, ADME can't collect network connection data.|
|Solaris 11.2 and later|`netstat`|Yes: `ADME_CMDS`, `ADME_PS`, pfiles, and pgrep|Add the lsof installation path to `secure_path` in the sudoers file.|
|Solaris versions earlier than 11.2|`lsof`|Yes: `ADME_CMDS`, `ADME_PS`, pfiles, and pgrep|lsof must be installed, its path must match the sudoer entry, and the path must be in `secure_path` in the sudoers file.|
|Windows|`netstat`, which is built in|No. Administrative credentials are passed through the Discovery credential record.|[PowerShell 3.0 or later](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/r_PowerShellForDiscovery.md) on the target host.|

|Permission|Applies to|Notes|
|----------|----------|-----|
|Local administrator on the target host|Windows|Required to enumerate all processes and connections.|
|Network access to the target host|Windows|WMI uses TCP port 135 and dynamic ports. WinRM uses TCP port 5985 or 5986.|
|PowerShell ExecutionPolicy Bypass|Windows|Set inline for each invocation. No persistent policy change is made.|
|Write access to `admin$\temp`|Windows|Default staging location for scripts and results.|
|Passwordless sudo access for the discovery user to the commands in the sudoer entries|AIX, CentOS and Ubuntu, HP-UX, Solaris|Required to run the network and process commands as root. On Solaris, both the `ADME_CMDS` and `ADME_PS` entries are required.|
|Root access for the discovery user to pfiles and pgrep|Solaris|Applies to both standard ADM and enhanced ADM.|
|SSH access to the target host|AIX, CentOS and Ubuntu, HP-UX, Solaris|The MID Server connects to the target host through SSH.|
|Write access to `/tmp`|AIX, CentOS and Ubuntu, HP-UX, Solaris|Default staging directory. You can change it with the `glide.discovery.adme.base_dir_unix` property. For more information, see [Configure ADM discovery parameters and properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/configuring-adm-disco.md).|

**Note:** If you set your Windows server Execution Policy to RemoteSigned or AllSigned, ADME can run PowerShell scripts. You must import the ServiceNow certificate to the trusted publisher in order for the scripts to execute properly.

## Configure the sudoers file for enhanced ADM

On UNIX and Linux hosts, the Discovery user must have passwordless sudo access to the commands in the sudoer entries for its operating system. The MID Server uses this user to run the commands as root and collect TCP connection data. Windows hosts don't use the sudoers file. Administrative credentials are passed directly through the Discovery credential record.

Each sudoer entry follows the same pattern:

-   The `Cmnd_Alias ADME_CMDS` line defines `ADME_CMDS` as the list of commands that enhanced ADM runs. On Solaris, the `Cmnd_Alias ADME_PS` line defines a second list for the process command.
-   The `discoUser ALL=(root) NOPASSWD:ADME_CMDS` line lets the Discovery user run the listed commands as root without a password. `discoUser` is the user in your Discovery credential.
-   The `Defaults` line disables `requiretty` so that the commands can run over an SSH session without a terminal.

The command paths in the entries are the default installation directories for each tool. If a tool is installed in a different directory on your hosts, adjust the path in the sudoer entry.

-   **AIX**

    Add these entries to the sudoers file on each AIX host:

    ```
    Cmnd_Alias ADME_CMDS = /usr/bin/netstat -Aan, \
                           /usr/sbin/lsof -iTCP -n -P
    discoUser ALL=(root) NOPASSWD:ADME_CMDS
    Defaults:discoUser ! requiretty
    ```

-   **CentOS and Ubuntu**

    Add these entries to the sudoers file on each CentOS or Ubuntu host:

    ```
    Cmnd_Alias ADME_CMDS = /usr/sbin/lsof -iTCP -n -P, \
                           /usr/bin/netstat -antp, \
                           /sbin/ss -tlnp, \
                           /sbin/ss -tenp
    discoUser ALL=(root) NOPASSWD:ADME_CMDS
    Defaults!ADME_CMDS !requiretty
    ```

-   **HP-UX**

    Add these entries to the sudoers file on each HP-UX host:

    ```
    Cmnd_Alias ADME_CMDS = /usr/local/bin/lsof -iTCP -n -P
    discoUser ALL=(root) NOPASSWD:ADME_CMDS
    Defaults!ADME_CMDS !requiretty
    ```

-   **Solaris**

    Add these entries to the sudoers file on each Solaris host:

    ```
    # ADME network commands:
    Cmnd_Alias ADME_CMDS = /usr/bin/netstat, \
                           /opt/csw/bin/lsof -iTCP -n -P -zglobal
    discoUser ALL=(root) NOPASSWD:ADME_CMDS
    Defaults!ADME_CMDS !requiretty
    
    # Standard ADM + ADME process commands:
    Cmnd_Alias ADME_PS = /usr/ucb/ps
    discoUser ALL=(root) NOPASSWD:ADME_PS
    Defaults!ADME_PS !requiretty
    
    Disco ALL=(root) /usr/bin/pfiles
    Disco ALL=(root) /usr/bin/pgrep
    ```

    Add the lsof installation path to `secure_path` in the sudoers file. For example, if lsof is in `/opt/csw/bin`, use `secure_path = /usr/bin:/usr/sbin:/bin:/sbin:/opt/csw/bin`.

    **Note:**

    -   In global zones, you must add `-zglobal` to the lsof entry.
    -   The `ADME_PS`, pfiles, and pgrep entries apply to standard ADM as well as enhanced ADM.
    -   Enhanced ADM detects the lsof path by using `command -v lsof` or `which lsof`. Make sure that the path in the sudoer entry matches the detected path.

**Note:** If the sudoer configuration is incorrect or requiretty is not disabled, ADME logs the following error in the `stderr.log` file: `Possible error in sudoer configuration or requiretty is not configured`.

## Set up and use enhanced ADM

To set up and use enhanced ADM, perform these steps:

1.  [Enable enhanced ADM with the glide.discovery.enable\_adme Discovery property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/configuring-adm-disco.md).
2.  Determine the base directory where the TCP tracking file is placed on the host computers. If you want to change the location, [specify it in these Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/configuring-adm-disco.md):
    -   `glide.discovery.adme.base_dir_unix`
    -   `mid.powershell.target_base_dir`
3.  Do either of the following based on the operating systems of the host computers:
    -   UNIX and Linux: [modify the sudoers file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/r_ApplicationDependencyMapping.md) to include the necessary commands.
    -   Windows: Set the `mid.windows.management_protocol` parameter on the MID Server to use WinRM or WMI. This parameter sets the protocol that your MID Server uses to communicate with remote Windows hosts.
4.  [Create a schedule and run Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/t_CreateADiscoverySchedule.md).
5.  [View the results in the TCP tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DataCollDiscoTCPConnections.md).
6.  Optionally control both the size of the TCP tracking file and the payload using parameters on the enhanced ADM probes. See [TCP connection discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DataCollDiscoTCPConnections.md) for the names of the probes and parameters.

-   **[Configure ADM discovery parameters and properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/configuring-adm-disco.md)**  
Using properties, you can enable or disable ADM discovery, and you can set the location of the TCP tracking file for enhanced ADM.

**Parent Topic:**[Advanced Discovery configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/c_DiscoveryExtendedCapabilities.md)

