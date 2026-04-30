---
title: Suggested resolutions in incident investigation with DEX
description: Review and execute suggested resolutions from the Investigation tab of incident records to resolve detected issues on DEX monitored devices.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-11-11"
reading_time_minutes: 1
breadcrumb: [Incident diagnostics and suggested resolutions, DEX for service desk agents, Digital End-User Experience, IT Service Management]
---

# Suggested resolutions in incident investigation with DEX

Review and execute suggested resolutions from the Investigation tab of incident records to resolve detected issues on DEX monitored devices.

## Suggested resolutions

View issue diagnosis and suggested resolutions to resolve detected device health issues. Each resolution card displays information such as the resolution name, related device health category, issue name and description, impacted metrics, resolution source, last attempted timestamp, and execution status.

Suggested resolutions are of the following types:

-   Self-help instruction: Displays steps that you can manually execute to resolve an issue.
-   Catalog request: Automatically submits a service catalog request for fulfillment.
-   Help resource: Link to documentation such as Knowledge Base articles and other web resources with steps that you can manually execute to resolve an issue.
-   Remedial action: Automated action executed on the end user's device to resolve an issue.

## Tracking completed actions

Track the status of completed resolutions, including actions that failed to execute, by selecting the **Completed** tab.

**Note:** Only actions executed from the Suggested resolutions in DEX incident investigation are displayed in the Completed action list.

An action card displays information like the action name, completion status, related device health category, issue name and description, action source, and completion time.

The available completion states for different resolution types are:

-   Remedial actions: Completed and Action failed.
-   Catalog requests: Item requested and Request completed.
-   Self-help instructions and help resources: Completed

## Action library for remedial actions

In addition to the suggested resolutions, you can run remedial actions from the Action library to resolve device and application issues. For more information, see [Run remedial actions from the Action library](../task/remedial-actions-action-library.md).

**Note:** Remedial actions run from the Suggested resolutions and Action library are added to a playbook in the DEX incident investigation page. You can monitor current and past actions or cancel ongoing actions from the playbook. For more information, see [Manage remedial actions in DEX incident investigation Playbook](../task/manage-incident-remedial-actions-playbook.md).

