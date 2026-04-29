---
title: Run Observable Enrichment
description: Select one or more implementations as applicable to run threat lookup on observables.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Run Enrichment operations in TISC, Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Run Observable Enrichment

Select one or more implementations as applicable to run threat lookup on observables.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Observables** &gt; **All Observables**.

4.  Open any observable record.

5.  Click **Run Observable Enrichment**.

    The Run Observable Enrichment **Select Implementations** modal screen is displayed.

    **Note:** Only supported records will be submitted against the selected implementation\(s\)

6.  Select the required implementation\(s\) \(for example, WHOIS\) from the list.

    ![Run Observable Enrichment](../image/tisc-run-observable-enrichment.png)

7.  Click **Submit**.

    The selected enrichment action will be executed and an information message is displayed that Threat lookup execution has started.

    **Note:**

    -   Once the execution initiated or completed, a work notes is posted on the activity stream of the form view.
    -   The enrichment results pushed from SIR workspace can be found in the **Enrichment Results** tab of that corresponding Observables details page in TISC Workspace.
    -   The enrichment results pushed from SIR workspace can be identified using **Source** field of the enrichment result table.

**Parent Topic:**[Run Enrichment operations in TISC](tisc-unified-experience-capabilities-and-modal-screens.md)

