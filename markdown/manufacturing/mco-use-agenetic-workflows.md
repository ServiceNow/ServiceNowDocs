---
title: Using agentic workflows in Now Assist for Manufacturing Commercial Operations \(MCO\)
description: Use the MCO AI agents within an agentic workflow to extract relevant data from repair documents, enabling the generation of corrective actions and associated charges.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist for MCO, Manufacturing Commercial Operations]
---

# Using agentic workflows in Now Assist for Manufacturing Commercial Operations \(MCO\)

Use the MCO AI agents within an agentic workflow to extract relevant data from repair documents, enabling the generation of corrective actions and associated charges.

<table id="table_zyk_1c2_dhc"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

Execute recall campaigns faster

</td><td>

This workflow enhances the efficiency of recall execution by automatically creating corrective action records and corresponding charge line items using repair documents. The elimination of manual data entry and validation processes reduces cycle time, minimizes errors, and promotes consistency throughout recall operations.

</td><td>

Create recall corrective actions AI agent

 Plan and execute recall campaign phases and subphases AI agent

</td></tr></tbody>
</table>Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aia-security-implementation.md)

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

**Related topics**  


[Explore Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-ai-agents.md)

[Create recall corrective actions using Now Assist for Manufacturing Commercial Operations \(MCO\)](../task/execute-recall-campaigns.md)

[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md)

