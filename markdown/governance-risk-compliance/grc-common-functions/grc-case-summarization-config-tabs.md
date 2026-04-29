---
title: GRC case summarization skill configuration fields
description: Review the skill details on each configuration tab before activating the GRC case summarization skill. Even after activation, these fields can be edited to refine the AI-generated summary.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate GRC case summarization, Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# GRC case summarization skill configuration fields

Review the skill details on each configuration tab before activating the GRC case summarization skill. Even after activation, these fields can be edited to refine the AI-generated summary.

<table id="table_c1d_hkd_k3c"><thead><tr><th>

Configuration tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Skill config prompts

</td><td>

Large language model \(LLM\) prompts for generating the summary.

</td></tr><tr><td>

General details

</td><td>

Skill details including name, description, product workflow, product name, LLM service, and skill template.

</td></tr><tr><td>

Choose input

</td><td>

Data the LLM considers when creating the summary. The input fields and rule conditions form an input template. The template can be edited to control what data is sent to the LLM. The configurable fields are:-   **Base input table**: Source table from which the skill pulls case data for the LLM.
-   **Base input fields**: Case record fields sent to the LLM as context for generating the summary.
-   **Add rule conditions to the input template**: Rule conditions that determine when this input template is applied.
-   **Add additional input data sources**: Additional data sources, such as related tables, activity streams, and relationships, that provide more context to the LLM.

</td></tr><tr><td>

Define availability

</td><td>

Conditions that control how and when the skill is available to users.-   **Skill is always available**: Skill runs regardless of conditions.
-   **Customize skill availability**: Skill is only available when conditions are met.

</td></tr><tr><td>

Define access

</td><td>

User roles that can access the skill.

</td></tr><tr><td>

Select display

</td><td>

Display location of the skill and the user roles that see the display.

</td></tr><tr><td>

Review and activate

</td><td>

Summary of the skill configuration.

</td></tr></tbody>
</table>