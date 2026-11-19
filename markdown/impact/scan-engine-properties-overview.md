---
title: Scan Engine properties
description: Use Scan Engine properties to control when scans run, what they cover, who sees findings, and how your teams govern code before it moves to production.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-properties-overview.html
release: brazil
topic_type: concept
last_updated: "2026-11-13"
reading_time_minutes: 5
keywords: [scan engine properties, scan configuration, scan scope, governance]
breadcrumb: [Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Scan Engine properties

Use Scan Engine properties to control when scans run, what they cover, who sees findings, and how your teams govern code before it moves to production.

Role required: `sn_se.scan_engine_admin`

## Why configure properties

In the base system, the Scan Engine runs with defaults that work for most instance setups. When you configure properties, you tailor scanning to your instance and your development process.

Configure properties to:

-   Schedule scans for the times that suit your instance.
-   Limit scan scope so that scans focus on the code you own.
-   Control how findings are tracked, retained, and counted toward technical debt.
-   Give developers feedback while they write code, and require them to resolve serious findings.
-   Set approval rules for exceptions, update sets, and pushes.
-   Connect instances so that definitions and exceptions integrate and stay consistent across your instance stack.

## What each set of properties does

Select a topic to see the full configuration steps.

|Property type|Description|
|-------------|-----------|
|[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md)|Activate the Scan Engine, schedule scans, set scan scope, track resolved findings, and set how long finding history is kept. See [Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md) for details on how scans work.|
|[Configure definition properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/additional-scan-engine-properties.md)|Control how definitions behave, including deactivation and how overrides and custom definitions sync between instances. See [Initiate limited definition scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-limited-def-scans.md) on definition scans.|
|[Configure scan filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-filters.md)|Exclude applications, tables, or individual records from scans. See [Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md) for information on scanning your instances.|
|[Configure real-time scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-real-time-scanning-properties.md)|Activate and choose who sees real-time findings, require users to resolve findings before they save, and set which tables and how many lines are scanned in real time. See [Run Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/run-scan-engine.md) for additional information on scanning your instances. See [Prevent and resolve technical debt with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/prevent-resolve-technical-debt-ai.md) for details on working with findings.|
|[Configure real-time code resolution with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-ai-code-fix-for-platform-health.md)|Turn on AI suggested fixes so that developers can resolve findings in real time. [Use Real-time prevention monitoring while coding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/real-time-prevention-monitoring.md) for managing findings while coding.|
|[Configure exception reason properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-reason-properties.md)|Decide which finding levels can have exceptions, who approves them, and what happens when a finding is detected again. See [Exception handling in Scan Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/exception-handling-overview.md) for working with exceptions.|
|[Configure update set scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/update-set-scanning-properties2.md)|Choose which update sets are scanned and require them to meet conditions before developers mark them complete. See [Initiate update set scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-update-set-scans.md) for scanning details.|
|[Configure Team Dev scanning properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/teamdev-scanning-properties.md)|Scan Team Dev code pushes that are pending review, set rules to approve or reject them automatically, and define teams and team leads for the dashboards. See [Track Platform Health trends](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/scan-engine-diagnostic-dashboards.md) for information on dashboards.|
|[Define My SN Instance environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/add-view-scan-engine-related-lists.md)|Define your instance environments to use exception processing, definition syncing, and user story tracking. See [Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-integration-scan-engine.md) for additional information on syncing between instances.|

-   **[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md)**  
Configure the primary scanning capabilities and configuration options for scheduled, on-demand, and real-time scans.
-   **[Customize Scan Engine definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/view-modify-scan-engine-properties.md)**  
You can modify an existing definition to further customize and refine its scanning criteria or deactivate a definition.

**Parent Topic:**[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-initial-scan-engine-settings.md)

