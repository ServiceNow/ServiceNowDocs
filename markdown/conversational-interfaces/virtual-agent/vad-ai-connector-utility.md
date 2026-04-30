---
title: AI Connector utility
description: Use this utility to link generative AI to custom skills for improved performance.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-03-25"
reading_time_minutes: 1
keywords: [Virtual Agent, Designer, AI Connector, utility, LLM, GenAI, Generative AI, Now Assist, Custom skills]
breadcrumb: [Virtual Agent Designer utilities, Virtual Agent Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# AI Connector utility

Use this utility to link generative AI to custom skills for improved performance.

## AI Connector utility properties

Specify the flow action properties for the node that you want to create.

<table id="action-utility-properties-sheet-table"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name of the AI Connector node.

</td></tr><tr><td>

Select custom skill

</td><td>

Open the drop-down menu to search for a custom skill.

</td></tr><tr><td>

Wait for response

</td><td>

Activate this toggle switch to wait for a response from the action before continuing the conversation.

</td></tr><tr><td class="sub-head" colspan="2">

Input and Output mappings

</td></tr><tr><td colspan="2">

All input and output mappings are based on the custom skill you select. For more information on custom skills, see [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), [Managing custom skills in Assistant Designer Asset library](../concept/managing-custom-skills.md), and [Using AI agents in Virtual Agent topics](../../now-assist-skill-kit/reference/ai-agent-custom-skill.md).

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example AI Connector utility

![AI Connector utility with no skill selected. The utility functions only after you select a custom skill that includes a query.](../images/vad-ai-connector-utility-properties.png)

![AI Connector utility with Web Search skill selected. All input and output mappings derive from the custom skill.](../images/vad-ai-connector-utility-properties-with-skill.png)

**Parent Topic:**[Virtual Agent Designer utilities](va-utilities.md)

