---
title: Agent Client Collector File-Based Discovery
description: Agent Client Collector File-Based Discovery \(FBD\) scans file systems on managed endpoints to discover installed software and track file inventories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/file-based-discovery-overview.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-05-04"
reading_time_minutes: 3
keywords: [file-based discovery, FBD, agent client collector, software discovery, file inventory]
breadcrumb: [ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Agent Client Collector File-Based Discovery

Agent Client Collector File-Based Discovery \(FBD\) scans file systems on managed endpoints to discover installed software and track file inventories.

FBD runs as a lightweight background process within the existing Agent Client Collector agent. It is configured and controlled entirely from the ServiceNow instance. Administrators define which directories to scan, which files to look for, and how often to scan. The agent discovers matching files, collects metadata such as name, path, size, and version, and sends the results back to the instance where they are stored in the appropriate CMDB and application tables.

To activate FBD, navigate to the Discovery Configuration Console \(**All** &gt; **Discovery Definition** &gt; **Configuration Console**\) and in the **File Based Discovery** section, activate the **Enable File Based Discovery** toggle switch.

\[Omitted image "DiscoConfigConsole.png"\] Alt text: Discovery Configuration Console

For details on the FBD configuration and system properties, see [Agent Client Collector File-Based Discovery properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/file-based-discovery-configuration-properties.md).

## Supported platforms

FBD supports the following operating systems:

-   Windows
-   Linux
-   macOS

## Required plugins

The following plugins are required for File-Based Discovery on Agent Client Collector:

-   **File-based Discovery** \(com.snc.discovery.file\_based\_discovery\)
-   **Software Asset Management - File Signature Normalization** \(com.snc.file\_signature\_normalization\) — Activated automatically once the File-based Discovery plugin is active
-   **Agent Client Collector - Visibility Content** \(sn\_acc\_vis\_content\)
-   **Software Asset Management Professional** \(com.snc.samp\)

## Delta scanning

Delta scanning is a performance optimization that applies only to the File Management policy. It reduces the volume of data sent from the endpoint to the instance on repeat scans.

The delta scanning process works as follows:

1.  **First scan** — A full scan runs. All matching files are sent to the instance. A fingerprint, which is a snapshot of all discovered file paths and sizes, is saved locally on the endpoint.
2.  **Subsequent scans** — The scanner compares the current file list against the saved fingerprint and reports only the differences:
    -   **Added** — files that exist now but were not in the previous fingerprint
    -   **Modified** — files that exist in both but with a different size
    -   **Deleted** — files that were in the previous fingerprint but no longer exist on disk
3.  **Periodic full scan** — After a configured number of delta scans \(default: 5\), a full scan is automatically forced to verify accuracy and correct any drift.

**Note:** Delta scanning does not apply to the SAM or SWID policies. These policies always perform a full scan on each run.

## Archive file scanning

Archive file scanning extends file-based discovery to inspect ZIP and JAR archive files and report the files contained within them. This enables discovery of software artifacts such as executables and libraries that are packaged in the ZIP or JAR files on the endpoint.

Archive file scanning is disabled by default. To enable it, set the **sn\_acc\_vis\_content.file\_discovery.archive\_scan\_enabled** property to **true**. This property requires the **discovery\_admin** role to modify.

When archive file scanning is enabled, the agent inspects each ZIP or JAR file encountered during a directory scan. The agent reads the archive's internal index to enumerate the files inside. No file content is extracted or decompressed. Only metadata is collected.

For each file found inside an archive, the agent applies the same filtering rules used for regular files on disk, including SAM allowlist and File Management extension rules. Files that pass the filters are reported alongside other discovered files.

For filtering rules and performance safeguards, see [Archive file scanning filtering rules and limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/archive-file-scanning-reference.md).

