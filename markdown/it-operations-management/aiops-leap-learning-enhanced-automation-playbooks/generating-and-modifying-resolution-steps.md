---
title: Generate and modify resolution steps in AIOps LEAP
description: Learn how to generate, edit, and track AI-generated resolution steps for automation opportunities in AIOps LEAP.
locale: en-US
release: yokohama
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Using AIOps LEAP, AIOps Learning Enhanced Automation Playbook \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Generate and modify resolution steps in AIOps LEAP

Learn how to generate, edit, and track AI-generated resolution steps for automation opportunities in AIOps LEAP.

## About this task

Resolution steps are actions designed to resolve issues identified by an automation opportunity. During the initial run, GAF generate these steps by analyzing work notes and historical resolutions.

The **Generate resolution steps** button creates resolution steps as required. As your system processes new incidents and records, regenerate these steps to maintain solution accuracy. AIOps LEAP provides three search capabilities: AI search, KB search, and web search.

-   AI search: Scans records within your existing instance to identify relevant resolutions.
-   KB search: Searches knowledge base resources external to your organization to suggest more effective resolution steps.
-   Web search: Queries web resources beyond your organization's systems to find comprehensive solutions, broadening the scope of potential resolutions.

**Note:**

-   Regenerating resolution steps with web search enabled incurs chargeable transactions. Exercise caution and careful planning before using the regenerate button to avoid unexpected costs.
-   Only a system administrator or a LEAP admin with system administrator access can enable these additional sources of searches. Users with agent or viewer access will need to contact their administrator to activate these features. Once enabled, LEAP expands its search capabilities to deliver more comprehensive and effective resolution steps.

## Before you begin

Role required: System admin

## Procedure

1.  Select **Workspaces** &gt; **AIOps LEAP**.

2.  On the AIOps LEAP landing page, select the required automation opportunity.

3.  If resolution steps are unavailable in the Overview section, select **Generate resolution steps**.

4.  If resolution steps are available, and you want to get alternate resolution steps, then use the **Regenerate** button.![Regenerate resolution steps](../images/regenerate-resolution-steps.png)

    **Note:**

    -   The Regenerate button is disabled while manual editing is in progress.
    -   Resolution steps are generated based on the capability enabled either using AI search or Knowledge Base or Web search.
5.  To manually modify resolution steps, select the edit icon.

    Each update to the resolution steps is recorded in the LEAP Outcome Snapshots table for traceability.

6.  To revert to the last generated resolution steps, use the **Revert to AI generated steps** button.


## Result

Resolution steps are generated, tracked, and can be reverted or edited as needed for improved automation accuracy.

