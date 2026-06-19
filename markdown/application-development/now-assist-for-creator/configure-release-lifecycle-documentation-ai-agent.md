---
title: Configure release lifecycle documentation AI agent
description: Configure the release lifecycle documentation AI agent to start automating your app governance tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/now-assist-for-creator/configure-release-lifecycle-documentation-ai-agent.html
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Release lifecycle documentation AI agent, Use agentic AI, Now Assist for Creator, Agentic development on the ServiceNow AI Platform, Building applications]
---

# Configure release lifecycle documentation AI agent

Configure the release lifecycle documentation AI agent to start automating your app governance tasks.

## Before you begin

To configure the release lifecycle documentation AI agent, you must have the Now Assist panel turned on and configured. See  for more information.

Role required: admin

## About this task

By default, the release lifecycle documentation AI agent is inactive. To use the release lifecycle documentation AI agent, you must configure the AI agent in AI Agent Studio. For more information about configuring AI agents, see .

## Procedure

1.  Install the Now Assist for Creator application and all plugins.

    For more information, see [Install Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/install-now-assist-for-creator.md).

2.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

3.  Select the **AI Agents** tab.

4.  Select the release lifecycle documentation AI agent card.

    \[Omitted image "rldaia-in-ai-agent-studio.png"\] Alt text: AI Agent Studio interface showing the release lifecycle documentation AI agent card highlighted with a blue border.

5.  Define additional security roles for who can access the AI agent and what data the AI agent has access to.

    By default, using the release lifecycle documentation AI agent requires the update\_set\_admin and sn\_aia.viewer roles. You can add additional role requirements if needed.

    For more information about the roles required, see [Roles required for using the release lifecycle documentation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/release-lifecycle-documentation-ai-agent-roles.md). For more information about defining AI agent access, see .

6.  In the side panel, select **Select channels and status**.

    \[Omitted image "rldaia-select-channels-and-status.png"\] Alt text: From the side panel, select Select channels and status.

7.  Toggle the switch to make the AI agent active.

    \[Omitted image "rldaia-agent-active-toggle.png"\] Alt text: Toggle the switch to activate the AI agent. The toggle is shown in its inactive state.

8.  Select **Test**.

    Testing an AI agent enables you to see that it functions the way that you defined it. To learn more, see .


## What to do next

Start using the release lifecycle documentation AI agent to generate update set descriptions and release notes.

-   [Generate release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-release-notes.md)
-   [Generate an update set description](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/generate-update-set-description.md)

-   **[Roles required for using the release lifecycle documentation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/release-lifecycle-documentation-ai-agent-roles.md)**  
Learn about which roles are required for using the release lifecycle documentation AI agent.

**Parent Topic:**[Release lifecycle documentation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator/release-lifecycle-documentation-agent-landing.md)

