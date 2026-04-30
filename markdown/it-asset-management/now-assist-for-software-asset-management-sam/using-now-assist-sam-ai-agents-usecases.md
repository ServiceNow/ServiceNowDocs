---
title: Using agentic workflows in Now Assist for SAM
description: Use the Now Assist for SAM AI agent collection to complete tasks autonomously.
locale: en-US
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2025-02-25"
reading_time_minutes: 3
breadcrumb: [Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Using agentic workflows in Now Assist for SAM

Use the Now Assist for SAM AI agent collection to complete tasks autonomously.

Ensure that you have the following prerequisites for running agentic workflows:

-   Your organization has a software asset management system integrated with AI agents. For more details on AI agents, see [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   Access to an AI-driven Now Assist panel. For more details on Now Asset Panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

<table id="table_hrp_zyl_m2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help manage software request

</td><td>

Fulfill a software asset request by either allocating the available entitlements, if sufficient rights exist, or generating a purchase order with the necessary line items for the requested software model.

</td><td>

-   Software entitlement allocation AI agent
-   Purchase order creation AI agent

</td></tr><tr><td>

Create software reclamation rule

</td><td>

Analyze the license usage of a product and if no reclamation rule exists, prompt the user to create one.

</td><td>

Software reclamation rule creation AI agent

</td></tr><tr><td>

Evaluate software removal candidate

</td><td>

Examine installed or subscription-based removal candidates for a software product by evaluating its software product usage within a specified period and the eligible total number of reclaimable candidates

</td><td>

Software removal candidate evaluation AI agent

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Important:** By default, all agentic workflows and AI agent records are read-only.

You can run the agentic workflow as is by activating the workflow. Additionally, you can [duplicate](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) the workflow if you want to customize the workflow. If you duplicate the agentic workflow, adjust the settings according to your requirements and then activate the duplicated agentic workflow. You can also [test](https://www.servicenow.com/docs/access?context=test-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) the duplicated agentic workflow to analyze its performance in the AI Agent Studio, while it executes the instructions that you defined.

When you activate the agentic workflow, activate all agents within the agentic workflow.

Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

-   **[Now Assist for Software Asset Management \(SAM\) AI agent collection to help manage software asset request agentic workflow](now-assist-sam-fulfill-sw-asset-requests-workflow.md)**  
Use the Help manage software request agentic workflow to fulfill a software request by either allocating the available entitlements or generating a purchase order for the software model.
-   **[Now Assist for Software Asset Management \(SAM\) AI agent collection to create software reclamation rule](now-assist-sam-create-software-reclamation-rule-workflow.md)**  
Use the Create software reclamation rule agentic workflow to automatically create reclamation rules to aggregate usage records and to identify unused software products that lack reclamation rules but are viable candidates.
-   **[Now Assist for Software Asset Management \(SAM\) AI agent collection to evaluate software removal candidate agentic workflow](now-assist-sam-evaluate-removal-candidate-workflow.md)**  
Use the Evaluate software removal candidate agentic workflow to assess installed or subscription-based software for potential removal by analyzing their usage over a specified period and determining the total number eligible for removal. After user confirmation, the workflow initiates the eligible removal candidate for reclamation.

**Parent Topic:**[Now Assist for Software Asset Management \(SAM\)](now-assist-sam.md)

