---
title: Confirm installation of AI Agent Advisor
description: Confirm the installation of the AI Agent Advisor application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-15"
reading_time_minutes: 1
keywords: [AI Agent Advisor, AI agents, Now Assist, Now Assist Center, Gen AI, Generative AI]
breadcrumb: [Configure, AI Agent Advisor, Enable AI experiences]
---

# Confirm installation of AI Agent Advisor

Confirm the installation of the AI Agent Advisor application.

## Before you begin

All required plugins must be installed before attempting to run AI Agent Advisor. For a list of dependencies, see [Supporting information for AI Agent Advisor](../concept/supporting-information-ai-agent-advisor.md).

Role required: AI Agent Advisor admin \[sn\_agent\_miner.app\_admin\]

## About this task

AI Agent Advisor installs and runs automatically as part of the standard Now Assist setup. No manual steps are required. After Now Assist is installed and configured, AI Agent Advisor will be present on your instance and will begin analysis automatically.

Follow these steps to confirm the installation of the AI Agent Advisor plugin.

## Procedure

1.  Confirm the AI Agent Advisor plugin is installed by navigating to **System Definition** &gt; **Plugins** and selecting the **Installed** tab.

2.  If the AI Agent Advisor plugin is not installed, perform the following steps to manually install it.

    1.  Navigate to **System Definition** &gt; **Plugins**.

    2.  In the search box, type `AI Agent Advisor`.

    3.  In the Store applications section under the Available for you tab, select the **AI Agent Advisor** card.

    4.  Select **Install**.

    5.  Select a version from the list.

    6.  Select an installation schedule option.

    7.  Select **Install**.

        The AI Agent Advisor application will install at the selected time.

3.  Navigate to **All** &gt; **Now Assist Center** or **Workspaces** &gt; **Now Assist Center** to confirm the successful installation.

    The Now Assist Center home page opens.

    Confirm the following:

    -   Automation opportunities appear on the Now Assist Center home page.
    -   All AI Agent Advisor dependencies are installed.

        Navigate to **System Definition** &gt; **Plugins** and select the **Installed** tab to confirm all required plugins are installed.

    -   Scheduled jobs are installed.

        Navigate to **System Definition** &gt; **Scheduled Jobs** to confirm that the Agent Miner jobs for incidents, cases, and cluster matching are included in the list.


## Result

The AI Agent Advisor application is installed and available to the appropriate user roles.

**Parent Topic:**[Configuring AI Agent Advisor](../concept/configuring-ai-agent-advisor.md)

**Related topics**  


[Set up automation discovery for AI Agent Advisor](now-assist-center-set-up-automation-discovery.md)

