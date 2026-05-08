---
title: Use agentic AI in Now Assist for Operational Sustainability \(formerly ESG\)
description: Use agents within an agentic workflow or as standalone agents to achieve specific automated outcomes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [use]
breadcrumb: [Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Use agentic AI in Now Assist for Operational Sustainability \(formerly ESG\)

Use agents within an agentic workflow or as standalone agents to achieve specific automated outcomes.

Find information such as the Large Language Models \(LLM\) supported in Now Assist and security controls that are important considerations for using agentic AI.

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
</table>## Supported Large Language Models

**Note:**

-   -   For the Now LLM Service updates, see Now LLM Service updates.

## Security implementation considerations

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. ACLs provide the Run As capability to let agents and agentic workflows execute actions either as a dynamic user or as an AI user.For more information, see Implement access control in Now Assist AI agents

## Considerations for running the autonomous AI Agents

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first duplicate the agentic workflow, and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.
-   Azure OpenAI is recommended for Now Assist for Operational Sustainability agentic workflows.

-   **[Generate Scope 3 carbon calculations](../task/generate-carbon-calculcations-for-metrics.md)**  
Use the AI-driven workflow to create calculated metric definitions \(CMD\) for Scope 3 carbon emissions. The workflow employs conversational agents and integrated tools to guide methodology selection, map metrics, and simplify sustainability reporting with accuracy and efficiency.

**Parent Topic:**[Now Assist for Operational Sustainability \(formerly ESG\)](now-assist-for-esg.md)

