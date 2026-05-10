---
title: Using agentic workflows in Now Assist for SAM
description: Use the Now Assist for SAM AI agent collection to complete tasks autonomously.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Using agentic workflows in Now Assist for SAM

Use the Now Assist for SAM AI agent collection to complete tasks autonomously.

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

</td></tr></tbody>
</table>**Important:** By default, all agentic workflows and AI agent records are read only.

You can run the agentic workflow as is by activating the workflow. Additionally, you can [duplicate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md) the workflow if you want to customize the workflow. If you duplicate the agentic workflow, adjust the settings according to your requirements and then activate the duplicated agentic workflow. You can also [test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-aia-use-case.md) the duplicated agentic workflow to analyze its performance in the AI Agent Studio, while it executes the instructions that you defined.

When you activate the agentic workflow, activate all agents within the agentic workflow.

Activate the trigger to invoke the agentic workflow automatically. If you prefer to invoke it manually, activating the trigger isn’t necessary.

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/find-ai-agents.md).

-   **[Now Assist for Software Asset Management \(SAM\) AI agent collection to help manage software asset request agentic workflow](now-assist-sam-fulfill-sw-asset-requests-workflow.md)**  
Use the Help manage software request agentic workflow to fulfill a software request by either allocating the available entitlements or generating a purchase order for the software model.
-   **[Now Assist for Software Asset Management \(SAM\) AI agent collection to evaluate software removal candidate agentic workflow](now-assist-sam-evaluate-removal-candidate-workflow.md)**  
Use the Evaluate software removal candidate agentic workflow to assess installed or subscription-based software for potential removal by analyzing their usage over a specified period and determining the total number eligible for removal. After user confirmation, the workflow proceeds to reclaim the eligible software, effectively removing them.
-   **[now-assist-sam-create-software-reclamation-rule-workflow.md](now-assist-sam-create-software-reclamation-rule-workflow.md)**  


**Parent Topic:**[Now Assist for Software Asset Management \(SAM\)](now-assist-sam.md)

