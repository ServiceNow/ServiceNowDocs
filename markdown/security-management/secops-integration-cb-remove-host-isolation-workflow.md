---
title: Security Operations Carbon Black Integration- Remove Host Isolation Flow
description: The Security Operations Carbon Black Integration - Remove Host Isolation flow unblocks communication with a specified host or endpoint in a Carbon Black system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
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

-   [Get IP from CI activity](../reference/get-ip-from-ci-activity.md)
-   If successful- [Collect Carbon Black Configurations Flow Action](../reference/collect-cb-config-activity.md)
-   [Get Sensor ID Flow Action](../reference/get-sensor-id-activity.md)[Get Sensor ID](../reference/get-sensor-id-activity.md)
-   If- Device supports isolation- and device is not isolated to disabled.
-   [Update Sensor activity](../reference/update-sensor-activity.md)- returns Isolate Host result.

![Remove Host Isolation low diagram](../image/RemoveHostIsolationWorkflow.png "Carbon Black Integration- Remove Host Isolation")

**Parent Topic:**[Security Operations Integration- Isolate Host capability](../../security-operations-common/concept/isolate-host-capability.md)

