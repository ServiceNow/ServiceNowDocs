---
title: CSD 2.0 for Jamf
description: Use the CSD 2.0 along with the Jamf spoke to deploy and revoke software deployments from Jamf and manage distributions on hosts.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# CSD 2.0 for Jamf

Use the CSD 2.0 along with the Jamf spoke to deploy and revoke software deployments from Jamf and manage distributions on hosts.

To use the Jamf spoke with CSD 2.0, you must activate Jamf spoke and CSD 2.0.

The Jamf spoke contains actions that CSD 2.0 uses to deploy software from a service catalog request and manage user and device collections on Jamf servers. In addition, CSD 2.0 can manage license counts for deployed software using ServiceNow Software Asset Management, revoke software deployed by Jamf without user interaction, and manage lease periods.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This application provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance. The agents guide you through the required details, confirms actions for safety, and attempts to handle errors while performing operations.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-use-case-ai-agents.md) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md) for more information about creating a clone.
-   See [Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-agents.md) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Jamf group membership addition AI agent|Enables users to add members to static groups in Jamf.|
|Jamf group deletion management AI agent|Enables users to delete groups in Jamf.|
|Jamf application targets addition AI agent|Enables users to add static groups as targets to applications in Jamf.|
|Jamf application targets removal AI agent|Enables users to remove static groups as targets from applications in Jamf.|
|Jamf group creation management AI agent|Enables users easily and deterministically create groups in Jamf.|
|Jamf group membership removal AI agent|Enables users to remove members from static groups in Jamf.|

**Note:**

-   To access data or perform operations on data in the table that is associated with the AI agent, users must have the CSD Admin role.
-   Ensure that you install the latest version of Jamf spoke.
-   To use the AI agents, ensure that you are using the default connection that is available with the Jamf spoke.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see [Modify an agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/modify-aia-use-case.md).

Available sample agentic workflow includes:

<table id="table_chb_l90v_c3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Jamf Group Management Agentic Flow

</td><td>

Sample agentic workflow that coordinates between multiple AI agents to handle tasks across various functionalities in Jamf.

</td><td>

-   Jamf group creation management AI agent
-   Jamf group membership removal AI agent
-   Jamf application targets removal AI agent
-   Jamf application targets addition AI agent
-   Jamf group membership addition AI agent
-   Jamf group deletion management AI agent

</td><td>

No**Note:** To activate the workflow, see [Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md).

</td></tr></tbody>
</table>-   **[Verify the Jamf spoke records](../task/csd2-jamf.md)**  
Verify that the spoke is integrated with CSD 2.0 after setting up and configuring the Jamf spoke and create server instance record to use Jamf spoke with CSD 2.0.
-   **[Store details of the Jamf server](../task/csd2-discapps-jamf.md)**  
Create a server instance record to discover applications and store details of the Jamf server.
-   **[Set up a software model](../task/csd2-jamf-sw.md)**  
Using the applications discovered on the Jamf server, set up a software model to manage licenses.
-   **[Define the Jamf configuration](../task/csd2-jamf-coll.md)**  
Associate that software with a group through a Jamf configuration to create catalog items for Jamf software deployment or to configure your instance to revoke software through .
-   **[Create a catalog item for the Jamf application](../task/csd2-create-cat-jamf.md)**  
Create a catalog item for an application you want to offer for distribution from the service catalog using the applications discovered on the Jamf server.
-   **[Deployment process](../task/csd2-jamf-deploy.md)**  
Order an application from a CSD 2.0 catalog item in the service catalog triggers the Order Client Software flow.

**Parent Topic:**[Client Software Distribution 2.0 application](csd-app-2.md)

