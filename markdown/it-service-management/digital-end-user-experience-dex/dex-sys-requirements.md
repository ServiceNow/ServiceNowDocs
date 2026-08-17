---
title: DEX system requirements
description: System requirements are the fundamental specifications and configuration needed to install and run DEX effectively.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/dex-sys-requirements.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Digital End-User Experience, IT Service Management]
---

# DEX system requirements

System requirements are the fundamental specifications and configuration needed to install and run DEX effectively.

Vancouver Patch 6 is the minimum version required for DEX.

## Supported ACC versions

DEX supports Agent Client Collector Framework \(ACC-F\) versions 3.4.1 and 3.5.1.

## DEX browser extension requirements

The minimum required browser versions for DEX browser extension are Google Chrome 114 or higher, and Microsoft Edge version 96 or higher.

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

Digital End-User Experience \(DEX\) utilizes approximately 1% average CPU consumption for both Windows and macOS devices.

## CPU protection threshold

When an agent meets the configured thresholds specified in the agent's `acc.yml` file, it enters CPU protection mode, either for an individual check or for all checks. For more information on the CPU protection threshold see, [Agent Client Collector CPU protection thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/acc-set-silent-reference.md)

**Note:** Configure the ACC CPU Protection Threshold to 20% for DEX deployments.

