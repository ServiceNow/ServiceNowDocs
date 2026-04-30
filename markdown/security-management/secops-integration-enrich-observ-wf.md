---
title: Security Operations Integration - Enrich Observable workflow
description: The Security Operations Integration - Enrich Observable sub flow allows you to enrich observables with additional information from a variety of sources using implementation flow designer.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Enrich Observable capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration - Enrich Observable workflow

The Security Operations Integration - Enrich Observable sub flow allows you to enrich observables with additional information from a variety of sources using implementation flow designer.

## Before you begin

Role required: sn\_si.analyst

## About this task

This workflow can be triggered from either Security Incident Response or Threat Intelligence in two ways.

-   by selecting one or more observables from the Observables list and selecting **Run observable enrichment** from the **Actions on selected rows** choice list.
-   by opening an observable record and clicking the **Run observable enrichment** related link.

Either method then allows you to specify which implementations to be used to enrich the selected observables. The associated implementation workflows are executed to perform the enrichment.



![Security Operations Integration - Enrich Observable](../image/flows-enrich-observables.png)

Activities specific to this flow are described here. For more information on other activities, see [Common Security Operations integration flows and orchestration Flow Actions](../../security-operations-common/concept/common-wf-activities.md).

Workflow process activities include:

-   [Capability Execution Tracking- No Impls activity](../reference/execution-tracking-noimpls-activity.md)
-   [Get Supported Security Capabilities activity](../reference/get-supported-security-capabilities-activity.md)[Capability Execution Tracking- No Impls activity](../reference/execution-tracking-noimpls-activity.md)

**Parent Topic:**[Security Operations Integration- Enrich Observable capability](../../security-operations-common/concept/enrich-observable-capability.md)

