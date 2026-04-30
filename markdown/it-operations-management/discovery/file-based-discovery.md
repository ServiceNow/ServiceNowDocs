---
title: File-based Discovery
description: File-based Discovery helps you identify what software is running on your Windows and UNIX servers and devices, even if there’s no registration information available. You can then manage and maintain records of your software licenses, check for unlicensed files, detect forbidden or damaged files, and help evaluate any threats from unwanted files.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 4
breadcrumb: [Running discoveries in your network, Discovery, ITOM Visibility, IT Operations Management]
---

# File-based Discovery

File-based Discovery helps you identify what software is running on your Windows and UNIX servers and devices, even if there’s no registration information available. You can then manage and maintain records of your software licenses, check for unlicensed files, detect forbidden or damaged files, and help evaluate any threats from unwanted files.

## Required plugins

The File-based Discovery \[com.snc.discovery.file\_based\_discovery\] plugin is required for file signature filtering. Your Discovery subscription includes this plugin, but you must [request activation](https://www.servicenow.com/docs/access?context=t_RequestAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US). Once the File-based Discovery plugin is active, the Software Asset Management - File Signature Normalization \[com.snc.file\_signature\_normalization\] plugin is also activated. For more information on the File Signature Normalization plugin, see [File Signature Normalization](https://www.servicenow.com/docs/access?context=sam-file-based-discovery&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US).

## How File-based Discovery works

File-based Discovery enhances the pre-existing discovery of installed software. It scans target servers for a known list of file signatures and processes those files with an established set of rules. The resulting data enhances the identification of installed software and identifies unregistered software products.

File-based Discovery is triggered in the exploration phase of normal Discovery. File-based Discovery probes execute a scan searching for specific file extensions or file names in paths that you configure. The resulting file information is returned in the probe payload. The sensor attempts to match the discovered files with installed software, using the file name, size, and version returned by the probe. File-based Discovery uses file signatures to detect software that might not have been registered. This information is then stored in the File Information \[cmdb\_file\_information\] table with a reference to the CI of the server. You can view the files found from each CI in a related list on this table. For more information, see [Related list of CI components](https://www.servicenow.com/docs/access?context=r_RelatedListsOfCIComponents&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). When [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) \(SAM\) is active, if any file matches a software product, Discovery populates the Product and Publisher information for that file. Use this information to understand what software is running on your server and to help evaluate any threats from unwanted files. Discovery uses lists of known file signatures for Windows and UNIX to constrain the scope of the search. The filtering process for Windows and UNIX hosts is executed differently because their signature lists differ greatly in size. The smaller UNIX signature list is included with the Unix - File Discovery probe and processed directly on the target. The Windows signature list is larger and can’t be processed on the target. The Windows - File Discovery probe scans the target for specific file extensions and paths and returns these results to the MID Server. The MID Server performs file signature filtering using the entire Windows list. The MID Server then sends all file information back to the instance for normalization and matching.

If SAMP is active on the instance, File-based Discovery creates or updates identified software products in the Software Installation \[cmdb\_sam\_sw\_install\] table and updates the licenses of matched software packages. Without SAMP, no software records are created and only the file information goes into the File Information \[cmdb\_file\_information\] table.

You can enable SWID tags in the Discovery Configuration Console. With SWID tag enabled, when running File-based Discovery, the SWID tag information then populates the \[cmdb\_swid\_tag\] table. Information about the software installed on a particular machine includes name, file information, publisher, version, installed on, and content. The software\_installation column in the \[cmdb\_swid\_tag\] is a reference to the \[cmdb\_sam\_sw\_install\] table.

**Note:** Base64 package is a prerequisite for any UNIX or Linux servers to scan SWID tag files using File-based Discovery.

![File-based Discovery filtering flow](../image/FileBasedDiscoveryFlowDiagram.png "File-based Discovery filtering flow")

File-based Discovery inserts any file not matched by the normalization process into the Unidentified File Set \[cmdb\_unidentified\_file\_set\] table. You can update the records in this table and provide additional details for previously unidentified files. If you provide values for the **Product** and **Publisher** fields for a file, settings in SAMP can enable File-based Discovery to use that file for installed software matching in future discoveries.

**Note:** You can disable File-based Discovery at any time by changing the setting in the [Discovery Configuration Console](c_DiscoveryConfigurationConsole.md#). If you disable File-based Discovery before scan results are returned, the file data is ignored.

![File-based Discovery table schema](../image/FBDFileMatchingFlowDiagram.png "File-based Discovery table schema")

**Note:**

File-based Discovery supports Windows and UNIX devices. The UNIX probe is POSIX-compliant and should run on any Linux/Solaris server. Discovery supports Windows versions 2008, 2008R2, 2012R2, 2016, 2019, and above with PowerShell 3.0-5.1. Discovery also supports AIX versions 5.3, 6.1, and 7.1 and HP/UX 8.11.

If you're running File-based Discovery on Ubuntu version 20, modify the default Bourne shell \(sh\) to point to Bourne Again shell \(bash\).

Version information is populated only for the files with version information returned from probes. Not all files have versions. Files with extensions such as .exe, .jar, and so on, have versions.

**Related topics**  


[Run File-based Discovery](../task/run-file-based-discovery.md#)

[File-based Discovery references](../reference/file-based-discovery-references.md)

[File-based Discovery issue resolution](../reference/file-based-discovery-troubleshooting.md)

