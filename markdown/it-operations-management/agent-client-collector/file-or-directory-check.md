---
title: File or directory check
description: OS-level permission requirements for the file or directory check.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/agent-client-collector/file-or-directory-check.html
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector checks – credential and permission requirements, Agent Client Collector Monitoring reference, Agent Client Collector, IT Operations Management]
---

# File or directory check

OS-level permission requirements for the file or directory check.

## Agent Client Collector Agent OS account

The Agent Client Collector agent OS account is only required if the target file or directory is owned by another service account. The Agent Client Collector agent OS account needs the following permissions:

-   Read permission, and for directories, execute or traverse permission, on the target `--directory`, `--dirpath`, or `--filepath`.
-   For `check-file-response-time`, read access to the contents of the file, not just metadata, because it measures read latency.

A file or directory owned by another application, such as its own log or data directory, is frequently not world-readable. In that case, the Agent Client Collector agent account needs group membership or an ACL grant to read it.

Configuration Prerequisites:

-   Confirm the target path exists and is spelled or cased correctly. Paths are case-sensitive on Linux.
-   Confirm read and execute permission on the full path, including every parent directory, not just the final file or directory. A missing execute bit on a parent directory blocks traversal even if the file itself is readable.

Troubleshooting:

-   A file not found result for a file that exists means a missing execute bit on a parent directory rather than a problem with the file itself.
-   For files owned by another service account, add the Agent Client Collector agent OS account to the owning group, or grant an ACL, rather than loosening the file's world permissions.

**Parent Topic:**[Agent Client Collector checks – credential and permission requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-monitoring-checks-credential-and-permission-requirements.md)

