---
title: Using agentic workflows in Now Assist for Manufacturing Commercial Operations \(MCO\)
description: Use the MCO AI agents within an agentic workflow to extract relevant data from repair documents, enabling the generation of corrective actions and associated charges.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/manufacturing/mco-use-agenetic-workflows.html
release: zurich
topic_type: concept
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Now Assist for MCO, Manufacturing Commercial Operations]
---

# Using agentic workflows in Now Assist for Manufacturing Commercial Operations \(MCO\)

Use the MCO AI agents within an agentic workflow to extract relevant data from repair documents, enabling the generation of corrective actions and associated charges.

|Agentic workflow name|Description|Available AI agents|
|---------------------|-----------|-------------------|
|Execute recall campaigns faster|This workflow enhances the efficiency of recall execution by automatically creating corrective action records and corresponding charge line items using repair documents. The elimination of manual data entry and validation processes reduces cycle time, minimizes errors, and promotes consistency throughout recall operations.|Create recall corrective actions AI agent|

Enable security implementation to execute AI agents and agentic workflows through Access Control Lists \(ACLs\) and user identities. For more information, see [Implement access control in AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)

**Important:** By default, all agent workflow and AI agent records are read-only.

To run the AI agents autonomously, you must first [duplicate the agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/clone-aia-usecase.md), and then proceed with the following steps:

-   Activate the agentic workflow.
-   Activate all agents within the agentic workflow.
-   Activate the trigger to invoke the agentic workflow automatically. The triggers for each agentic workflow must be unique. If you prefer to invoke it manually, activating the trigger isn’t necessary.

**Related topics**  


[Explore AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-ai-agents.md)

[Execute recall campaigns faster Agentic Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/manufacturing/execute-recall-campaigns.md)

[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)

