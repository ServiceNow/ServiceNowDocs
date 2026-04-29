---
title: Run Sighting Search
description: Perform Run Sighting Search related integration.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Run Enrichment operations in TISC, Observables, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Run Sighting Search

Perform Run Sighting Search related integration.

## Before you begin

Role required: sn\_sec\_tisc.admin

To perform this action select the implementation and add common run time inputs that apply for all the selected implementations as applicable.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Observables** &gt; **All Observables**.

4.  Open any observable record.

5.  Click **Run Sighting Search**.

    The Run Sighting Search **Select Implementations** modal screen is displayed.

    **Note:** The Run Sighting Search performs the threat intelligence lookups to determine whether the observables are associated with any known threats.

6.  Select the required implementation\(s\) from the list.

    ![Run Sighting Search](../image/tisc-run-sighting-search-modal01.png)

7.  Click **Next**.

8.  Select the common run time input value such as Select Date/Time frequency and Number of hours.

    ![Run Sighting Search - Common inputs](../image/tisc-run-sighting-search-modal02.png)

9.  Click **Submit**.

    The selected enrichment action will be executed and an information message is displayed that Run Sighting Search execution has started.

    **Note:**

    -   Once the execution initiated or completed, a work notes is posted on the activity stream of the form view.
    -   The enrichment results pushed from SIR workspace can be found in the **Enrichment Results** tab of that corresponding Observables details page in TISC Workspace.
    -   The enrichment results pushed from SIR workspace can be identified using **Source** field of the enrichment result table.

**Parent Topic:**[Run Enrichment operations in TISC](tisc-unified-experience-capabilities-and-modal-screens.md)

