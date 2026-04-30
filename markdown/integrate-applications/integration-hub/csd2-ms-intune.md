---
title: CSD 2.0 for Microsoft Intune
description: Use the CSD 2.0 along with the Microsoft Intune spoke to deploy and revoke software deployments, and manage distributions on hosts.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 5
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# CSD 2.0 for Microsoft Intune

Use the CSD 2.0 along with the Microsoft Intune spoke to deploy and revoke software deployments, and manage distributions on hosts.

To use the Microsoft Intune spoke with CSD 2.0, you must activate Microsoft Intune spoke and CSD 2.0.

The Microsoft Intune spoke contains actions that CSD 2.0 uses to deploy software from a service catalog request and manage user and devices on Microsoft Intune servers. In addition, CSD 2.0 can manage license counts for deployed software using ServiceNow Software Asset Management, revoke software deployed by Microsoft Intune without user interaction, and manage lease periods.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This application provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance. The agents guide you through the required details, confirms actions for safety, and attempts to handle errors while performing operations.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Microsoft Intune application assignment deletion AI agent|Enables users to delete application assignments in Intune.|
|Microsoft Intune group deletion management AI agent|Enables users to delete groups in Microsoft Intune.|
|Microsoft Intune application assignment creation AI agent|Enables users to create application assignments in Intune.|
|Microsoft Intune group membership removal AI agent|Enables users to remove members \(Devices, Users, or Owners\) from groups in Microsoft Intune.|
|Microsoft Intune group membership addition AI agent|Enables users to add members \(devices, users, and owners\) to groups in Intune.|
|Microsoft Intune group creation management AI agent|Enables users to create groups in Microsoft Intune.|

**Note:**

-   To access data or perform operations on data in the table that is associated with the AI agent, users must have the CSD Admin role.
-   Ensure that you install the latest version of Microsoft Intune spoke.
-   To use the AI agents, ensure that you are using the default connection that is available with the Microsoft Intune spoke.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Available sample agentic workflow includes:

<table id="table_hys_nsy_c3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Microsoft Intune Group Management Agentic Flow

</td><td>

Sample agentic workflow that coordinates between multiple AI agents to handle tasks that span across various functionalities in Microsoft Intune.

</td><td>

-   Microsoft Intune application assignment creation AI agent
-   Microsoft Intune application assignment deletion AI agent
-   Microsoft Intune group membership addition AI agent
-   Microsoft Intune group creation management AI agent
-   Microsoft Intune group membership removal AI agent
-   Microsoft Intune group deletion management AI agent

</td><td>

No**Note:** To activate the workflow, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>-   **[Configure group assignments](../task/csd2-intune-app.md)**  
Configure group assignments for all the applications you want to deploy.
-   **[Verify the Microsoft Intune spoke records](../task/csd2-intune.md)**  
Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Microsoft Intune spoke and create server instance record to use Microsoft Intune spoke with CSD 2.0.
-   **[Store details of the Microsoft Intune server](../task/csd2-intune-discapps.md)**  
Create a server instance record to discover applications and store details of the Microsoft Intune server.
-   **[Set up a software model](../task/csd2-intune-sw.md)**  
Using the applications discovered on the Microsoft Intune server, set up a software model to manage licenses.
-   **[Define the Microsoft Intune configuration](../task/csd2-intune-coll.md)**  
Associate that software with a group through a Microsoft Intune configuration to create catalog items for Microsoft Intune software deployment or to configure your instance to revoke software through Microsoft Intune.
-   **[Create a catalog item for the Microsoft Intune applications](../task/csd2-intune-create-cat.md)**  
Create a catalog item for an application you want to offer for distribution from the service catalog using the applications discovered on the Microsoft Intune server.
-   **[Deployment process](../task/csd2-intune-deploy.md)**  
Order an application from a CSD 2.0 catalog item in the service catalog triggers the Order Client Software flow.

**Parent Topic:**[Client Software Distribution 2.0 application](csd-app-2.md)

