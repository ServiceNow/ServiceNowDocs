---
title: Set up Now Assist AI agents
description: The default \(out-of-the-box\) AI agents provide preconfigured agentic workflows that address common business challenges across ServiceNow applications. Before activating the default AI agents, you must ensure that your instance meets the prerequisites and complete the required configuration steps.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-02-06"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist AI agents, Enable AI experiences]
---

# Set up Now Assist AI agents

The default \(out-of-the-box\) AI agents provide preconfigured agentic workflows that address common business challenges across ServiceNow applications. Before activating the default AI agents, you must ensure that your instance meets the prerequisites and complete the required configuration steps.

## Before you begin

Role required: sn\_aia\_admin

## About this task

**Prerequisites**

-   **Platform version:**
    -   Minimum: Yokohama Patch 1+ or Xanadu Patch 7+
    -   Recommended: Yokohama Patch 8 or Zurich Patch 4
-   **Required plugins and store Apps**

    -   Now Assist AI agents store app \(version 6.0.17 or later as of December 2025\)
    -   At least one Now Assist workflow plugin:
        -   Now Assist for ITSM
        -   Now Assist for HRSD
        -   Now Assist for CSM
        -   Now Assist for Security Operations
    -   Generative AI Controller plugin \(minimum version 11.0.0\)
    **Note:** Select **Load demo data** during installation to access preconfigured examples.

-   **Licensing Requirements**

    Now Assist Pro Plus or Enterprise entitlement

-   **Required User Roles**
    -   sn\_aia.admin - Provides access to AI Agent Studio
    -   sn\_nowassist\_admin.nsa\_admin - Enables Now Assist administration

## Procedure

1.  Enable AI Search.

    1.  Navigate to **AI Search** &gt; **AI Search Status**.
    2.  Verify that AI Search is enabled.
2.  Enable Now Assist panel.

    1.  Navigate to **Now Assist Admin** &gt; **Experiences**.
    2.  Turn on the **Panel** option.
3.  Access the AI Agent Studio.

    1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
    2.  Review the available default \(out-of-the-box\) agentic workflows.
4.  Activate the default agentic workflows.

    1.  Select the agentic workflow that you want to use from the available default workflows.
    2.  Activate the workflow. The default workflows are set to read only and must be activated before use.
    The default \(OOTB\) agentic workflows include:

    -   Generate resolution plans
    -   Analyze incident trends
    -   Classify tasks
    -   Investigate IT problems
    -   Process emails for tasks
5.  Configure chat assistants.

    1.  Navigate to **Conversational Interfaces** &gt; **Assistants**.
    2.  Determine which chat assistants can access your AI agents.
    3.  Complete the configuration wizards for Now Assist panel \(NAP\) or Now Assist Virtual Agent \(NAVA\).
6.  Configure LLM Connections \(optional\).

    If using external LLM providers instead of the default OpenAI GPT-4.1:

    1.  Navigate to **Now Assist Admin Console** &gt; **Settings** &gt; **Manage Integration**.
    2.  Configure API credentials for your chosen LLM provider.
    **Note:** The default Orchestration layer uses OpenAI GPT-4.1 on ServiceNow-managed Azure servers.

7.  Test the default AI agents.

    1.  Navigate to **AI Agent Studio** &gt; **Testing** &gt; **Test AI reasoning**.
    2.  Verify that the orchestrator canvas displays agent execution properly.
    3.  Review AI agent decision logs to confirm interactions and thought processes are recorded.

