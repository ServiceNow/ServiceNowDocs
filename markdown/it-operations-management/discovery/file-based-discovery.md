---
title: File-based Discovery
description: File-based Discovery helps you identify what software is running on your Windows and UNIX servers and devices, even if there's no registration information available. You can then manage and maintain records of your software licenses, check for unlicensed files, detect forbidden or damaged files, and help evaluate any threats from unwanted files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/file-based-discovery.html
release: brazil
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# File-based Discovery

File-based Discovery helps you identify what software is running on your Windows and UNIX servers and devices, even if there's no registration information available. You can then manage and maintain records of your software licenses, check for unlicensed files, detect forbidden or damaged files, and help evaluate any threats from unwanted files.

## Required plugins

The File-based Discovery \[com.snc.discovery.file\_based\_discovery\] plugin is required for file signature filtering. Your Discovery subscription includes this plugin, but you must [request activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_RequestAPlugin.md). Once the File-based Discovery plugin is active, the Software Asset Management - File Signature Normalization \[com.snc.file\_signature\_normalization\] plugin is also activated. For more information on the File Signature Normalization plugin, see [File Signature Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-file-based-discovery.md).

## How File-based Discovery works

File-based Discovery enhances the pre-existing discovery of installed software. It scans target servers for a known list of file signatures and processes those files with an established set of rules. The resulting data enhances the identification of installed software and identifies unregistered software products. For information about using Agent Client Collector for Visibility Content to perform file-based discovery, see [Discover java installation data using Agent Client Collector for Visibility Content file-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/acc-file-based-discovery.md).

File-based Discovery is triggered in the exploration phase of normal Discovery. File-based Discovery probes execute a scan searching for specific file extensions or file names in paths that you configure. The resulting file information is returned in the probe payload. The sensor attempts to match the discovered files with installed software, using the file name, size, and version returned by the probe. File-based Discovery uses file signatures to detect software that might not have been registered. This information is then stored in the File Information \[cmdb\_file\_information\] table with a reference to the CI of the server. You can view the files found from each CI in a related list on this table. For more information, see [Related list of CI components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_RelatedListsOfCIComponents.md). When [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_SoftwareAssetMgmt.md) \(SAM\) is active, if any file matches a software product, Discovery populates the Product and Publisher information for that file. Use this information to understand what software is running on your server and to help evaluate any threats from unwanted files. Discovery uses lists of known file signatures for Windows and UNIX to constrain the scope of the search. The filtering process for Windows and UNIX hosts is executed differently because their signature lists differ greatly in size. The smaller UNIX signature list is included with the Unix - File Discovery probe and processed directly on the target. The Windows signature list is larger and can’t be processed on the target. The Windows - File Discovery probe scans the target for specific file extensions and paths and returns these results to the MID Server. The MID Server performs file signature filtering using the entire Windows list. The MID Server then sends all file information back to the instance for normalization and matching.

If SAMP is active on the instance, File-based Discovery creates or updates identified software products in the Software Installation \[cmdb\_sam\_sw\_install\] table and updates matched software package licenses. Without SAMP, no software records are created. Only the file information goes into the File Information \[cmdb\_file\_information\] table.

You can enable SWID tags in the Discovery Configuration Console. With SWID tag enabled, when running File-based Discovery, the SWID tag information then populates the \[cmdb\_swid\_tag\] table. Information about the software installed on a particular machine includes name, file information, publisher, version, installed on, and content. The software\_installation column in the \[cmdb\_swid\_tag\] is a reference to the \[cmdb\_sam\_sw\_install\] table.

**Note:** Base64 package is a prerequisite for any UNIX or Linux servers to scan SWID tag files using File-based Discovery.

File-based Discovery inserts any file not matched by the normalization process into the Unidentified File Set \[cmdb\_unidentified\_file\_set\] table. You can update the records in this table and provide additional details for previously unidentified files. If you provide values for the **Product** and **Publisher** fields for a file, SAMP settings can enable File-based Discovery to use that file for installed software matching in future discoveries.

You can disable File-based Discovery at any time by changing the setting in the [Discovery Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/c_DiscoveryConfigurationConsole.md). If you disable File-based Discovery before scan results are returned, the file data is ignored.

**Note:**

File-based Discovery supports Windows, UNIX, and macOS devices. The UNIX probe is POSIX-compliant and should run on any Linux/Solaris server. Discovery supports Windows versions 2008, 2008R2, 2012R2, 2016, 2019, and later with PowerShell 3.0–7. Discovery also supports AIX versions 5.3, 6.1, and 7.1 and HP/UX 8.11.

To use File-based Discovery on target hosts that run PowerShell 7, configure the MID Server to prefer PowerShell 7. For more information, see [Configure MID Server parameters for PowerShell 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/config-mid-params-ps7.md).

If you’re running File-based Discovery on Ubuntu version 20, modify the default Bourne shell \(sh\) to point to Bourne Again shell \(bash\).

Version information is populated only for the files with version information returned from probes. Not all files have versions. Files with extensions such as .exe, .jar, and so on, have versions.

## Target system permissions

File-based Discovery needs specific permissions on each UNIX target system to scan files and read software details. The following sections list the required permissions and the sudoers configuration for the discovery user.

The MID Server runs the discovery script on each UNIX system with sudo. When the discovery user has sudo access, File-based Discovery scans every directory in the scan path.

When the Discovery user doesn't have sudo access, File-based Discovery scans only the directories that all users can read. It skips protected directories and doesn't report an error for them.

On Windows systems, File-based Discovery uses the administrative discovery credential and runs a signed script. Windows systems don't use sudoers.

-   **Require permissions**

    The Discovery user needs the following permissions on each UNIX target system:

    |Permission|Description|
    |----------|-----------|
    |Run the discovery script with sudo|Enables file-based Discovery to scan directories that aren't readable by all users.|
    |Read and run on the directories in the scan path|Enables the scan to move through the directory trees you select.|
    |Read on the files that match the scan list|Enables File-based Discovery to read each file's size and details.|
    |Read on the temporary directory, /tmp by default|Enables the scan to write and read its working files on the target system.|
    |Read on SWID files, when SWID tag scanning is enabled|Enables File-based Discovery to read software identification details from SWID files.|

-   **Required operating system tools**

    File-based Discovery uses standard operating system tools on each target system. The following tools must be available in the system path:

    -   find, wc, awk, and grep
    -   ps and nohup
    -   sh or bash
    When SWID tag scanning is enabled, base64 or uuencode must also be available. File-based Discovery uses uuencode first and falls back to base64.

-   **Sudoers configuration**

    Add entries to the sudoers file on each UNIX target system. These entries give the discovery user the sudo access that File-based Discovery needs. Replace discoUser with your discovery credential user and adjust the tool paths to match your installation.

    Linux, CentOS, Ubuntu, and RHel use the following entries for Linux systems:

    ```
    Cmnd_Alias FBD_SCRIPT = /bin/sh /tmp/SNC_File_Discovery_Script_*.sh
    Cmnd_Alias FBD_CMDS = /usr/bin/find *, /usr/bin/wc *, /bin/cat *
    discoUser ALL=(root) NOPASSWD:FBD_SCRIPT, FBD_CMDS
    Defaults!FBD_SCRIPT !requiretty
    Defaults!FBD_CMDS !requiretty
    
    ```

    To enable SWID tag scanning on Linux, add the following entry:

    ```
    Cmnd_Alias FBD_SWID = /usr/bin/base64 *, /usr/bin/uuencode *
    discoUser ALL=(root) NOPASSWD:FBD_SWID
    Defaults!FBD_SWID !requiretty
    
    ```

    Use the same script and command entries on AIX, Solaris, and HP-UX systems. For SWID tag scanning on these systems, use uuencode:

    ```
    Cmnd_Alias FBD_SWID = /usr/bin/uuencode *
    discoUser ALL=(root) NOPASSWD:FBD_SWID
    Defaults!FBD_SWID !requiretty
    
    ```

    On AIX, use this requiretty syntax instead of the Linux form:

    ```
    Defaults:discoUser ! requiretty
    ```


## Example

A Discovery user scans the /opt and /etc directories on a Linux system. These directories aren't readable by all users.

With the sudoers entries in place, the discovery user runs the scan with sudo. File-based Discovery reads the files in both directories and reports the software it finds.

Without the sudoers entries, File-based Discovery skips /opt and /etc. It reports only the software in directories that all users can read.

**Related topics**  


[Run File-based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/run-file-based-discovery.md)

[File-based Discovery references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/file-based-discovery-references.md)

[File-based Discovery issue resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/discovery/file-based-discovery-troubleshooting.md)

