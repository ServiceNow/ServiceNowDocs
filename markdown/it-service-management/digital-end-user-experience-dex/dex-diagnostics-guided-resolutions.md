---
title: Incident investigation with DEX
description: Service desk agents can diagnose and resolve issues for Digital End-User Experience \(DEX\) monitored devices from an incident record by using DEX diagnostics and suggested resolutions.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-11-03"
reading_time_minutes: 3
breadcrumb: [DEX for service desk agents, Digital End-User Experience, IT Service Management]
---

# Incident investigation with DEX

Service desk agents can diagnose and resolve issues for Digital End-User Experience \(DEX\) monitored devices from an incident record by using DEX diagnostics and suggested resolutions.

Incident investigation with DEX provides a comprehensive view of device and application health metrics, issue diagnosis, and suggested resolutions. It helps identify and resolve common device and application issues, leading to faster incident resolution and enhanced service desk experience.

**Important:** Incident investigation with DEX is available from the Zurich release and requires Service Operations Workspace for ITSM version  8.2 or later.

## Accessing DEX incident diagnostics and suggested resolutions

You can access incident diagnostics and suggested resolutions for DEX monitored devices from the **Investigation** tab of an incident record page. Navigate to the Service Operations Workspace and open the incident record from the Incidents list. For more information, see [Incident Management in Service Operations Workspace](../../service-operations-workspace/concept/incident-sow.md) and [Features of the Investigation tab](../../service-operations-workspace/reference/features-of-investigation-tab.md).

**Important:** The configuration item \(CI\) associated with the incident record must be a DEX monitored device.

![DEX incident diagnostics and suggested resolutions accessed from the Investigation tab of an incident record](../image/dex-diagnostics-investigation.png "DEX incident diagnostics and suggested resolutions")

## Device health and metric checklist

Review the overall health and performance of the device associated with the incident record in the Device health section. The Device health checklist shows details of device and application metrics for a specified duration. For more information, see [Reviewing device health metrics in incident investigation with DEX](device-health-metrics.md).

Selecting the Refresh icon ![](../image/icon-dex-refresh.png) displays the latest available data for device and application metrics.

## Top processes by CPU and memory usage

Monitor the top processes by CPU and memory usage on DEX monitored devices. Automated snapshots captured periodically for different time range options show the top processes by CPU and memory usage on a device and the combined average usage percentages for these processes. For more information, see [Reviewing top processes by resource usage in incident investigation with DEX](process-snapshot.md).

## Suggested resolutions and remedial actions

View issue diagnosis and suggested resolutions to improve device and application performance in the **Suggested resolutions** tab. For more information, see [Suggested resolutions in incident investigation with DEX](dex-suggested-resolutions.md).

In addition to the suggested resolutions, you can run remedial actions from the Action library to resolve device and application issues. For more information, see [Run remedial actions from the Action library](../task/remedial-actions-action-library.md).

## Playbook Experience for remedial actions

Use the Playbook Experience in incident investigation with DEX to view details of remedial actions in progress, cancel ongoing actions, and view playbook history. For more information, see [Manage remedial actions in DEX incident investigation Playbook](../task/manage-incident-remedial-actions-playbook.md).

