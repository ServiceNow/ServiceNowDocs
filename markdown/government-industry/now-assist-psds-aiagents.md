---
title: Standalone AI Agents in Public Sector Digital Services
description: Use standalone agents to achieve specific automated outcomes with the Public Sector Digital Services AI Agent Collection application. ​
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-11-06"
reading_time_minutes: 1
breadcrumb: [Using agentic AI, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Standalone AI Agents in Public Sector Digital Services

Use standalone agents to achieve specific automated outcomes with the Public Sector Digital Services AI Agent Collection application. ​

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

The following table describes the available AI agents in the Now Assist for Public Sector Digital Services \(PSDS\) application.

<table id="table_hzb_sd4_cfc"><thead><tr><th>

AI Agent name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Information Request Playbook Fee Estimation Agent

</td><td>

-   Analyzes fee waiver justification from applicant for an information request case record, and validates justification against predefined rules
-   Outlines the steps required to estimate the fees associated with an information request
-   Retrieves similar case records and allows user to exclude any from the fee calculation
-   Estimates and communicates fee breakdown associated with an information request case record based on similar request queries and request details from the user
-   Communicates sub-total estimate, fee waiver recommendation, and total with fee waiver.

</td></tr></tbody>
</table>**Note:** Verify that AI Search is enabled on the instance before configuring the agents.

There may be AI agents installed with the Now Assist application that are not used in use cases. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)

**Related topics**  


[estimate-fees-ai-agents-using]

