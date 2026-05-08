---
title: DNS probe
description: DNS probes determine the DNS names for configuration items \(CI\).
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# DNS probe

DNS probes determine the DNS names for configuration items \(CI\).

The default DNS Name Resolver probe is a lightweight and fast probe. It achieves its speed by executing in parallel on the MID Server. The probe utilizes DNS lookup by the MID Server host OS to make use of the maintained DNS cache. The probe also leverages the hosts file on the OS.

These performance improvements can be disabled by reverting to the legacy DNS probe with either MID Server properties or parameters. The names of the MID Server properties/parameters are \[mid.probe.use\_legacy\_forward\_dns\] and \[mid.probe.use\_legacy\_reverse\_dns\]. For more information, see MID Server parameters and MID Server properties.

|Probe|Description|
|-----|-----------|
|DNS|Determines DNS names for devices. It has the parameter ip\_addresses.|
|DNSLookupProbe|Resolves the IP address of a host.|
|DNSNameResolver|Resolves the DNS name of an IP address.|

|Probe|Description|
|-----|-----------|
|dns|Triggered by 'dns'. Uses 'DNS Name Resolver' Scanner and uses classification 'Process Classification \[discovery\_classy\_proc\]'|

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

