---
title: Security Operations Integration - Threat Lookup workflow
description: The Security Operations Integration - Threat Lookup capability workflow accesses available threat lookup implementations and executes the implementation workflows associated with each to perform threat lookups of selected observables.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration - Threat Lookup capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration - Threat Lookup workflow

The **Security Operations Integration - Threat Lookup** capability workflow accesses available threat lookup implementations and executes the implementation workflows associated with each to perform threat lookups of selected observables.

## Before you begin

Role required: sn\_ti.write

## About this task

This workflow can be triggered in these ways.

-   by selecting one or more observables from the Observables list and selecting **Run threat lookup** from the **Actions on selected rows** choice list.
-   by opening an observable record and clicking the **Run threat lookup** related link.
-   From the Observables related list in a security incident.

Each method then allows you to specify which lookup implementations to be used to scan the selected observables. The associated implementation workflows are executed to perform the lookups.

![Security Operations Integration - Threat Lookup](../image/sec-ops-iteg-threat-lookup-wf.png "Threat Lookup")

Activities specific to this workflow are described here. For more information on other activities, see [Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md).

Workflow process activities include:

-   [Get Supported Security Capabilities activity](../reference/get-supported-security-capabilities-activity.md)
-   [Capability Execution Tracking- No Impls activity](../reference/execution-tracking-noimpls-activity.md)

**Parent Topic:**[Security Operations Integration - Threat Lookup capability](../../security-operations-common/concept/sec-ops-threat-lookups-capability.md)

