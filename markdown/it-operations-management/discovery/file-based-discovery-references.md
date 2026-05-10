---
title: File-based Discovery references
description: Review this reference material for further details on File-based Discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-24"
reading_time_minutes: 4
breadcrumb: [File-based Discovery, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# File-based Discovery references

Review this reference material for further details on File-based Discovery.

## How File-based Discovery minimizes performance impact

Scanning large networks, particularly for Windows computers, can extend scan time considerably. Moreover, file scanning can create heavy CPU demands on target machines and produce large payloads that greatly increase processing time. To avoid performance issues, File-based Discovery allows you to optimize processing with many of the settings configured using the [Discovery Configuration Console](../concept/c_DiscoveryConfigurationConsole.md#).

-   **Multi-phase scan**: Probes are triggered in multiple phases to reduce long scan times. The first probe creates the scanning process on the target, which runs in the background. Subsequent probes check the progress of this scan each time Discovery runs and return the results when the scan is complete. For example, if a file scan is initiated via Quick Discovery or from a Discovery schedule, no information is returned if a background scan is still running. If the scan is finished the next time the server is discovered, the probe returns the data.

    **Important:** The multi-phase scan that File-based Discovery uses does not return results immediately. Do not expect any results from a file-based scan until Discovery runs again on those targets and fetches the list of files discovered by the previous scan.

-   **Scan folders**: You can limit the scope of the scan to particular folders as well as scan hidden folders.
-   **Scan extensions**: You can retrieve all files for a given list of extensions as well as ignore specific file extensions when scanning.
-   **Scan UNIX file names**: Because the number of unique file names used to identify installed software on UNIX is relatively small, the complete list of file names is included in the UNIX probe. This enables the probe to filter the files it discovers against the signature list on the target. No additional filtering is required until the results are returned to the instance.
-   **Scan Windows file names**: For Windows File-based Discovery, the probe does not initiate a scan on target for full signature list. Instead, Discovery generates a list of file extensions that the probe attempts to match on the target. This reduced list is then filtered on the MID Server against the entire Windows signature list.
-   **Reduced payloads**: By filtering the scan results with the file signature list before the results get to the instance, Discovery reduces the size of the payload from target servers. Only those files from the targets that match the files specified in this list are returned to the instance.
-   **Scan throttling**: To reduce the impact on Windows CPU and I/O performance on remote targets, Windows File-based Discovery is configured to sleep occasionally during scans. You can fine-tune this behavior with Discovery properties. Throttling Windows scans can make those scans take longer.

## File-based Discovery tables

Descriptions of the tables provided by the File-based Discovery \[com.snc.discovery.file\_based\_discovery\] plugin for storing data:

-   **File Information \[cmdb\_file\_information\]**

    This table stores all the files, matched or unmatched, that were discovered on a particular CI. The files are available in a related list on CI computer records. The following columns are provided in the default view:

    -   **Path**: Path in which the file was found on the target.
    -   **Product**: Software product name. This field is populated when SAMP is activated and a match exists.
    -   **Publisher**: Name of the publisher of the file, such as Oracle or Microsoft. This is a reference to the Company \[core\_company\] table. This field is populated when SAMP is activated and a match exists.
    -   **Size**: Size of the file.
    -   **Software installation**: Name of the installed software associated with this file, from the Software Installation \[cmdb\_sam\_sw\_install\] table. This field is populated when SAMP is activated and a match exists.
    -   **Version**: Version of the file. Currently, for Windows only.
-   **Unidentified File Set \[cmdb\_unidentified\_file\_set\]**

    This table stores all the files returned by Discovery that cannot be matched to a software product, with or without SAMP. Discovery populates the name, size, and version of each unmatched file in the record. These optional fields can be used to further identify the file and make it available for future file matching:

    -   Publisher
    -   Product
    -   Version
    -   Edition
    -   Platform
    -   Language

**Note:** A feature in Software Asset Management Professional \(SAMP\) allows signature data in this table to be shared with Content Data Services \(CDS\). When you enable data sharing, the system automatically uploads records from the Unidentified File Set \[cmdb\_unidentified\_file\_set\] table to CDS when you provide the missing information. Uploading the identified files makes them available to improve future file matching. For details, see [Add a custom software product](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/t_AddACustomProduct.md).

For a full reference of File-based Discovery system properties and script includes, see the [File Based Discovery](https://support.servicenow.com/now/nav/ui/classic/params/target/kb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0813350) Now Support Knowledge Base article.

## File-based Discovery issue resolution

If you're experiencing any issues when setting up or running File-based Discovery, see [File-based Discovery issue resolution](file-based-discovery-troubleshooting.md).

**Related topics**  


[File-based Discovery](../concept/file-based-discovery.md)

