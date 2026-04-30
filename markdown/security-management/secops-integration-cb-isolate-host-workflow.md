---
title: Security Operations Carbon Black Integration - Isolate Host Flow
description: The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Carbon Black Integration - Isolate Host Flow

The Security Operations Carbon Black Integration - Isolate Host is the implementation for the Carbon Black integration launched by the Security Operations Integration - Isolate Host flow.

## Before you begin

Role required: sn\_si.analyst

## About this task

The flow process flow action include:

-   [Execution Tracking - Begin \(CIs\) Flow Action](../reference/execution-tracking-begins-cis-activity.md)
-   [Get IP from CI](../reference/get-ip-from-ci-activity.md)
-   [Collect Carbon Black configurations](../reference/collect-cb-config-activity.md)
-   [Capability Execution Tracking- Failure Flow Action](../../security-operations-common/concept/capability-execution-tracking-failure.md)
-   [Get Sensor ID](../reference/get-sensor-id-activity.md)
-   [Set Network Isolation Enabled Flow Action](../reference/set-network-isolation-enabled-activity.md)
-   [Update Sensor](../reference/update-sensor-activity.md) - returns Isolate Host result.

![Flow designer for Security Operations Carbon Black Integration - Isolate Host](../image/carbon-black-integration-isolate-host-flow-v1.png)![Flow designer for Security Operations Carbon Black Integration - Isolate Host](../image/carbon-black-integration-isolate-host-flow-v1-2.png)

-   **[Get Sensor ID Flow Action](../reference/get-sensor-id-activity.md)**  
The Get Sensor ID flow action gathers sensor identifiers to use in the flow.
-   **[Set Network Isolation Enabled Flow Action](../reference/set-network-isolation-enabled-activity.md)**  
The Set Network Isolation Enabled flow action enables network isolation.
-   **[Update Sensor Flow Action](../reference/update-sensor-activity.md)**  
The Update Sensor flow action updates the sensor to isolate hosts or endpoints.

**Parent Topic:**[Security Operations Integration- Isolate Host capability](../../security-operations-common/concept/isolate-host-capability.md)

