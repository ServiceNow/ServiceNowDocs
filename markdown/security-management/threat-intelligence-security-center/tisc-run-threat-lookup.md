---
title: Run Threat Lookup
description: Select one or more implementations as applicable to run threat lookup on observables.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Run Enrichment operations in TISC, Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Run Threat Lookup

Select one or more implementations as applicable to run threat lookup on observables.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Observables** &gt; **All Observables**.

4.  Open any observable record.

5.  Click **Run Threat Lookup**.

    The Run Threat Lookup **Select Implementations** modal screen is displayed.

    **Note:** The Run Threat Lookup performs the threat intelligence lookups to determine whether the observables are associated with any known threats.

6.  Select the required implementation\(s\) from the list.

    ![Run Threat lookup](../image/tisc-observable-run-threat-lookup-modal.png)

7.  Click **Submit**.

    The selected enrichment action will be executed and an information message is displayed that Threat lookup execution has started.

    **Note:**

    -   Once the execution initiated or completed, a work notes is posted on the activity stream of the form view.
    -   The enrichment results pushed from SIR workspace can be found in the **Enrichment Results** tab of that corresponding Observables details page in TISC Workspace.
    -   The enrichment results pushed from SIR workspace can be identified using **Source** field of the enrichment result table.

**Parent Topic:**[Run Enrichment operations in TISC](tisc-unified-experience-capabilities-and-modal-screens.md)

