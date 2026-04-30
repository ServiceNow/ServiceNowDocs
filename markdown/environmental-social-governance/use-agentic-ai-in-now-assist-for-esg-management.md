---
title: Use agentic AI in Now Assist for Operational Sustainability
description: Use AI agents within an agentic workflow or as standalone agents to achieve specific automated outcomes.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-06"
reading_time_minutes: 2
keywords: [use]
breadcrumb: [Now Assist for Operational Sustainability, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Use agentic AI in Now Assist for Operational Sustainability

Use AI agents within an agentic workflow or as standalone agents to achieve specific automated outcomes.

Find information such as the large language models \(LLM\) supported in Now Assist and security controls that are important considerations for using agentic AI.

## Agentic workflows in Now Assist for Operational Sustainability

<table id="table_ycb_p4p_hhc"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Carbon calculations

</td><td>

Accelerate carbon reporting with AI-powered calculations, validation, and insights for Scope 3 emissions.

</td><td>

-   Documents and visual insights AI agent
-   Calculations operands AI agent

</td></tr></tbody>
</table>## Supported large language models

**Note:**

-   You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://www.servicenow.com/docs/access?context=ai-model-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   For the Now LLM Service updates, see [Now LLM Service updates](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user.For more information, see [Implement access control in Now Assist AI agents](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)

## Considerations for running autonomous AI agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run AI agents autonomously, you must first [duplicate the agentic workflow](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

-   **[Generate Scope 3 carbon calculations](../task/generate-carbon-calculcations-for-metrics.md)**  
Use the carbon calculations agentic workflow to create a calculated metric definition \(CMD\) for Scope 3 carbon emissions. The workflow employs AI agents and integrated tools to guide methodology selection, map metrics, and simplify sustainability reporting with accuracy and efficiency.

**Parent Topic:**[Now Assist for Operational Sustainability Management](now-assist-for-esg.md)

