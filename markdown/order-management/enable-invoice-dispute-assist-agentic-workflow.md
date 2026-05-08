---
title: Make the invoice dispute assist workflow available in the Now Assist panel
description: Configure the invoice dispute assist agentic workflow in AI Agent Studio to make it available to agents in the Now Assist panel in the CSM/FSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Now Assist for Order Management]
---

# Make the invoice dispute assist workflow available in the Now Assist panel

Configure the invoice dispute assist agentic workflow in AI Agent Studio to make it available to agents in the Now Assist panel in the CSM/FSM Configurable Workspace.

## Before you begin

The application scope must be set to Manage Invoice Operations. You can change the application scope using the application picker ![](../../../reuse/icons/product-icons/globe-outline-24.svg) in the Unified Navigation bar.

Role required: sn\_aia.admin

## About this task

Agentic workflows that are installed with Now Assist applications aren’t automatically activated. You must activate the invoice dispute assist agentic workflow before it can be used in the Now Assist panel. After you enable the workflow, you can optionally promote it to make it appear as a suggested topic in the Now Assist panel for faster access.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  On the Manage agentic workflows and AI agents page, select the **Agentic workflows** tab.

3.  Select the **Invoice Dispute Assist** agentic workflow.

4.  From the navigation pane, select **Select channels and status**.

    You could leave the settings in the remaining tabs at their default values.

5.  On the Select channels and status page, enable the **Engage via Now Assist panel** option.

6.  Select **Save and test**.

7.  Promote the agentic workflow to add it to the list of suggested topics in the Now Assist panel.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    2.  On the Assistant Designer page, select the **Agentic workflows** tab.

    3.  Narrow your search by selecting **Now Assist Panel - Platform \(default\)** from the **Select assistant** drop-down menu.

    4.  Locate the Invoice Dispute Assist agentic workflow and select **Promoted** from the More actions icon ![](../../../reuse/icons/product-icons/ellipsis-vertical-outline-24.svg).

    The invoice dispute assist agentic workflow appears as a promoted topic in the Now Assist panel, making it directly accessible to agents without requiring a search.


**Parent Topic:**[Configuring Now Assist for Order Management](../concept/now-assist-for-order-management-configuring.md)

**Related topics**  


[bundle-platai.activate-aia-use-case]

