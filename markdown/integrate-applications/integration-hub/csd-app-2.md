---
title: Client Software Distribution 2.0 application
description: Client Software Distribution 2.0 application \(CSD 2.0\) application enables administrators to distribute software from the service catalog using third-party management systems.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-01-29"
reading_time_minutes: 8
breadcrumb: [Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Client Software Distribution 2.0 application

Client Software Distribution 2.0 application \(CSD 2.0\) application enables administrators to distribute software from the service catalog using third-party management systems.

CSD 2.0 enables an administrator to create all the records necessary to deploy software from service catalog requests, including software models and catalog items. You can use the CSD 2.0 application to automate the deployment and revocation of software from a third-party software provider using the custom flows. You can define lease periods for software distributed from the Service Catalog and allow lease extensions in some cases, pending approvals. Deployment is accomplished using provider-specific spoke flows, subflows, and actions. For example, deployment is accomplished using Microsoft Endpoint Configuration Manager spoke.

CSD 2.0 also integrates with Software Asset Management \(SAM Professional or SAM Foundation\) to manage license information of the deployed software.

**Note:** CSD 2.0 is different from [Client Software Distribution using Integration Hub](../../integrationhub/concept/csd-integrationhub.md). CSD 2.0 is available on ServiceNow Store.

![CSD 2.0 process flow](../image/CSDProcess.png "CSD 2.0 process flow when CSD is integrated with SAM")

**Note:** To integrate CSD 2.0 with SAM, navigate to **Client Software Distribution 2.0** &gt; **Properties** and select the check box for **Determines whether to use SAM plugin\(SAM Foundation or SAM Professional\) tables for managing software models and licensing information**.![Option to integrated with SAM.](../image/CSD2-props.png)

## Important considerations

Ensure that you are aware of these differences between CSD and CSD 2.0:

<table id="table_dd5_mdr_w5b"><thead><tr><th>

 

</th><th>

CSD

</th><th>

CSD 2.0

</th></tr></thead><tbody><tr><td>

Supported providers

</td><td>

Microsoft System Center Configuration Management \(SCCM\).

</td><td>

Microsoft Endpoint Configuration Manager, Jamf, and Microsoft Intune.

</td></tr><tr><td>

Procedure to add new provider

</td><td>

User must write extension point scripts.

</td><td>

User can use subflows in Workflow Studio. This is easier than writing extension point scripts in CSD.

</td></tr><tr><td>

License compliance check and entitlements

</td><td>

Tightly coupled with the SAM license data.

</td><td>

Flexibility to choose either the SAM tables or CSD 2.0 tables.

</td></tr><tr><td>

Data discovery

</td><td>

Microsoft SCCM provider uses PowerShell cmdlets for data discovery.

</td><td>

Microsoft Endpoint Configuration Manager spoke is updated to use the REST protocol for data discovery. This improves the performance and reduces load on MID Server as REST supports pagination.

</td></tr><tr><td>

Software revocation

</td><td>

CSD can revoke software requested using the CSD catalog. CSD can also uninstall software using SCCM when revocation is triggered from the reclamation candidates for SCCM provider.

</td><td>

CSD 2.0 can revoke software requested using the CSD 2.0 catalog. CSD 2.0 can also uninstall software using Microsoft Endpoint Configuration Manager, Microsoft Intune, and Jamf when revocation is triggered from the reclamation candidates.

</td></tr></tbody>
</table>## Application version

CSD 2.0 v1.5.0 is the latest version.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This application provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

<table id="table_ejq_jpy_c3c"><thead><tr><th>

AI agent

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog item creation AI agent

</td><td>

Automates the creation of catalog items for applications provided by service providers like Microsoft Intune and Jamf. The agent also manages software models, configurations, group associations, and catalog item generation.**Note:** This version of CSD 2.0 supports Microsoft Intune and Jamf providers only.

</td></tr><tr><td>

Microsoft Endpoint Configuration Manager collection creation management AI agent

</td><td>

Creates collections in Microsoft Endpoint Configuration Manager. The agent prompts for required collection details, validates inputs, and requests confirmation before creating the collection. The agent also handles common errors and reports the outcome of the operation.

</td></tr><tr><td>

Microsoft Endpoint Configuration Manager collection deletion management AI agent

</td><td>

Deletes collections in Microsoft Endpoint Configuration Manager. The agent collects the required inputs, checks for dependencies, and requests confirmation before deletion. The agent also attempts to resolve dependencies automatically and reports the result.

</td></tr><tr><td>

Microsoft Endpoint Configuration Manager collection membership addition AI agent

</td><td>

Adds collections as deployment targets for applications in Microsoft Endpoint Configuration Manager. The agent gathers the required information, confirms the action, and handles errors that occur during the operation.

</td></tr><tr><td>

Microsoft Endpoint Configuration Manager collection membership removal AI agent

</td><td>

Removes device or user members from collections in Microsoft Endpoint Configuration Manager. The agent guides users through the required inputs, confirms the action before execution, and handles errors during the process.

</td></tr><tr><td>

Microsoft Endpoint Configuration Manager application targets addition AI agent

</td><td>

Adds device or user targets to collections in Microsoft Endpoint Configuration Manager. The agent prompts for the required details, validates inputs, requests confirmation, and reports the result of the operation.

</td></tr><tr><td>

Microsoft Endpoint Configuration Manager application targets removal AI agent

</td><td>

Removes collections as targets from applications in Microsoft Endpoint Configuration Manager. The agent gathers the required inputs, confirms the action, and handles errors while performing the removal.

</td></tr></tbody>
</table>Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** To access data or perform operations on data in the table that is associated with the AI agent, users must have the CSD Admin role.

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

<table id="table_ikz_kqv_v3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Microsoft Endpoint Configuration Manager Collection Management Agentic Flow

</td><td>

Manages Microsoft Endpoint Configuration Manager device and user collections and their application assignments. This agentic workflow interprets user requests, separates them into discrete collection and deployment tasks, and coordinates the required operations to create or delete collections, manage membership, and assign or remove application targets in a controlled, sequential manner.

</td><td>

-   Microsoft Endpoint Configuration Manager collection deletion management AI agent
-   Microsoft Endpoint Configuration Manager application targets removal AI agent
-   Microsoft Endpoint Configuration Manager collection membership addition AI agent
-   Microsoft Endpoint Configuration Manager collection creation management AI agent
-   Microsoft Endpoint Configuration Manager application targets addition AI agent
-   Microsoft Endpoint Configuration Manager collection membership removal AI agent

</td><td>

No**Note:** To activate the workflow, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>-   **[Request the CSD 2.0 application](../task/req-csd.md)**  
Client Software Distribution 2.0 application plugin \(com.sn.csd\) is available on ServiceNow Store and can be used with a subscription to Integration Hub.
-   **[Components installed with CSD 2.0](../reference/csd2-installed.md#)**  
Several types of components are installed with the CSD 2.0 application.
-   **[Create licenses for distributed software using CSD 2.0](../task/csd2-license-ntsam.md)**  
Licenses are associated with the software model and must be created if you want to track the license for software deployed by CSD 2.0.
-   **[Create entitlements for distributed software using SAM](../task/csd2-license.md)**  
Entitlements are associated with the software model and must be created if you want to track the license for software deployed by CSD 2.0 using SAM.
-   **[Client software distribution ordering process](../reference/csd2-orderprocess.md)**  
Software deployed by CSD 2.0 can be ordered from the service catalog by individual users or by approved users on behalf of others.
-   **[Extend a software lease](../task/csd2-extend.md)**  
Users of software deployed by CSD 2.0 can request the extension of a lease window, if the software is revocable by a software distribution system.
-   **[CSD 2.0 for Microsoft Endpoint Configuration Manager](csd2.md)**  
Use the CSD 2.0 along with the Microsoft Endpoint Configuration Manager spoke to deploy and revoke software deployments from Microsoft Endpoint Configuration Manager and manage distributions on hosts.
-   **[CSD 2.0 for Jamf](csd2-jamf-tsk.md)**  
Use the CSD 2.0 along with the Jamf spoke to deploy and revoke software deployments from Jamf and manage distributions on hosts.
-   **[CSD 2.0 for Microsoft Intune](csd2-ms-intune.md)**  
Use the CSD 2.0 along with the Microsoft Intune spoke to deploy and revoke software deployments, and manage distributions on hosts.
-   **[CSD 2.0 validation process](csd2-validation.md)**  
After Microsoft Endpoint Configuration Manager deploys software to a target computer, CSD 2.0 detects the installation and validates its status.
-   **[Software revocation](csd2-revocation.md#)**  
Revoke software without any user interaction if the software can be revoked and has a lease end date using the provider-specific revocation flow.
-   **[Integrate CSD 2.0 with other software providers](csd2-integrate.md#)**  
Integrate CSD 2.0 with client software distribution providers, such as Casper, Altiris, or LANDesk.

**Parent Topic:**[Building integrations in Integration Hub](../../integrationhub/concept/building-integrations-ih.md)

