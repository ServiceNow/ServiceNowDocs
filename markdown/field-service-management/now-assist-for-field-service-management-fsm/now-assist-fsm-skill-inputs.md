---
title: Skill inputs for Now Assist for Field Service Management \(FSM\)
description: Use the inputs for each skill to configure how a skill is used.
locale: en-US
release: australia
product: Now Assist for Field Service Management \(FSM\)
classification: now-assist-for-field-service-management-fsm
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for FSM]
---

# Skill inputs for Now Assist for Field Service Management \(FSM\)

Use the inputs for each skill to configure how a skill is used.

## Skills Overview

Depending on the selected skill, you can configure inputs. These settings determine how a skill is used. An input identifies the data that is used for a skill, such as the table and fields used to generate a work order task summary.

You can use Now LLM Service, Now LLM Long Term Stable models \(LTS\), Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for all Now Assist skills and AI agents. Use the Configuration Controls in [AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-model-providers.md) to define which options are available, then set the skill-level preferences in the [Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manage-large-language-models.md). For more information, see [Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/servicenow-large-language-model-now-llm/exploring-large-language-models.md).

## Work order task summarization skill

The work order task summarization skill includes the inputs that identify the table and fields that are used when a closure note summary is generated.

The following table lists the inputs for the work order task summarization skill.

<table id="table_case_summary_inputs"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Work Order Task \[wm\_task\]

</td></tr><tr><td>

Input fields

</td><td>

-   Description
-   Short description
-   Work notes
-   Additional comments
-   Affected Product name
-   Part requirement model
-   Part requirement required quantity
-   Part requirement reserved quantity

</td></tr></tbody>
</table>## KB generation skill

The KB generation skill includes the inputs that identify the table and fields that are used when the knowledge article draft is generated for a case.

The following table lists the inputs for the knowledge article generation skill.

<table id="table_mnf_45q_1bc"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input table

</td><td>

Work Order Task \[wm\_task\]

</td></tr><tr><td>

Input fields

</td><td>

-   Short description
-   Description
-   Work notes
-   Comments

</td></tr></tbody>
</table>