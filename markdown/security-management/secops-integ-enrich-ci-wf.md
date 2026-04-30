---
title: Security Operations Integration - CI Enrichment flow
description: The Security Operations Integration - CI Enrichment flow allows you to enrich data in configuration items \(CI\) associated with a security incident.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Enrich CI capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration - CI Enrichment flow

The Security Operations Integration - CI Enrichment flow allows you to enrich data in configuration items \(CI\) associated with a security incident.

## Before you begin

Role required: sn\_si.analyst

## About this task

This flow is triggered from Security Incident Response in two ways.

-   by selecting one or more CIs from the **Configuration Items** tab \(under the **Affected Items** related link\) and selecting **Run CI enrichment** from the **Actions on selected rows** choice list.
-   by opening a CI record and clicking the **Run CI enrichment** related link.

Either method then allows you to specify which implementations to be used to enrich the selected CIs. The associated implementation flows are executed to perform the enrichment.

**Note:** The base system does not include an implementation flow for this capability. To enrich CIs, you must create your own implementation [flow](https://www.servicenow.com/docs/access?context=c_WorkflowOverview&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

![Security Operations Integration - CI Enrichment flow](../image/enrich-ci-flow.png "CI Enrichment")

Actions specific to this flow are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md).

The flow process actions include:

-   [Execution Tracking - Begin Flow Action](../../security-operations-common/concept/execution-tracking-begin.md)
-   [Security Operations Integration - CI Enrichment flow](secops-integ-enrich-ci-wf.md)
-   [Capability Execution Tracking- No Impls action](../reference/execution-tracking-noimpls-activity.md)
-   [Get Supported Security Capabilities action](../reference/get-supported-security-capabilities-activity.md)

**Parent Topic:**[Security Operations Integration- Enrich CI capability](../../security-operations-common/concept/enrich-ci-capability.md)

