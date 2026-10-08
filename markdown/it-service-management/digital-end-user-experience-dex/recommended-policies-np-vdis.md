---
title: Recommended VDI policies and configuration files for NPVDIs
description: VDI policy and VDI configuration file records to activate on your instance so that DEX can monitor non-persistent \(NP\) Virtual Desktop Infrastructures \(VDIs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/recommended-policies-np-vdis.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-10-01"
reading_time_minutes: 1
keywords: [non-persistent vdi, vdi policies, vdi configuration files, sn\_agent\_vdi\_policy, sn\_agent\_vdi\_config\_file, agent client collector]
audience: administrator
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Recommended VDI policies and configuration files for NPVDIs

VDI policy and VDI configuration file records to activate on your instance so that DEX can monitor non-persistent \(NP\) Virtual Desktop Infrastructures \(VDIs\).

Configure these records as described in [Prepare agent deployment on a non-persistent virtual desktop infrastructure machine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/npvdi-agent-instance-prep.md).

**Note:** For each record listed in this topic, make sure **Active** is set to `true`.

## VDI policies

Configure the following records in the VDI Policies \[sn\_agent\_vdi\_policy\] table.

|Policy|Used for|
|------|--------|
|Enhanced Discovery Policy|SaaS and installed usage|
|VISC Get application metric|SaaS and installed usage|
|SAM background policy \(Non OsqueryD\)|SaaS and installed usage|
|VISC Get browser extension init|SaaS and installed usage|
|VISC Get browser extension device init|SaaS and installed usage|
|SAM discovery|SaaS and installed usage|
|DEX NP VDI Windows Device Metrics|DEX performance metrics|
|DEX NP VDI Windows Apps Metrics|DEX performance metrics|
|DEX Local Metric Tag Enrichment|DEX performance metrics. Requires version 4.3.2 or later.|
|DEX Metrics Reporter|DEX performance metrics|
|DEX Metric Aggregations|DEX performance metrics|

## VDI configuration files

Configure the following records in the VDI Configuration Files \[sn\_agent\_vdi\_config\_file\] table.

|Configuration file|Used for|
|------------------|--------|
|AccVisMonitoredUrls|SaaS and installed usage|
|MonitoredServiceApps|SaaS and installed usage|
|DEXAgentSystemConfig|DEX performance metrics|
|DEXMetricEnrichmentSchema|DEX performance metrics|
|DEXMetricRulesConfig|DEX performance metrics|
|DEXMonitoredInstalledApps|DEX performance metrics|
|DEXAdvancedAppMonitoringConfig|DEX performance metrics|

For the check instances, frequencies, and parameters that these policies run, see [DEX policies for non-persistent VDIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-policies-np-vdis.md).

To configure the agent on the golden image, see [Enable a non-persistent virtual desktop infrastructure agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/enable-npvdi-agent.md).

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)

