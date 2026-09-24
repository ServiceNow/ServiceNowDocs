---
title: Using agentic workflows in ServiceNow Otto for Manufacturing Commercial Operations
description: Use the MCO AI agents within an agentic workflow to extract relevant data from repair documents, enabling the generation of corrective actions and associated charges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-use-agenetic-workflows.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, Manufacturing Commercial Operations]
---

# Using agentic workflows in ServiceNow Otto for Manufacturing Commercial Operations

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
</table>Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aia-security-implementation.md)

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

-   **[Using generative AI in ServiceNow Otto for Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-use-generative-ai-skills.md)**  
If you have an agent role, you can summarize the report details with the ServiceNow Otto for MCO application.
-   **[Execute recall campaigns faster agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-execute-recall-campaigns-faster-ai-wf.md)**  
Use MCO AI agents agentic workflow to generate the corrective actions and charges for the required repair documents quickly and efficiently.

**Parent Topic:**[Using Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/manufacturing-using.md)

**Related topics**  


[Explore AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-ai-agents.md)

[Create recall corrective actions using ServiceNow Otto for MCO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/execute-recall-campaigns.md)

[Large language models on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/exploring-large-language-models.md)

