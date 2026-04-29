---
title: Security Operations System Command Integration- Get Running Processes flow
description: The Security Operations System Command Integration - Get Running Processes flow retrieves the running processes of a configuration item when added or updated to a Windows or Unix-based security incident in the Analysis state.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Operations Integration- Get Running Processes capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations System Command Integration- Get Running Processes flow

The Security Operations System Command Integration - Get Running Processes flow retrieves the running processes of a configuration item when added or updated to a Windows or Unix-based security incident in the **Analysis** state.

## Before you begin

Role required: sn\_si.analyst

## About this task

For new security incidents, the flow runs automatically when you submit the incident with a selected configuration item, when the state automatically changes to **Analysis**. If it remains in the **Draft** state, then it does not run.

Existing security incidents are automatically updated when you are in the **Analysis** state and you add a new configuration item.

The flow process actions include:

-   [Get Configuration Item FQDN Flow Action](../../security-operations-orchestration/reference/get-config-FQDN-activity.md)
-   [Determine Shell Script by OS activity](../../security-operations-integrations/reference/determine-shell-script-by-os-activity.md)
-   [Execution Tracking - Begin Flow Action](../../security-operations-common/concept/execution-tracking-begin.md)
-   [Get Running Processes via PowerShell](../../security-operations-integrations/reference/get-running-processes-via-pwrshell-activity.md)
-   [Execute Shell Script activity](../../security-operations-integrations/reference/execute-shell-script-activity.md)
-   [Capability Execution Tracking- Failure Flow Action](../../security-operations-common/concept/capability-execution-tracking-failure.md)
-   [Extract Shell Script from MID Script activity](../../security-operations-integrations/reference/extract-shell-script-mid-script-activity.md)
-   [Combine Results](../../security-operations-integrations/reference/combine-results-activity.md) and return values in an array
-   [Create Enrichment Data records Flow Action](../../security-operations-common/concept/create-enrich-data-records.md)
-   [Capability Execution Tracking - Complete Flow Action](../../security-operations-common/concept/capability-execution-tracking-complete.md)

![Security Operations System Command Integration- Get Running Processes flow](../image/get-running-processes-flows.png "Get Running Processes")

## Procedure

1.  Open a security incident.

2.  Update the **State** to **Analysis**, if necessary.

3.  Add a configuration item \(computer, server, or similar\).

4.  Click **Update**.

    Security Incident Response Orchestration provides running process information in the **Related Link** &gt; **Security Incident Enrichments**tab. For more information, see [Security Operations enrichment data mapping](../../security-operations-common/concept/enrichment-data-mapping.md).

    Actions specific to this flow are described here. For more information on other actions, see [Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md).


-   **[Combine results activity](../../security-operations-integrations/reference/combine-results-activity.md)**  
The Combine results workflow activity merges the results from third-party integrations to use in the workflow.
-   **[Execute Shell Script activity](../../security-operations-integrations/reference/execute-shell-script-activity.md)**  
The Execute Shell Script workflow activity runs a MID server shell script within the workflow.
-   **[Extract Shell Script from MID Script activity](../../security-operations-integrations/reference/extract-shell-script-mid-script-activity.md)**  
The Extract Shell Script from MID script workflow activity pulls a MID server shell script to use with in the workflow.
-   **[Get Running Processes via PowerShell activity](../../security-operations-integrations/reference/get-running-processes-via-pwrshell-activity.md)**  
The Get Sensor ID workflow activity gathers running processes using PowerShell to use in the workflow.

**Parent Topic:**[Security Operations Integration- Get Running Processes capability](../../security-operations-common/concept/get-running-processes-capability.md)

