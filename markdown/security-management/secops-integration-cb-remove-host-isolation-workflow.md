---
title: Security Operations Carbon Black Integration- Remove Host Isolation Flow
description: The Security Operations Carbon Black Integration - Remove Host Isolation flow unblocks communication with a specified host or endpoint in a Carbon Black system.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Isolate Host capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Carbon Black Integration- Remove Host Isolation Flow

The **Security Operations Carbon Black Integration - Remove Host Isolation** flow unblocks communication with a specified host or endpoint in a Carbon Black system.

## Before you begin

Role required: sn\_si.analyst

## About this task

This flow is not part of a capability and needs a custom orchestration in order to run.

The flow process activities include:

-   [Get IP from CI Flow Action](../reference/get-ip-from-ci-activity.md)
-   If successful- [Collect Carbon Black Configurations Flow Action](../reference/collect-cb-config-activity.md)
-   [Get Sensor ID Flow Action](../reference/get-sensor-id-activity.md)[Get Sensor ID](../reference/get-sensor-id-activity.md)
-   If- Device supports isolation- and device is not isolated-[Set Network Isolation Enabled Flow Action](../reference/set-network-isolation-enabled-activity.md) to disabled.
-   [Update Sensor Flow Action](../reference/update-sensor-activity.md)- returns Isolate Host result.

![Remove Host Isolation flow diagram](../image/RemoveHostIsolationWorkflow.png "Carbon Black Integration- Remove Host Isolation")

**Parent Topic:**[Security Operations Integration- Isolate Host capability](../../security-operations-common/concept/isolate-host-capability.md)

