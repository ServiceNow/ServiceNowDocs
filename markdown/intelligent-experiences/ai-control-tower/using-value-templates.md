---
title: Using value templates
description: Use value templates to define, calculate, and track the value delivered by your AI systems and models.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, AI Control Tower, Enable AI experiences]
---

# Using value templates

Use value templates to define, calculate, and track the value delivered by your AI systems and models.

Value templates introduces a unified and structured framework for defining, calculating, and tracking the value delivered by your AI assets. You can define value based on personas and formulas using customizable templates.

Value templates offer the following benefits.

-   Transparency: Provides visibility into how value is determined for an AI asset.
-   Customization: Supports various persona-driven and formula-based definitions.

**Note:** When you change an AI asset state from Managed to Unmanaged, the associated value template state automatically changes from Published to Unmanaged and Draft to Retired. Existing value template mappings remain same, but the AI asset is excluded from value calculations. When you again change the AI asset to Managed state, the value template state \(only Unmanaged mappings\) automatically reverts to Published.

Currently, value templates are supported for skills, AI agents, and AI use cases. A value template is assigned to an asset when a skill, AI agent, or AI use case is activated and deployed as an asset in the system. The following table lists the default value templates.

<table id="table_fbp_pvw_xfc"><thead><tr><th>

AI asset

</th><th>

Default value template

</th></tr></thead><tbody><tr><td>

ServiceNow skill

</td><td>

Daily skill executions \(Usage\) x average time per execution \(Time\) x 50% \(Acceptance rate\) For example, for Incident Summarization skill, if the daily executions are 1500, average time per execution is 0.2 minutes, acceptance rate is 90%, the value as per the default value template is 1500x0.2x90/100, which is 270 minutes.

</td></tr><tr><td>

ServiceNow AI agent

</td><td>

Daily AI agent executions \(Usage\) x average time per execution \(Time\) x 50% \(Acceptance rate\)For example, for Problem investigator agent, if the daily executions are 1000, average time per execution is 1.5 minutes, acceptance rate is 50%, the value as per the default value template is 1000x1.5x50/100, which is 750 minutes.

</td></tr><tr><td>

AWS and Microsoft AI agents

</td><td>

Daily AI agent invocations \(Usage\) x 15 mins \(Time\) x 50% \(Acceptance rate\)

</td></tr><tr><td>

ServiceNow AI use case

</td><td>

Daily AI use case invocations \(Usage\) x average time per invocation \(Time\) x 50% \(Acceptance rate\)

</td></tr></tbody>
</table>-   **[Create a new value template](../task/create-new-value-template.md)**  
Add a value template to define, calculate, and track the value delivered by an AI asset.
-   **[Edit a value template](../task/edit-value-template.md)**  
Edit a value template to update how value is calculated for AI assets.
-   **[Create a new value template mapping](../task/create-value-template-mapping.md)**  
Create a value template mapping for an AI asset to standardize the usage of templates.
-   **[Assign a default template](../task/assign-default-template.md)**  
Assign a template as default to an AI system.
-   **[Review a value template mapping](../task/review-value-template-mapping.md)**  
Review and approve value template mapping for an AI asset.

**Parent Topic:**[Using AI Control Tower](using-ai-control-tower.md)

