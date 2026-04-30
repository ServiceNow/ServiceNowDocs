---
title: Suggested steps generation in Now Assist for Customer Service Management \(CSM\)
description: Generate suggested steps automatically by analyzing clusters of closed cases with similar case resolution in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI skills, Now Assist for CSM, Customer Service Management]
---

# Suggested steps generation in Now Assist for Customer Service Management \(CSM\)

Generate suggested steps automatically by analyzing clusters of closed cases with similar case resolution in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent and sn\_customerservice.consumer\_agent

## About this task

The system uses data from the **Short description** field and the filter conditions set in the case input table to generate the suggested actions based on similar past resolved cases. These steps outline the next best actions that agents can take as part of resolving cases.

If suggested steps are available for a case, Now Assist for CSM generates and displays these steps in a card at the top of the Recommended Actions tab in the contextual side panel.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Using the List icon ![icon for seeing the list of cases](../../../common/image/List_MenuIcon.png), open a case that is not in **Closed** or **Complete** state.

3.  Select the Recommendations icon in the contextual side panel to display the Recommended Actions tab.

    The system displays the **Suggested steps by Now Assist** card at the top of the tab.

4.  In the **Suggested steps by Now Assist** card, select **Generate**.

    The steps to resolve the case appears in the **Recommendations** window in the case record. This action may take a few minutes.

    ![Suggested steps by Now Assist to resolve the issue](../image/suggested-steps.png "Suggested steps by Now Assist")

    **Note:**

    Suggested Steps show an AI gradient styling across:

    -   The sidebar
    -   The Suggested Steps component
    -   The Sparkle icon
    -   The Generate button
    These visual updates help users clearly identify AI‑generated experiences, creating a more consistent and intuitive interface.


**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](../concept/now-assist-csm-using.md)

