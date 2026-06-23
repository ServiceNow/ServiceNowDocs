---
title: Using agentic workflows in Now Assist for ITSM
description: Use the IT Service Management AI agent collection to complete tasks autonomously.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-ai-agents-use-cases.html
release: xanadu
product: Now Assist for IT Service Management \(ITSM\)
classification: now-assist-for-it-service-management-itsm
topic_type: concept
last_updated: "2025-02-07"
reading_time_minutes: 4
keywords: [Now Assist, Agentic AI]
breadcrumb: [Now Assist for IT Service Management \(ITSM\), IT Service Management]
---

# Using agentic workflows in Now Assist for ITSM

Use the IT Service Management AI agent collection to complete tasks autonomously.

<table id="table_lxk_lck_h2c"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

[Triage and categorize ITSM incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-catincidents-usecase.md)

</td><td>

Enables fulfillers to determine the category, subcategory, and configuration item automatically for a given incident. After categorizing the incident, it looks for related major incidents or known problems and links them automatically.

</td><td>

1.  Categorize incident AI agent
2.  Link major incident AI agent
3.  Link incident to problem AI agent

</td></tr><tr><td>

[Investigate and resolve ITSM incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-incident-resolver-workflow.md)

</td><td>

Provides recommendations for a resolution using catalog, Knowledge, and past incidents and sends the information to the user.

</td><td>

1.  Find catalog item AI agent
2.  ITSM incident resolution investigation AI agent

</td></tr><tr><td>

[Manage Microsoft 365 group members](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-O365-groupmembers-workflow.md)

</td><td>

Adds or removes groups and email distribution lists from the Microsoft 365 group.

</td><td>

Microsoft 365 group membership AI agent

</td></tr><tr><td>

[Generate post incident reviews](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-mim-usecase.md)

</td><td>

Generates a post-incident report for major incidents and notifies the fulfiller.

</td><td>

Post-incident review AI agent

</td></tr><tr><td>

[Generate change request plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-change-planner-usecase.md)

</td><td>

Generates a comprehensive implementation, test, and backout plan based on the specified change request number. It also analyzes the potential risk and impact of a change request and proposes a justification.

</td><td>

1.  Change implementation plan AI agent
2.  Change backout plan AI agent
3.  Change test plan AI agent
4.  Change risk and impact analysis AI agent
5.  Change justification proposal AI agent
6.  Finish change plan AI agent

</td></tr><tr><td>

[Notify users with Twilio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-twilio-text-usecase.md)

</td><td>

Sends text messages to recipients using Twilio.

</td><td>

Twilio SMS text AI agent

</td></tr></tbody>
</table>**Important:** By default, all agentic workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for ITSM agentic workflows. For information on Large Language Models \(LLMs\) for AI agents and agentic workflows, see [Select the LLM for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/select-aia-llm.md).

**Note:** The Notify users with Twilio agentic workflow can only be invoked using a manual trigger.

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/intelligent-experiences/enable-ai-experiences/find-ai-agents.md).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

-   **[IT Service Management AI agent collection Triage and categorize ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-catincidents-usecase.md)**  
Use the Triage and categorize ITSM incidents AI agent team to assign incident categories, subcategories, configuration items \(CI\), major incidents, and known problems autonomously.
-   **[IT Service Management AI agent collection Investigate and resolve ITSM incidents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-incident-resolver-workflow.md)**  
Use the Investigate and resolve ITSM incidents AI agent team to get recommendations to resolve an incident based on the incident number. Check for related catalog items, Knowledge articles, and similar resolved incidents to generate resolution steps for the incident.
-   **[IT Service Management AI agent collection Manage Microsoft 365 group members agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-O365-groupmembers-workflow.md)**  
Use the Microsoft 365 group membership AI agent to manage users in the Microsoft 365 email distribution list.
-   **[IT Service Management AI agent collection Generate post incident reviews agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-mim-usecase.md)**  
Use the Post-incident review AI agent to generate a review report after a major incident is closed. You can review and revise this report if necessary.
-   **[IT Service Management AI agent collection Generate change request plans agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-change-planner-usecase.md)**  
Use the Change request planning AI agent team to monitor similar change requests autonomously and generate the necessary plans. This approach may help reduce the time required for scheduling changes and managing change-related risks.
-   **[IT Service Management AI agent collection Notify users with Twilio agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm-aiagents-twilio-text-usecase.md)**  
Use the Twilio SMS text AI agent to help streamline communication processes and enhance workflow efficiency.

**Parent Topic:**[Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/now-assist-for-it-service-management-itsm/now-assist-itsm.md)

