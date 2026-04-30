---
title: GCP Events pattern-based discovery
description: Discovery uses event patterns to update GCP component data in near real-time. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-01-12"
reading_time_minutes: 1
keywords: [GCP Events, Google Cloud Platform Events, GCP event discovery, GCP patterns]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# GCP Events pattern-based discovery

Discovery uses event patterns to update GCP component data in near real-time. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the GCP discovery prerequisites section in [Google Cloud Platform \(GCP\) Cloud components discovery using Patterns](gcp-cloud-discovery-patterns.md).

## Events discovered by Discovery during horizontal discovery

When GCP components change state, events are created. Discovery uses event patterns to detect these changes and update the CMDB.

|Pattern|CI|
|-------|---|
|Google Cloud Platform \(GCP\) - Networking - Events|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Cloud Platform \(GCP\) - Networking Firewall - Events|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|
|Google Cloud Platform \(GCP\) - Subnetwork - Events|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

