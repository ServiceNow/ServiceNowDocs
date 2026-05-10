---
title: Create an agent
description: Create an automation request agent to efficiently manage the tasks of the automation request without manual intervention.
locale: en-US
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Create an agent

Create an automation request agent to efficiently manage the tasks of the automation request without manual intervention.

## Before you begin

Role required: sn\_ac.automation\_admin, sn\_ac.automation\_technical\_user

## Procedure

1.  Navigate to **Workspaces** &gt; **Automation Center workspace**.

2.  Select the list icon \(![list icon](../images/list-icon.png)\).

3.  Open an automation request.

    Ensure that you have repeatable steps documented in the **Details Sequence of Steps** section of the form. This ensures that the agent can perform the tasks. If the steps are either missing or not appropriate, then an error message is displayed.

    ![Details Sequence of Steps](../images/agent-detail.png)

4.  Select **Create agent** from the options at the top.

    **Note:** The **Create agent** option is available only if the Now Assist AI Agents skill is installed and the automation request is in **In progress** state.

    The **Choose destination instance** dialog box is displayed.

    ![Choose destination instance](../images/create-agent-1.png)

5.  Choose an instance to create the agent in, and select **Continue**.

    You can select the current instance or any other instance. Ensure that the instance you choose has Automation Center installed.

    To configure an instance, set the connection alias for the **AC Agent Enablement connection** alias. For information on configuring an instance, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md).

    A summary of the agent that is in progress is displayed.

6.  Select **Create agent in AI studio** after reviewing the content.

    For the detailed procedure to create an agent in AI studio, see [Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md).

    The agent is created for the automation request.


**Parent Topic:**[Working with automations](../concept/automations.md)

