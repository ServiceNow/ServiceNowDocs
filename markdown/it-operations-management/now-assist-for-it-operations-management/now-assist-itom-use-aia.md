---
title: Use the analyze alert impact agentic workflow
description: Learn how to use the analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.
locale: en-US
release: yokohama
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Analyze alert impact agentic workflow, Using agentic workflows in Now Assist for ITOM, Now Assist for ITOM, IT Operations Management]
---

# Use the analyze alert impact agentic workflow

Learn how to use the analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.

## Before you begin

Before using the analyze alert impact agentic workflow, you must have the following:

-   Now Assist for IT Operations Management \(ITOM\) installed on your instance. See [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   The analyze alert impact agentic workflow turned on in the Now Assist panel. See [Analyze alert impact agentic workflow](../concept/now-assist-itom-agentic-aia.md).
-   AI agents configured and activated for the observability tools integrated with Event Management, such as Dynatrace, Kentik, or New Relic. See [Configuring agents and skills for Now Assist for ITOM](../concept/itom-ai-agent-configuration.md).

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an agentic workflow](https://www.servicenow.com/docs/access?context=define-sec-controls-aw&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \(![Express list icon](../../event-management/image/express-list1.png)\).

3.  Select an alert, making sure that the source is Dynatrace, Kentik, or New Relic.

4.  Open the panel by selecting the Now Assist icon \(![Now Assist icon.](../../../administer/now-assist-platform/images/wwna-icon.png)\).

5.  Ask a tool-specific question about the alert.

    For example, for New Relic alerts, you can ask `Have there been recent deployments for this alert?`. See [Questions for the analyze alert impact agentic workflow](../reference/questions-now-assist-workflows.md) for the list of available questions.

    Now Assist uses the relevant AI agents to analyze your question and respond with a summary or insight. The first response for an alert might take several seconds to appear.


## What to do next

Use the information that you received to understand the alert impact and respond accordingly. You can also ask more questions about the alert.

**Note:** Your conversation in the Now Assist panel is specific to the alert that you selected in Step 3. To ask about a different alert, open that alert and select the Now Assist icon \(![Now Assist icon.](../../../administer/now-assist-platform/images/wwna-icon.png)\) to start a new conversation.

**Parent Topic:**[Analyze alert impact agentic workflow](../concept/now-assist-itom-agentic-aia.md)

