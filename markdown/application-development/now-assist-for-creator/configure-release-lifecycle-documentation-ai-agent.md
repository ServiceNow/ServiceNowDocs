---
title: Configure release lifecycle documentation AI agent
description: Configure the release lifecycle documentation AI agent to start automating your app governance tasks.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Release lifecycle documentation AI agent, Use agentic AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Configure release lifecycle documentation AI agent

Configure the release lifecycle documentation AI agent to start automating your app governance tasks.

## Before you begin

To configure the release lifecycle documentation AI agent, you must have the Now Assist panel turned on and configured. See [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

Role required: admin

## About this task

By default, the release lifecycle documentation AI agent is inactive. To use the release lifecycle documentation AI agent, you must configure the AI agent in AI Agent Studio. For more information about configuring AI agents, see [Configure Now Assist AI agents](https://www.servicenow.com/docs/access?context=configuring-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Install the Now Assist for Creator application and all plugins.

    For more information, see [Install Now Assist for Creator](../../../administer/flow-designer/task/install-now-assist-for-creator.md).

2.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

3.  Select the **AI Agents** tab.

4.  Select the release lifecycle documentation AI agent card.

    ![AI Agent Studio interface showing the release lifecycle documentation AI agent card highlighted with a blue border.](../image/rldaia-in-ai-agent-studio.png)

5.  Define additional security roles for who can access the AI agent and what data the AI agent has access to.

    By default, using the release lifecycle documentation AI agent requires the update\_set\_admin and sn\_aia.viewer roles. You can add additional role requirements if needed.

    For more information about the roles required, see [Roles required for using the release lifecycle documentation AI agent](../reference/release-lifecycle-documentation-ai-agent-roles.md). For more information about defining AI agent access, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

6.  In the side panel, select **Select channels and status**.

    ![From the side panel, select Select channels and status.](../image/rldaia-select-channels-and-status.png)

7.  Toggle the switch to make the AI agent active.

    ![Toggle the switch to activate the AI agent. The toggle is shown in its inactive state.](../image/rldaia-agent-active-toggle.png)

8.  Select **Test**.

    Testing an AI agent enables you to see that it functions the way that you defined it. To learn more, see [Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).


## What to do next

Start using the release lifecycle documentation AI agent to generate update set descriptions and release notes.

-   [Generate release notes](../task/generate-release-notes.md)
-   [Generate an update set description](../task/generate-update-set-description.md)

-   **[Roles required for using the release lifecycle documentation AI agent](../reference/release-lifecycle-documentation-ai-agent-roles.md)**  
Learn about which roles are required for using the release lifecycle documentation AI agent.

**Parent Topic:**[Release lifecycle documentation AI agent](release-lifecycle-documentation-agent-landing.md)

