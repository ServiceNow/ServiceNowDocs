---
title: Device action execution states and offline behavior
description: Device actions report their progress through execution state codes, and the platform queues actions that are triggered on offline devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/device-actions-states.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [DEX Self-service reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Device action execution states and offline behavior

Device actions report their progress through execution state codes, and the platform queues actions that are triggered on offline devices.

|State|Code|Description|
|-----|----|-----------|
|Running|602|Action is currently executing. Also applies to actions queued for execution on an offline device.|
|Declined|605|The end user declined the confirmation prompt without running the action.|
|Closed successful|606|Action completed successfully.|
|Closed unsuccessful|607|Action completed but the remediation failed. Review the linked task record for failure details.|

## Device actions on offline devices

When a device action is triggered on an offline device, the platform queues the action and retries it automatically when the device reconnects. Queued actions are valid for one calendar day. If the device does not reconnect before the end of the calendar day, the action must be triggered again.

When the device is offline, the interface indicates that the action could not be completed immediately. The end user receives a notification when the queued action executes.

Queued actions remain in the Running state until the device reconnects and the action completes or fails.

**Note:** The platform processes queued actions in batches of 200, with a 10-second delay between batches.

