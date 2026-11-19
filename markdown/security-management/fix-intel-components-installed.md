---
title: Components installed with Fix Intelligence for Security Exposure Management
description: Activating the Fix Intelligence for Security Exposure Management plugin \(sn\_vul\_fix\) installs the following tables, role, scripts, automation, and integration components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/fix-intel-components-installed.html
release: yokohama
topic_type: reference
last_updated: "2026-07-29"
reading_time_minutes: 1
keywords: [components installed, sn\_vul\_fix, Fix Intel]
breadcrumb: [Reference, Fix Intelligence for Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Components installed with Fix Intelligence for Security Exposure Management

Activating the Fix Intelligence for Security Exposure Management plugin \(`sn_vul_fix`\) installs the following tables, role, scripts, automation, and integration components.

## Tables

|Table|Purpose|
|-----|-------|
|`sn_vul_fix_intel` \(Fix\)|Stores one record per unique fix.|
|`sn_vul_fix_cache`|Link cache used to compute finding links per sync.|
|`sn_vul_fix_download_queue`|Work queue of sync files to download.|
|`sn_vul_fix_import`|Import-set staging table for inbound fix data.|

The plugin also adds a read-only `fix_intel` reference column to the Vulnerability Response `sn_vul_vulnerable_item` and `sn_vul_vulnerability` tables, and to the Remediation Task table.

## Role

`sn_vul_fix.read` grants read access to the Fix tables. It is contained by the Vulnerability Response read roles, so existing VR users inherit it.

## Automation and integration

-   **Poll and Store Fix Intelligence Data** flow and its action, triggered on a scheduled timer.
-   A business rule set that advances the sync watermark, triggers the risk rollup, drives fix-based grouping, and derives the risk rating.
-   A scheduled job that bootstraps the Fix Intelligence for SEM dashboard widgets and then disables itself.
-   The **Fix Intelligence Connection** connection alias and outbound REST message, which ServiceNow Support configures.

**Parent Topic:**[Fix Intelligence for SEM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/fix-intel-reference.md)

**Related topics**  


[Security Exposure Management Workspace Components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/sem-components-installed.md)

