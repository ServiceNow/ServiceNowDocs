---
title: Monitor and manage instance health
description: The full and delta instance scan feature with Impact Platform Health Scan Engine enables ServiceNow administrators and developers to initiate, monitor, and manage instance health.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/scan-engine-parallel-processing.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Exploring Impact, Impact]
---

# Monitor and manage instance health

The full and delta instance scan feature with Impact Platform Health Scan Engine enables ServiceNow administrators and developers to initiate, monitor, and manage instance health.

Administrators receive real-time scan-state visibility and contextual notifications at each stage of scan execution, from initiation and queuing to completion or cancellation.

Two UI action buttons are available to Initiate Scan and Force Full Scan, allowing context-aware scan initiation with immediate feedback on scan status and resource availability.

-   **Initiate Scan**: Intelligently determines the scan type as whether to run a full or delta scan based on instance history, reducing user decision-making burden while optimizing scan efficiency.
-   **Force Full Scan**: Administrators retain the ability to override an in-progress scan when a complete instance scan is needed instead of a delta scan, providing flexibility while maintaining resource control.

Users can see whether their scan was initiated, queued, or blocked, preventing duplicate requests. The system determines whether to run a full or delta scan based on instance history and enforces concurrency rules to protect instance performance. Only one full instance scan can run at a time. Scan status is visible to users, preventing repeated execution attempts.

## Key capabilities

-   **Real-time status visibility:** Clear indicators showing scan states \(in progress, queued, complete\)
-   **Scan cancellation:** Ability to cancel in-flight scans or queued requests
-   **Safe concurrency:** Update Set Scans and Application Scans can execute while full scans are running

## Prevent and resolve technical debt

The Scan Engine examines your instances for findings related to active definitions stored in the Scan Findings table.

Impact Platform Health delivers AI-generated code fixes at two critical points in your development lifecycle. Whether you're actively writing code or cleaning up existing technical debt, the Scan Engine detects violations against your defined coding standards and ServiceNow Otto generates fixes automatically.

You can view findings, apply manual fixes, generate AI-suggested fixes, or submit exceptions for findings you believe aren't valid.

This unified approach reduces manual remediation time and improves platform quality across your ServiceNow instances.

**Related topics**  


[Platform Health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/platform-health-idi.md)

[Manage and monitor scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/initiate-manage-scan-engine.md)

[Prevent and resolve technical debt with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/prevent-resolve-technical-debt-ai.md)

