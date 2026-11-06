---
title: File-based Discovery
description: File-based Discovery helps you identify what software is running on your Windows and UNIX servers and devices, even if there's no registration information available. You can then manage and maintain records of your software licenses, check for unlicensed files, detect forbidden or damaged files, and help evaluate any threats from unwanted files.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/discovery/file-based-discovery.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-10-13"
reading_time_minutes: 7
breadcrumb: [Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# File-based Discovery

File-based Discovery helps you identify what software is running on your Windows and UNIX servers and devices, even if there's no registration information available. You can then manage and maintain records of your software licenses, check for unlicensed files, detect forbidden or damaged files, and help evaluate any threats from unwanted files.

## Required plugins

The File-based Discovery \[com.snc.discovery.file\_based\_discovery\] plugin is required for file signature filtering. Your Discovery subscription includes this plugin, but you must [request activation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_RequestAPlugin.md). Once the File-based Discovery plugin is active, the Software Asset Management - File Signature Normalization \[com.snc.file\_signature\_normalization\] plugin is also activated. For more information on the File Signature Normalization plugin, see [File Signature Normalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/sam-file-based-discovery.md).

## How File-based Discovery works

File-based Discovery enhances the pre-existing discovery of installed software. It scans target servers for a known list of file signatures and processes those files with an established set of rules. The resulting data enhances the identification of installed software and identifies unregistered software products. For information about using Agent Client Collector for Visibility Content to perform file-based discovery, see [Discover Java installation data using Agent Client Collector for Visibility Content File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-file-based-discovery.md).

File-based Discovery is triggered in the exploration phase of normal Discovery. File-based Discovery probes execute a scan searching for specific file extensions or file names in paths that you configure. The resulting file information is returned in the probe payload. The sensor attempts to match the discovered files with installed software, using the file name, size, and version returned by the probe. On Linux and UNIX devices, the Unix - File Discovery probe doesn't return version information. File-based Discovery uses file signatures to detect software that might not have been registered. This information is then stored in the File Information \[cmdb\_file\_information\] table with a reference to the CI of the server. You can view the files found from each CI in a related list on this table. For more information, see [Related list of CI components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/r_RelatedListsOfCIComponents.md). When [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SoftwareAssetMgmt.md) \(SAM\) is active, if any file matches a software product, Discovery populates the Product and Publisher information for that file. Use this information to understand what software is running on your server and to help evaluate any threats from unwanted files. Discovery uses lists of known file signatures for Windows and UNIX to constrain the scope of the search. The filtering process for Windows and UNIX hosts is executed differently because their signature lists differ greatly in size. The smaller UNIX signature list is included with the Unix - File Discovery probe and processed directly on the target. The Windows signature list is larger and can’t be processed on the target. The Windows - File Discovery probe scans the target for specific file extensions and paths and returns these results to the MID Server. The MID Server performs file signature filtering using the entire Windows list. The MID Server then sends all file information back to the instance for normalization and matching.

If SAMP is active on the instance, File-based Discovery creates or updates identified software products in the Software Installation \[cmdb\_sam\_sw\_install\] table and updates matched software package licenses. Without SAMP, no software records are created. Only the file information goes into the File Information \[cmdb\_file\_information\] table.

You can enable SWID tags in the [Discovery Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/c_DiscoveryConfigurationConsole.md). With SWID tag enabled, when running File-based Discovery, the SWID tag information then populates the Swid Tags \[cmdb\_swid\_tag\] table. Information about the software installed on a particular machine includes name, file information, publisher, version, installed on, and content. The software\_installation column in the Swid Tags \[cmdb\_swid\_tag\] table is a reference to the Software Installations \[cmdb\_sam\_sw\_install\] table.

**Note:** Base64 package is a prerequisite for any UNIX or Linux servers to scan SWID tag files using File-based Discovery.

File-based Discovery inserts any file not matched by the normalization process into the Unidentified File Set \[cmdb\_unidentified\_file\_set\] table. You can update the records in this table and provide additional details for previously unidentified files. If you provide values for the **Product** and **Publisher** fields for a file, SAMP settings can enable File-based Discovery to use that file for installed software matching in future discoveries.

You can disable File-based Discovery at any time by changing the setting in the [Discovery Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/c_DiscoveryConfigurationConsole.md). If you disable File-based Discovery before scan results are returned, the file data is ignored.

**Note:**

-   File-based Discovery supports Windows, UNIX, and macOS devices. The UNIX probe is POSIX-compliant and should run on any Linux/Solaris server. Discovery supports Windows versions 2008, 2008R2, 2012R2, 2016, 2019, and later with PowerShell 3.0–7. Discovery also supports AIX versions 5.3, 6.1, and 7.1 and HP/UX 8.11.
-   -   To use File-based Discovery on target hosts that run PowerShell 7, configure the MID Server to prefer PowerShell 7. For more information, see [Configure MID Server parameters for PowerShell 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/config-mid-params-ps7.md).
-   If you’re running File-based Discovery on Ubuntu version 20, modify the default Bourne shell \(sh\) to point to Bourne Again shell \(bash\).
-   Version information is populated only for the files with version information returned from probes. Not all files have versions. On Windows devices, files with extensions such as .exe, .jar, and so on, have versions. On Linux and UNIX devices, the probe doesn't return version information. For more information, see the following section.

## Software version information on Linux and UNIX devices

The Unix - File Discovery probe returns file name and file size only for Linux and UNIX devices. It is not designed to collect file version metadata. As a result, the **Version** field in the File Information \[cmdb\_file\_information\] table is empty for files discovered on Linux and UNIX devices. This is expected behavior, not a configuration issue. Linux software versions are collected through the rpm- and dpkg-based discovery probes instead, such as the Linux - Install Software probe.

To obtain version information for software on Linux and UNIX devices, enable SWID tag scanning for products that provide valid SWID tags. SWID tags include version data and populate the Swid Tags \[cmdb\_swid\_tag\] table. Enable SWID tag scanning selectively for products known to provide valid SWID tags rather than enabling it across all servers, to avoid unnecessary scanning overhead. For more information, see [Discovery Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/c_DiscoveryConfigurationConsole.md).

## Target system permissions

File-based Discovery connects to each target system with the configured discovery credential and reads files directly as that credential's account. On both UNIX and Windows target systems, the credential's own file system permissions determine what File-based Discovery can access. File-based Discovery skips any directories and files that the account can't read and doesn't report an error for them.

On Windows systems, File-based Discovery reads files with the NTFS permissions of the discovery credential's account through WinRM/WMI. The scan writes its working files to the admin$ administrative share, which defaults to `C:\Windows\Temp\<mid-instance-name>`.

-   **Required permissions \(UNIX\)**

    The Discovery user needs the following permissions on each UNIX target system:

    |Permissions required|Description|
    |--------------------|-----------|
    |Read and execute \(traverse\) on the directories in the scan path|Enables the scan to move through the directory trees you select. Directories that the credential's account can't traverse are skipped, with no error reported.|
    |Read on the files that match the scan list|Enables File-based Discovery to read each file's size and details. Files that the account can't read are skipped, with no error reported.|
    |Read and write on the temporary directory, /tmp by default|Enables the scan to write and read its working files on the target system.|
    |Read on SWID files, when SWID tag scanning is enabled|Enables File-based Discovery to read software identification details from SWID files.|

    **Note:** File-based Discovery scans the `/opt` and `/etc` directories on a Linux system. If the discovery credential's account doesn't have read and execute permissions on these directories, File-based Discovery skips them without reporting an error. It reports only the software in directories that the account can read.

-   **Required operating system tools**

    File-based Discovery uses standard operating system tools on each target system. The following tools must be available in the system path on each target:

    -   find, wc, awk, and grep
    -   ps and nohup
    -   sh or bash
    -   sed, cat, mv, rm, chmod, tr, and head
    When SWID tag scanning is enabled, base64 or uuencode must also be available. File-based Discovery uses uuencode first and falls back to base64.


**Related topics**  


[Run File-based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/run-file-based-discovery.md)

[File-based Discovery references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/file-based-discovery-references.md)

[File-based Discovery issue resolution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/discovery/file-based-discovery-troubleshooting.md)

