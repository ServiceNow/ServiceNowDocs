---
title: Create a prompt
description: After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.
locale: en-US
release: xanadu
product: Now Assist Skill Kit
classification: now-assist-skill-kit
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Now Assist Skill Kit, Now Assist Skill Kit, Enable AI experiences]
---

# Create a prompt

After you create a custom skill, create a prompt. Creating a prompt enables you to choose what skill inputs to use, as well as the type of tool.

## Before you begin

Role required: sn\_skill\_builder.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Home**.

2.  Select the skill that you want to create a prompt for.

3.  Select the edit icon \(![Now Assist Skill Kit Edit icon.](../image/icon-edit-pencil.png)\) and name the prompt.

4.  Write the prompt.

5.  Select **Skill Inputs**.

    ![Add skill input modal in Now Assist Skill Kit.](../image/nask-add-skill-input.png)

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

The Truncate option means that, if your prompt is too big, the prompt context will be shortened to fit the model context length.

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

9.  Add a tool.

    ![Add tool modal in Now Assist Skill Kit.](../image/nask-add-tool.png)

10. On the form, fill in the fields.

<table id="table_p4n_2vg_lcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="4">

Type

</td><td>

Flow Action.

</td></tr><tr><td>

Retriever.

</td></tr><tr><td>

Subflow.

</td></tr><tr><td>

Script.

</td></tr><tr><td>

Name

</td><td>

The name of the tool.

</td></tr><tr><td>

Conditions

</td><td>

-   Always
-   Script


</td></tr></tbody>
</table>11. Select **Add**.

12. If you're not ready to finalize the prompt and publish the skill, select **Save** or **Save as**.


## What to do next

After you have created a prompt, you must test it. To learn more about testing your prompt, see [Test a prompt](test-prompt-template.md).

-   **[Add a retriever](add-retriever.md)**  
Add a retriever to your prompt to augment and add context to your prompts with AI search results.

**Parent Topic:**[Using Now Assist Skill Kit](../concept/using-now-assist-skill-kit.md)

**Related topics**  


[Create a skill](create-new-skill.md)

[Use prompt assistance](use-prompt-assistance.md)

[Test a prompt](test-prompt-template.md)

[Evaluate a prompt](evaluate-prompt.md)

[Finalize and publish a skill](publish-skill.md)

[Activate a skill](activate-skill.md)

[Call a custom skill from a script](call-custom-skill-from-script.md)

