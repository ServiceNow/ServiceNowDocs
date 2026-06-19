---
title: Running process-based discovery
description: Running process-based discovery extends File-Based Discovery \(FBD\) with process-based path detection, enabling the Agent Client Collector for Visibility - Content agent to detect software running outside of standard configured scan directories.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/running-process-based-discovery.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 1
keywords: [running process-based discovery, file-based discovery, FBD, process scan, agent client collector, software discovery]
breadcrumb: [Agent Client Collector File-Based Discovery, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Running process-based discovery

Running process-based discovery extends File-Based Discovery \(FBD\) with process-based path detection, enabling the Agent Client Collector for Visibility - Content agent to detect software running outside of standard configured scan directories.

## Why use running process-based discovery

Some software is never installed into the standard program directories that FBD scans. Common examples include:

-   Portable applications run from a removable drive or a user folder
-   User-installed tools placed in a personal directory, such as a Python interpreter under a user profile
-   Command-line utilities installed into a user's local binary directory

A directory-only scan cannot detect applications installed outside standard scan directories, but they are visible as running processes. Running process-based discovery closes that gap, giving SAM teams a more complete and accurate view of the software in use across your organization. This reduces risk and improves audit readiness.

## Platform coverage

Running process-based discovery supports Windows, Linux, and macOS. Coverage scope varies by operating system and depends on the privileges granted to the agent service account. For platform-specific coverage details and privilege requirements, see [Running process-based discovery platform coverage and properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/running-process-based-discovery-platform-coverage-properties.md).

-   **[Enable running process-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/enable-running-process-based-discovery.md)**  
Enable running process-based discovery so that the Agent Client Collector for Visibility - Content agent detects software running from directories outside your configured File-Based Discovery scan paths.
-   **[Exclude directories from running process-based discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/exclude-directories-running-process-based-discovery.md)**  
Exclude specific directories from running process-based discovery so that processes running from those locations aren't recorded or included in File-Based Discovery scans.

**Parent Topic:**[Agent Client Collector File-Based Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/file-based-discovery-overview.md)

