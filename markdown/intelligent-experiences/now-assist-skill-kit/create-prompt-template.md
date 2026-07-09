---
title: Create a prompt
description: After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/now-assist-skill-kit/create-prompt-template.html
release: zurich
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Create a prompt

After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to create a prompt for.

3.  Select the edit icon \(\[Omitted image "icon-edit-pencil.png"\] Alt text: Now Assist Skill Kit Edit icon.\) and name the prompt.

4.  Write the prompt.

5.  Select **Skill Inputs**.

    \[Omitted image "nask-add-skill-input.png"\] Alt text: Add skill input modal in Now Assist Skill Kit.

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

A name for the table.

</td></tr><tr><td>

Choose test record

</td><td>

The record that is used to test the prompt.

</td></tr><tr><td class="sub-head" colspan="2">

For Strings, Numeric. Boolean, Simple Array, JSON Object, JSON Array

</td></tr><tr><td>

Test values

</td><td>

The values that are used to test the prompt.

</td></tr></tbody>
</table>6.  Select **Add skill input**.

7.  Select **Insert inputs**.

    The input options change depending on what kind of data type you choose.

8.  Search for the inputs that you want to use for the prompt.

    For example, you can search for the incident short description or priority.

9.  If you're not ready to finalize the prompt and publish the skill, select **Save** or **Save as**.

    **Note:** Skills can have multiple prompts. Usage conditions determine which prompt is executed. If no conditions are met, the default prompt is executed. To configure prompt usage conditions, see [Configure a skill prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/configure-skill-prompt.md).


## What to do next

After you have created a prompt, you must test it. To learn more about testing your prompt, see [Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md).

-   **[Add a tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/add-a-tool.md)**  
Add and manage tools visually in the Tools editor, including decision branching, to execute different tools for your skill. Adding decision branches between tools enables you to define the conditions that need to be met for a tool to run. If no conditions are met, the default branch's step is executed.

**Parent Topic:**[Using Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/now-assist-skill-kit/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill]()

[Use prompt assistance]()

[Test a prompt]()

[Evaluate a prompt]()

[Finalize and publish a skill]()

[Activate a skill]()

[Call a custom skill from a script]()

