---
title: Agent Client Collector File-Based Discovery properties
description: Configure File-Based Discovery behavior using system properties that control scanning paths, performance throttling, and file filtering options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/file-based-discovery-configuration-properties.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 3
keywords: [File-Based Discovery, configuration, properties, Agent Client Collector]
breadcrumb: [Agent Client Collector for Visibility - Content reference, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector File-Based Discovery properties

Configure File-Based Discovery behavior using system properties that control scanning paths, performance throttling, and file filtering options.

## Discovery settings properties

All File-Based Discovery configuration properties are configurable from the System Properties page \(**All** &gt; **System Properties** &gt; **All Properties**\).

|Property|Description|Platforms|
|--------|-----------|---------|
|**glide.discovery.file\_discovery.path.windows**|Directories to scan on Windows endpoints \(pipe-separated\). Supports environment variables \(%PROGRAMFILES%\) and wildcards.|Windows|
|**glide.discovery.file\_discovery.path.linux**|Directories to scan on Linux/macOS endpoints \(colon-separated\). Supports environment variables \($HOME\) and wildcards.|Linux, macOS|
|**glide.discovery.file\_discovery.ignore\_path.windows**|Directories to exclude from scanning on Windows \(pipe-separated\).|Windows|
|**glide.discovery.file\_discovery.ignore\_path.unix**|Directories to exclude from scanning on Linux/macOS \(colon-separated\).|Linux, macOS|
|**glide.discovery.file\_discovery.throttle\_size.windows**|Number of files to process before pausing \(Windows\).|Windows|
|**glide.discovery.file\_discovery.throttle\_size.unix**|Number of files to process before pausing \(Linux/macOS\).|Linux, macOS|
|**glide.discovery.file\_discovery.sleeptime.windows**|Pause duration in milliseconds after each throttle batch \(Windows\).|Windows|
|**glide.discovery.file\_discovery.sleeptime.unix**|Pause duration in milliseconds after each throttle batch \(Linux/macOS\).|Linux, macOS|
|**glide.discovery.file\_discovery.skip\_hidden\_folders.windows**|When enabled, skips hidden files and folders during scanning \(Windows\).|Windows|
|**glide.discovery.file\_discovery.skip\_hidden\_folders.unix**|When enabled, skips dot-prefixed \(hidden\) files and folders during scanning \(Linux/macOS\).|Linux, macOS|
|**glide.discovery.file\_discovery.scan\_swid.windows**|Enables or disables SWID tag scanning on Windows platforms. When enabled, the scanner looks for .swid, .swidtag, and .cmptag files in the configured scan directories.|Windows|
|**glide.discovery.file\_discovery.scan\_swid.unix**|Enables or disables SWID tag scanning on Linux and macOS platforms. When enabled, the scanner looks for .swid, .swidtag, and .cmptag files in the configured scan directories.|Linux, macOS|

<table id="table_ftm_n5j_hjc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File matching rules \(**sn\_acc\_vis\_content\_file\_config**\)

</td><td>

Defines the filename matching rules. Each rule specifies:-   File name: The pattern to match.
-   Condition: `exact_match`, `starts_with`, `ends_with`, or `contains`.
-   Extension: Reference to the **sn\_acc\_vis\_content\_file\_extension** property.

</td></tr><tr><td>

File extensions \(**sn\_acc\_vis\_content\_file\_extension**\)

</td><td>

Defines which file extensions to scan for File Management \(such as .exe, .dll, .msi, .pkg, and so forth\). Each record specifies an extension and the platform it applies to \(Windows, Mac, or All\).

</td></tr><tr><td>

Full Scan Mode \(**sn\_acc\_vis\_content.file\_disovery.enable\_fbd\_fullscan**\)

</td><td>

When false \(strict mode\), only files that match a rule in the File Config table are discovered. When true, all files with a matching extension are discovered only if no specific rule exists for them.

Default: false

</td></tr><tr><td>

Delta Scan Frequency \(**sn\_acc\_vis\_content.file\_discovery.fresh\_scan\_frequency\_by\_delta\_count**\)

</td><td>

The number of delta scans to perform before forcing a full scan. This ensures data accuracy over time.For details on delta scanning, see [Agent Client Collector File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/file-based-discovery-overview.md).

Default: 5

</td></tr><tr><td>

MME Types \(Linux only\) \(**sn\_acc\_vis\_content.file\_discovery.mime\_type.unix**\)

</td><td>

Colon-separated list of MIME types to scan on Linux \(such as `application/x-pie-executable:text/x-shellscript`\). On Linux, File Management uses MIME type detection instead of extension-based matching.

</td></tr><tr><td>

Running process-based discovery \(**sn\_acc\_vis\_content.file\_discovery.fbd\_process\_scan\_enabled**\)

</td><td>

Running process-based discovery enables the ACC-VC agent to detect software running outside of standard scan directories, including applications that a directory-only scan can't detect.

 Default: false

</td></tr><tr><td>

Archive file scanning \(**sn\_acc\_vis\_content.file\_discovery.archive\_scan\_enabled**\)

</td><td>

Archive file scanning extends file-based discovery to look inside ZIP and JAR archive files and report the files contained within them. This enables discovery of software artifacts that are distributed in compressed packages without requiring the archive to be extracted on the endpoint.

 Default: false

</td></tr></tbody>
</table>## Performance throttling

The throttling properties control how File-Based Discovery manages system resources during scanning operations. The throttle size determines how many files are processed in each batch, while the sleep time controls the pause duration between batches to prevent excessive system load.

## Path configuration

Path properties support environment variables and wildcards for flexible directory specification. Use pipe separators \(\|\) for Windows paths and colon separators \(:\) for Linux and macOS paths. The ignore path properties allow you to exclude specific directories from scanning to improve performance and avoid unnecessary data collection.

