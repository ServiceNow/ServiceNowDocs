---
title: Using agentic workflows in Now Assist for PSDS
description: Automate the process of synthesizing similar information requests, associated fees, and apply those fees to cases​ using the Help manage public information requests agentic workflow, as part of the Public Sector Digital Services AI Agent Collection application. ​
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Using agentic workflows in Now Assist for PSDS

Automate the process of synthesizing similar information requests, associated fees, and apply those fees to cases​ using the **Help manage public information requests** agentic workflow, as part of the Public Sector Digital Services AI Agent Collection application. ​

The following table lists the skills and agents associated with this workflow. These AI agents work to arrive at a subtotal fee estimate, a recommendation for whether a fee waiver request should be approved or rejected, and a total fee estimate with the fee waiver, if applicable.

**Important:** In the **Define availability** screen for the AI agent, make sure that the **Status** field is enabled to activate the AI agent.

<table id="table_hzb_sd4_cfc"><thead><tr><th>

Agentic Workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Help manage public information requests

</td><td>

-   Analyzes fee waiver justification from applicant for an information request case record, and validates justification against predefined rules
-   Outlines the steps required to estimate the fees associated with an information request
-   Retrieves similar case records and allows user to exclude any from the fee calculation
-   Estimates and communicates fee breakdown associated with an information request case record based on similar request queries and request details from the user
-   Communicates sub-total estimate, fee waiver recommendation, and total with fee waiver.

</td><td>

1.  Information Request Playbook Fee Estimation Agent
2.  Information Request Playbook Fee Waiver Review Agent

</td></tr></tbody>
</table>Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:**

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). For more information, see .

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user. For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for ITSM agentic workflows. For information on Large Language Models \(LLMs\) for AI agents and agentic workflows, see [Select the LLM for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=select-aia-llm&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Related topics**  


[Public Sector Digital Services AI agent collection Help manage public information requests workflow](estimate-fees-ai-agents-using.md)

