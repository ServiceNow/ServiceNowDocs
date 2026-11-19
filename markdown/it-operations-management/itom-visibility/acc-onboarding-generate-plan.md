---
title: Generate an Agent Client Collector installation plan
description: Configure and deploy new agents in your environment, using the Agent Onboarding guide. The Agent Onboarding guide generates a customized installation plan for deploying the Agent Client Collector on your endpoints or servers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/itom-visibility/acc-onboarding-generate-plan.html
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 2
keywords: [agent onboarding, installation plan, agent configuration]
breadcrumb: [Use the Agent Client Collector \(ACC\) admin workspace, Use ITOM Infra Services Workspace, ITOM Infra Services Workspace, ITOM Visibility, IT Operations Management]
---

# Generate an Agent Client Collector installation plan

Configure and deploy new agents in your environment, using the Agent Onboarding guide. The Agent Onboarding guide generates a customized installation plan for deploying the Agent Client Collector on your endpoints or servers.

## Before you begin

Ensure that you have installed Agent Client Collector admin workspace version 1.1.0.

Role required: agent\_client\_collector\_admin

## About this task

The Agent Onboarding guide generates a customized installation plan based on your deployment type, operating system, and use case. The plan includes the commands and configuration steps required to install the Agent Client Collector on your endpoints or servers.

## Procedure

1.  Navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select the **ACC agents** icon \[Omitted image "acc-agents-icon.png"\] Alt text: ACC agents icon.

3.  Select the **Agent onboarding** tab.

    Page 1 of the Agent Onboarding guide opens.

    \[Omitted image "agent-onboarding-step1.png"\] Alt text: Agent onboarding wizard - Page 1

4.  Configure the fields on the page.

    |Field|Description|
    |-----|-----------|
    |I'm installing ACC &lt;version number&gt; on|Place where you're installing your agent, either endpoints or servers.|
    |that is running|Platform on which the agents are running.|
    |to collect data for|Component for which the agent is collecting data.|

5.  Select **Next: Configuration**.

    Page 2 of the Agent Onboarding guide opens, displaying default configuration settings for the component for which you're collecting data.

6.  Activate the toggle switch for a setting to enable customizing the value.

    For details on the available settings, see [Agent onboarding configuration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-onboarding-config-settings.md).

7.  Select the **Next: Installation plan** button to view the agent installation plan, based on your configured settings.

    For details on the displayed agent installation plan steps and the commands required to be carried out for each, see [Agent installation plan steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/agent-installation-plan-steps.md).

    The settings configured for your agent appear in the Agent configuration panel.

    \[Omitted image "agent-configuration-tab.png"\] Alt text: Agent configuration panel

8.  Select **Export plan** to download and print the installation plan.


## Result

The installation plan is generated and ready to use. Each step in the plan includes the commands or configuration actions required to deploy the Agent Client Collector on your endpoints or servers.

## What to do next

After completing the installation plan steps, verify that the agent is running and connected to the ServiceNow instance, on the ACC agents page.

**Parent Topic:**[Use the Agent Client Collector \(ACC\) admin workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/use-acc-admin-workspace.md)

