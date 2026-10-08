---
title: Trigger remedial actions from flows
description: Trigger DEX remedial actions from a flow in Workflow Studio to remediate issues on a device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/Trigger-ra-flow.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-10-06"
reading_time_minutes: 1
keywords: [remedial actions, flows, Workflow Studio, device health]
breadcrumb: [Creating DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Trigger remedial actions from flows

Trigger DEX remedial actions from a flow in Workflow Studio to remediate issues on a device.

## When to use a flow

Workflow Studio is a ServiceNow interface for building flows, subflow, and actions. Create a flow in Workflow Studio to run a remedial action as a process step. Run it after an approval, when a requested item is fulfilled, or on a schedule.

## How it works

Your flow calls the **Execute remedial action** subflow, which is included with the DEX Application and Device Health application. A subflow is a reusable sequence of actions that a flow can trigger.

-   Your flow passes the three subflow inputs:
    -   The device, which is its computer configuration item \(CI\) in the Configuration Management Database \(CMDB\).
    -   The remedial action, which can be any active base system or custom remedial action.
    -   The remedial action parameters.
-   The subflow checks that the action can run on the device, and then triggers it.
-   The subflow waits for the action to finish and returns the outcome to your flow.
-   When a remedial action runs, the system creates a remedial action execution record. You can view these records, along with runs from the Action Library, in the Remedial Action Executions list.

## Requirements

-   DEX Application and Device Health \(ADH\) version 5.3.2 or later.
-   An active remedial action that supports the operating system of the device. To create one, see [Create a remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-remedial-action.md).

