---
title: Create a prompt
description: After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.
locale: en-US
release: australia
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-04-17"
reading_time_minutes: 4
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Create a prompt

After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to create a prompt for.

3.  In the **Prompt** window, create your prompt.

    For guidance on creating prompts, see [Developing the prompt](../reference/developing-the-prompt.md).

4.  In the **Skill contents** sidebar, select the plus \(+\) icon next to **Skill Inputs**.

5.  In the **Add skill input** window, update the fields as needed.

<table id="table_vmq_tgh_lcc"><thead><tr><th>

Input type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Datatype

</td><td>

Select a data type of the input.-   Record
-   String
-   Numeric
-   Boolean
-   Simple Array
-   JSON Object
-   JSON Array


</td></tr><tr><td>

Name

</td><td>

A name for the input.

</td></tr><tr><td>

Description

</td><td>

A description for the input.

</td></tr><tr><td>

Mandatory

</td><td>

The Mandatory option means that you must supply a value for the input when you run the skill.

</td></tr><tr><td>

Truncate

</td><td>

The Truncate option means that, if your prompt is too large, the prompt context is shortened to fit the model context length.

</td></tr><tr><td class="sub-head" colspan="2">

For Records

</td></tr><tr><td>

Table name

</td><td>

Select a table.

</td></tr><tr><td>

Choose test record

</td><td>

The record that is used to test the prompt, and is the default value for the input.

</td></tr><tr><td class="sub-head" colspan="2">

For Strings, Numeric. Boolean, Simple Array, JSON Object, JSON Array

</td></tr><tr><td>

Test values

</td><td>

Default values that are used when the skill runs. You can override this at run time.

</td></tr></tbody>
</table>6.  Select **Add skill input**.

7.  In the **Prompt** window, position your cursor in the prompt text where you want to insert an input reference, then select **+ Inputs and tools**.

    A search panel appears listing your available skill inputs. Select an input to insert a `{{variablename}}` reference at the cursor position. When the skill runs, the reference is replaced with the actual input value.

    For record inputs, you can reference specific fields on the record using dot notation, for example `{{incident.short_description}}`, `{{incident.priority}}`.

8.  If you're not ready to finalize the prompt and publish the skill, select **Save** or **Save as**.

    **Tip:** A skill can have multiple prompts. The prompt without usage conditions acts as the default — it runs when no other prompt's conditions are met. To add usage conditions to a prompt, select **Manage prompt** and then **Usage conditions**. Usage conditions are built from your skill inputs, so you must have at least one input defined before you can configure them. To learn more about prompt settings and usage conditions, see [Configure a skill prompt](configure-skill-prompt.md).


## What to do next

After you have created a prompt, you must test it. To learn more about testing your prompt, see [Test a prompt](test-prompt-template.md).

-   **[Add a tool](../concept/add-a-tool.md)**  
Add and configure tools in the Now Assist Skill Kit tool canvas to gather data and context before a prompt runs. Tools can be chained sequentially, run in parallel, or branched conditionally using decision nodes.
-   **[Add a retriever](add-retriever.md)**  
Add a retriever to your prompt to augment and add context to your prompts with AI search results.
-   **[Add a web search tool](add-web-search.md)**  
Add a web search tool to your skill to retrieve web content and include it as context in your prompt.

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)

