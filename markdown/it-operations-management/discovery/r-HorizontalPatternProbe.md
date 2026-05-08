---
title: Horizontal Pattern probe
description: Discovery uses the Horizontal Pattern probe to launch patterns for horizontal discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [List of Discovery probes, Discovery probes and sensors, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Horizontal Pattern probe

Discovery uses the Horizontal Pattern probe to launch patterns for horizontal discovery.

The Horizontal Pattern probe works with the Horizontal Discovery sensor to enable Discovery to use patterns for discovery. When you see messages in the ECC Queue from this probe, they appear with the ECC queue name **Pattern Launcher**, followed by the name of the pattern. The probe contains a sensor named **Horizontal Discovery Sensor**, which performs the actual updates of the CMDB based on identification rules.

If you create your own device or process classifier and you want to use patterns for discovery, you must [specify this probe in the classifier record](../concept/c-UsingPatternsForHorizontalDiscovery.md#). You do not need to modify this probe or the Horizontal Discovery sensor.

## Splitting payload

When Discovery uses patterns to find certain devices like load balancers, large amounts of data could be sent to the ECC Queue. To better handle large amounts of data, the horizontal pattern probe can split the payload into chunks, and then create multiple ECC Queue records.

Control how the MID Server splits payloads and handles payloads using properties. See MID Server properties for more information.

**Parent Topic:**[List of Discovery probes](r_ListOfDiscoveryProbes.md)

