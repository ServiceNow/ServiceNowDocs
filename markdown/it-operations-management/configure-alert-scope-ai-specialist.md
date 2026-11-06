---
title: Configure alert scope
description: Define which alerts your AI specialist receives by setting filter conditions—the AI specialist is only assigned alerts that match all active conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/configure-alert-scope-ai-specialist.html
release: australia
topic_type: task
last_updated: "2026-11-01"
reading_time_minutes: 2
keywords: [alert scope, AI specialist, configure, filter]
breadcrumb: [Onboard the AIOps specialist, AIOps AI Specialist, ITOM AIOps specialists, AI in ITOM AIOps, ITOM AIOps, IT Operations Management]
---

# Configure alert scope

Define which alerts your AI specialist receives by setting filter conditions—the AI specialist is only assigned alerts that match all active conditions.

## Before you begin

Very you have the following setting

-   Platform version Brazil Patch 2 or later.
-   ServiceNow Otto for IT Operations Management \(ITOM\) application, version 2.10.0 or later.
-   AIOps Experience application, version 27.2.68 or later.
-   AIOps AI Specialist \(sn\_ai\_aiops\_force\) plugin, version 3.0.0 or later.

-   You're on the AIOps AI Specialist page and a profile is created for the AI specialist.
-   Role required: evt\_mgmt\_admin or evt\_aiops\_manager

## About this task

Alert Scope is the set of filter conditions that controls which alerts your AI specialist receives and acts on. Only alerts that match the defined scope are assigned to the AI specialist. Everything else goes to your human operators.

Scope keeps the AI specialist precise. A well-defined scope means the AI focuses on the alert types it is best suited to handle. It reduces noise for your operators and helps avoiding mismatched assignments.

## Procedure

1.  On the AIOps AI Specialist page, select the **Tasks** tab.

2.  Under **Scoping**, review the default filter conditions already applied out-of-the-box to determine which alerts are relevant for the AI specialist.

    \[Omitted image "ai-specialist-scope.png"\] Alt text: Define alert scope for the AI specialist.

    To add a custom filter condition, select the edit icon \(\[Omitted image "icon-edit.png"\] Alt text: Edit icon\). You can filter by alert source, severity, type, category, or configuration item. Combine multiple conditions to narrow the scope precisely.

    \[Omitted image "ai-specialist-scope-cust-cond.png"\] Alt text: Add custom conditions to control which alerts the AI specialist handles

3.  Review all active conditions together.

    **Important:** All active conditions are evaluated as AND logic. An alert must match every condition to be assigned to this AI specialist. If you want to handle alerts from two different sources, you will need two separate scope configurations or a condition that uses an **in** operator to list multiple values.

4.  Select **Apply**.

    You can change the scope at any time, even after the AI specialist is active on your team. Changes take effect immediately. Alerts already in the AI specialist's queue before the scope change are not affected. The updated conditions apply only to new incoming alerts.

5.  Select **Save**.


## What to do next

[Configure task modules for the AIOps AI Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/configure-task-modules-ai-specialist.md) to control what the AI specialist does when it receives an alert.

**Parent Topic:**[Onboard the AIOps specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/onboard-ai-specialist.md)

