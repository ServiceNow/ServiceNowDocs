---
title: Full and delta instance scan initiation
description: The full and delta instance scan feature enables ServiceNow administrators and developers to initiate, monitor, and manage instance scans directly from the Scan Results list view.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Full and delta instance scan initiation

The full and delta instance scan feature enables ServiceNow administrators and developers to initiate, monitor, and manage instance scans directly from the Scan Results list view.

The system intelligently determines whether to run a full or delta scan based on instance history, while enforcing concurrency rules to protect instance performance. Administrators receive real-time scan-state visibility and contextual notifications at each stage of scan execution, from initiation and queuing to completion or cancellation.

Two UI action buttons are available on the Scan Results list view, Initiate Scan and Force Full Scan. These options provide context-aware scan initiation with immediate feedback on scan status and resource availability.

-   **Initiate Scan**: Intelligently determines the scan type as whether to run a full or delta scan based on instance history, reducing user decision-making burden while optimizing scan efficiency.
-   **Force Full Scan**: Administrators retain the ability to override an in-progress scan when a complete instance scan is needed instead of a delta scan, providing flexibility while maintaining resource control.

Users gain visibility into whether their scan was initiated, queued, or blocked preventing repeated scan execution requests, but, resulting in no actual scan being executed. The system intentionally restricts users from running multiple full instance scans in parallel. Scan status is prioritized with visibility to the primary users with an indication of scan state preventing repeatedly attempted scan execution.

## Key capabilities

-   **Real-time status visibility:** Clear indicators showing scan states \(in progress, queued, complete\)
-   **Scan cancellation:** Ability to cancel in-flight scans or queued requests
-   **Safe concurrency:** Update Set Scans and Application Scans can execute while full scans are running

## Concurrency rules and scan behavior

Full and Delta scan supports update set scans and application scope scans. The Scan Engine enforces specific concurrency rules to protect instance performance and manage resource allocation:

-   **First scan behavior:** If the instance does not have any prior full scan, selecting **Initiate Scan** triggers a Full Instance Scan. Consecutive scans will be Delta Instance Scans.
-   **Full Instance Scan blocking:** Only one Full Instance Scan can run at a time. The system prevents parallel full scans to avoid excessive resource load. Additional full scan requests are blocked with an alert message.
-   **In-progress alerts:** If a scan is already in progress, attempting to initiate another scan displays an alert: "Cannot initiate a delta scan while another scan is in progress. Please wait for the current scan to complete or use Force Full Scan to override."
-   **Force Full Scan override:** Administrators can use the **Force Full Scan** button to cancel the current scan and immediately start a new Full Instance Scan. The current scan is cancelled automatically, and the new full scan is initiated.
-   **Parallel scan allowance:** While certain scans run, Update Set Scans and Application Scans can still execute concurrently without blocking.
-   **Scan status visibility:** Users can see scan states in real-time on the Scan Results list view, including "Getting ready," "Complete," and "Cancelled" status indicators.

## User notifications and status indicators

The system provides contextual notifications and visual indicators to keep users informed:

-   **Scan triggered message:** When a scan is successfully initiated, users see: "A new scan has been triggered and it will take a moment to reflect in the queue. Please refresh the page for the latest scan results."
-   **Scan in progress alert:** When attempting to initiate a scan while one is already running, an alert displays: "Cannot initiate a delta scan while another scan is in progress. Please wait for the current scan to complete or use Force Full Scan to override."
-   **Trigger Scan modal:** When using Force Full Scan while a Delta Scan is in progress, a confirmation modal appears with the title "Trigger Scan" and message: "A Delta Scan is currently in progress. Do you want to cancel the ongoing Delta Scan and start a Full Scan instead?" Users can select **OK** to proceed or **Cancel** to abort.
-   **Real-time updates:** The Scan Results list view displays scan metadata including Number \(PSR\#\), Start Time, Scan Type \(Full Instance Scan, Delta Instance Scan, On Demand Instance Scan\), Status, and Scan Engine Score.

**Note:** Users must refresh the page to see the latest scan status updates in the queue.

## Access control by persona

Scan initiation capabilities are determined by user roles:

|Role|Permissions|
|----|-----------|
|Admin|Initiate scans and Force Full Scan|
|AI Fix User|Initiate scans only|
|Scan User|No scan initiation buttons \(view only\)|
|Read User|No scan initiation buttons \(view only\)|

**Note:** See [Roles installed with Impact](../reference/impact-roles.md) for additional information on user roles.

**Related topics**  


[Initiating parallel scans](../task/scan-engine-parallel-processing-task.md)

