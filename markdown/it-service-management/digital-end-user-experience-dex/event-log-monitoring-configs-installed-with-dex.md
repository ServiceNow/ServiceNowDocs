---
title: Event log monitoring configurations installed with DEX
description: The Application and Device Health plugin \(com.sn\_dex\) installs 20 event log monitoring configurations that are active by default. Use this reference to identify the monitored events, log sources, and matching criteria for Windows and macOS devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/event-log-monitoring-configs-installed-with-dex.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-07-28"
reading_time_minutes: 2
keywords: [event log monitoring config, base system events, windows event log, macos unified log, event monitoring, default event configurations, com.sn\_dex, event log monitoring configs table, device health plugin, windows event ids, macos system log, vpn connection failure, application crash monitoring, failed login attempt, usb device monitoring, kernel panic, endpoint event tracking]
audience: administrator
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Event log monitoring configurations installed with DEX

The Application and Device Health plugin \(com.sn\_dex\) installs 20 event log monitoring configurations that are active by default. Use this reference to identify the monitored events, log sources, and matching criteria for Windows and macOS devices.

The Application and Device Health plugin \(com.sn\_dex\) installs 20 event log monitoring configurations in the Event Log Monitoring Configs table. All 20 configurations are active by default: 11 for Windows and 9 for macOS.

**Note:** These base system configurations count toward the 25-event maximum per operating system. On Windows, the 11 base system configurations leave 14 available for custom events. On macOS, the 9 base system configurations leave 16 available. To add a custom event, remove any base system configuration you don't need. See [Add an event to monitor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/add-event-to-monitor.md). For field descriptions, see [New DEX event form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/new-dex-event-form.md).

|Configuration name|Event ID|Log source|
|------------------|--------|----------|
|Resource exhaustion / low memory|2004|System|
|Windows Update installation failure|20|Setup|
|Wi-Fi – WLAN connection failed|8001|System|
|VPN connection failure|20227|System|
|Application crashes|1000|Application|
|Windows Defender threat detected|1116|Microsoft-Windows-Windows Defender/Operational|
|Device driver load failure|219|System|
|Failed login attempt|4625|Security|
|Unexpected system shutdown|41|System|
|USB device connected|2003|System|
|MSI installer failure|1024|Application|

|Configuration name|Process|Subsystem or category|Query type|Event message|
|------------------|-------|---------------------|----------|-------------|
|VPN disconnected|locationd|com.apple.networkextension|Contains|NEVPNConnectivityStateDisconnecting|
|Software installation failed|installer|—|Regex|.\*\(Installation\|Package\|cancelled\).\*|
|Software update failed|softwareupdated|—|Regex|.\*\(failed\|error\|unable\|download\|install\).\*|
|USB storage mounted|—|com.apple.DiskArbitration|Contains|mounted|
|Login failed|authorizationhost|com.apple.Authorization|Contains|pam\_authenticate failed|
|Wi-Fi disconnected|wifip2pd|com.apple.wifip2pd|Contains|not associated|
|USB device connected|kernel|—|Contains|enumerated|
|Kernel panics|kernel|com.apple.system.logging.kernel\_panics|Contains|panic|
|Application crash|loginwindow|com.apple.loginwindow.logging|Contains|crashed|

**Parent Topic:**[DEX Application and Device Health reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-console-reference.md)

