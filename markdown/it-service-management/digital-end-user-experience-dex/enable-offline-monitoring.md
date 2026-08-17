---
title: Enable offline monitoring
description: Enable offline monitoring so that metrics collected on a device while it's disconnected from the instance are automatically resent once the device reconnects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/enable-offline-monitoring.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [offline monitoring, data loss handler, enable data loss job, offline data recovery]
breadcrumb: [Collecting DEX metrics, Configure, Digital End-User Experience, IT Service Management]
---

# Enable offline monitoring

Enable offline monitoring so that metrics collected on a device while it's disconnected from the instance are automatically resent once the device reconnects.

## Before you begin

Role required: admin

## About this task

When a device running DEX loses connectivity to the instance, OpenTelemetry \(OTel\) metrics continue to be collected on the device. The metrics are sent to the instance when connectivity is restored. The **DEX Data Loss Handler** scheduled job detects this gap and resends the queued data once the device reconnects. This job is installed but inactive by default. After you activate the job, it runs every hour and resends any data lost while a device was offline. Loss-metric reports include data only for agents currently marked active.

**Note:** For offline monitoring, DEX can process a maximum of 24 million data points per day across all devices.

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Scheduled Jobs**.

2.  In the **Name** filter, search for `Data loss handler`.

3.  Open the **DEX Data Loss Handler** record.

4.  Select the **Active** check box.

5.  Select **Update**.


