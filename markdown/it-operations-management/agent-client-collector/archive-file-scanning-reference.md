---
title: Archive file scanning filtering rules and limits
description: Reference information for the filtering rules and performance safeguards that apply when Agent Client Collector for Visibility - Content scans ZIP and JAR archive files during File-Based Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/archive-file-scanning-reference.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-06-09"
reading_time_minutes: 1
keywords: [archive file scanning, File-Based Discovery, ZIP, JAR, agent client collector, ACC-VC]
breadcrumb: [Agent Client Collector for Visibility - Content reference, Agent Client Collector, IT Operations Management]
---

# Archive file scanning filtering rules and limits

Reference information for the filtering rules and performance safeguards that apply when Agent Client Collector for Visibility - Content scans ZIP and JAR archive files during File-Based Discovery.

## Filtering rules

Archive entries are filtered using the same rules as files found on disk, with the following differences.

|Capability|Regular files|Archive entries|
|----------|-------------|---------------|
|SAM allowlist matching|Yes|Yes|
|File Management extension rules|Yes|Yes|
|MIME type detection \(Linux\)|Yes|No. The file does not exist on disk, so the system can't inspect its content type|
|Version detection|Yes|No. Version can't be queried for a file that hasn't been extracted|
|SWID tag support|Yes|No. Archive contents aren't decompressed or read, so SWID tags inside ZIP or JAR files aren't processed|

**Note:** On Linux, File Management matching relies on MIME type detection rather than extension rules. As a result, archive entries can only be matched by SAM rules, not by MIME type.

## Performance safeguards

The following limits are enforced to prevent archive scanning from affecting agent performance or endpoint stability.

|Safeguard|Limit|Behavior when exceeded|
|---------|-----|----------------------|
|Maximum archive file size|500 MB|Archive is skipped entirely|
|Maximum entries per archive|50,000 files|Scanning stops after the limit; entries discovered so far are retained|
|Per-archive timeout|30 seconds|Scanning of that archive is aborted; entries discovered so far are retained|
|Corrupt or password-protected archives|Not applicable|Detected automatically, logged, and skipped|
|Nested archives \(archive inside an archive\)|Not applicable|Not scanned. Only top-level archives on disk are inspected|
|Global file limit \(**maxFiles**\)|Configured per policy|Archive entries count toward the global file limit; scanning stops when the limit is reached|

