---
title: Create a prompt
description: After you create a custom skill, create a prompt. The prompt defines the instructions that the skill sends to the LLM and the skill inputs that it uses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-skill-kit/create-prompt-template.html
release: brazil
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Using AI Skill Kit, AI Skill Kit, Generative AI skills, Enable AI Experiences]
---

# Create a prompt

After you create a custom skill, create a prompt. The prompt defines the instructions that the skill sends to the LLM and the skill inputs that it uses.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **AI Skill Kit** &gt; **Home**.

2.  Select the skill that you want to create a prompt for.

3.  Select the edit icon \[Omitted image "icon-edit-pencil.png"\] Alt text: and name the prompt.

4.  Write the prompt.

5.  Select **Skill Inputs**.

    \[Omitted image "nask-add-skill-input.png"\] Alt text: Add skill input modal in AI Skill Kit.

<table id="table_vmq_tgh_lcc"><thead><tr><th>

Input type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Datatype

</td><td>

-   Record
-   String
-   Numeric
-   Boolean
-   Simple Array
-   JSON Object
-   JSON Array


</td></tr><tr><td>

Name

</td><td>

Name of the input.

</td></tr><tr><td>

Description

</td><td>

Description of the input.

</td></tr><tr><td>

Mandatory

</td><td>

Option to require a value for the input when the skill runs.

</td></tr><tr><td>

Truncate

</td><td>

Option to shorten the prompt context to fit the model context length when the prompt is too large.

</td></tr><tr><td class="sub-head" colspan="2">

For records

</td></tr><tr><td>

Table name

</td><td>

Name of the table that contains the test record.

</td></tr><tr><td>

Choose test record

</td><td>

Record used to test the prompt.

</td></tr><tr><td class="sub-head" colspan="2">

For String, Numeric, Boolean, Simple Array, JSON Object, and JSON Array

</td></tr><tr><td>

Test values

</td><td>

Values used to test the prompt.

</td></tr></tbody>
</table>6.  Select **Add skill input**.

7.  Select **Insert inputs**.

    The input options change depending on the data type that you select.

8.  Search for the inputs that you want to use for the prompt.

    For example, you can search for the incident short description or priority.

9.  If you're not ready to finalize the prompt and publish the skill, select **Save** or **Save as**.

    **Note:** Skills can have multiple prompts. Usage conditions determine which prompt is executed. If no conditions are met, the default prompt is executed. To configure prompt usage conditions, see [Configure a skill prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/configure-skill-prompt.md).


## What to do next

After you create a prompt, test it. To learn more about testing your prompt, see [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md).

-   **[Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/add-a-tool.md)**  
Add and manage tools visually in the Tools editor, including decision branching, to execute different tools for your skill. Adding decision branches between tools enables you to define the conditions that must be met for a tool to run. If no conditions are met, the default branch's step is executed.

**Parent Topic:**[Using AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill]()

[Use prompt assistance]()

[Test a prompt]()

[Evaluate a prompt]()

[Finalize and publish a skill]()

[Activate a skill]()

[Call a custom skill from a script]()

