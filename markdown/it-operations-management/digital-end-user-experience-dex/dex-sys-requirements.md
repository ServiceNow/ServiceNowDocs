---
title: DEX system requirements
description: System requirements are the fundamental specifications and configuration needed to install and run DEX.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/dex-sys-requirements.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 1
breadcrumb: [Before you begin, Configure, Digital End-User Experience, IT Operations Management]
---

# DEX system requirements

System requirements are the fundamental specifications and configuration needed to install and run DEX.

Zurich Patch 1 is the minimum version required for Digital End-User Experience \(DEX\).

## DEX browser extension requirements

The minimum required browser versions for DEX browser extension are Google Chrome 114 or later and Microsoft Edge version 96 or later.

## Operating system compatibility

DEX is compatible with the following operating systems:

-   Microsoft Windows
    -   Windows 10 Enterprise Edition
    -   Windows 11 Professional
    -   Windows 11 Enterprise
    -   Windows 11 Surface on ARM64
-   Apple macOS
    -   Monterey
    -   Ventura
    -   Sonoma
    -   Sequoia

## CPU consumption

Digital End-User Experience \(DEX\) uses approximately 1% average CPU for both Windows and macOS devices.

## CPU protection threshold

When an agent meets the configured thresholds specified in the agent's `acc.yml` file, it enters CPU protection mode, either for an individual check or for all checks. For more information about the CPU protection threshold, see [Agent Client Collector CPU protection thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/agent-client-collector/acc-set-silent-reference.md)

**Note:** Configure the ACC CPU Protection Threshold to 20% for DEX deployments.

