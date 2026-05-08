---
title: Generate a data binding and formula
description: Automatically generate a data binding and formula using natural language with correct syntax.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Generate a data binding and formula

Automatically generate a data binding and formula using natural language with correct syntax.

## Before you begin

1.  Install UI Generation application \(28.1 – Zurich or later\). For more information, see [Install UI generation](install-ui-generation.md).
2.  Make sure that you have the ui\_builder\_admin role. For more information, see [Grant UI Builder admin role](grant-ui-builder-admin-role.md).

3.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Creator** and activate the Data Binding Generation skill.
4.  Select a large language model \(LLM\) provider.

Role required: ui\_builder\_admin

## About this task

Learn to use Data Binding Generation in ServiceNow® UI Builder with Now Assist to automatically generate bindings and formulas. These bindings can be applied to any component property, such as labels, text, lists, or buttons, and can include logic, calculations, or data transformations.

## Procedure

1.  Open UI Builder.

2.  Create an experience or open an existing one.

    For more information, see [Create an experience for UI Builder](../../ui-builder/task/create-experience.md).

3.  Create a page or open an existing one.

    For more information, see [Create a page in UI Builder](../../ui-builder/task/create-page.md).

4.  Create a page variant or open an existing one.

    For more information, see [Create a page variant](../../ui-builder/task/create-variant.md).

5.  Open the Page Editor.

6.  Add a data resource or open an existing one.

    For more information, see [Add and configure data resources to a page](../../ui-builder/task/add-data-resources.md).

7.  From the Data Binding popover, select **Get started**.

    ![A data binding panel in ServiceNow UI Builder, allowing users to generate and preview formulas or data outputs for page components using natural language prompts.](../image/ui-gen-data-binding-popover.png)

8.  You can enter your prompt using natural language or select one from the examples.

    **Note:** For example:

    -   Instead of writing `IF(@context.propers.bare,"bare page","not bare page")`, you can enter `If the page is bare, show 'bare page'; otherwise, show 'not bare page’`.
    -   Instead of `LEN([1,2,3]), ")`, you can enter `How many items are in this list?`
    ![A data binding panel in ServiceNow UI Builder, where users enter natural language prompts to generate formulas, preview results, and bind data to page components.](../image/ui-gen-data-binding-popover-prompt.png)

9.  Select the arrow to generate a binding or formula.

10. Review the syntax and output.

11. Select **Accept and Edit**.

    ![A data binding panel in UI Builder, where users create a formula for a welcome message, preview formula, and have options to accept, edit, or reject it.](../image/ui-gen-data-binding-popover-accept.png)

12. Apply or reject the binding.

    -   If you’re happy with the output, select **Apply**.
    -   If you’re unhappy with the output, select **Reject** and start over by entering a new prompt.
13. Preview and test the output.


## Result

Data binding and formula are generated.

|Symptom|Cause|Resolution|
|-------|-----|----------|
|Data binding generation returns incorrect syntax|The prompt is ambiguous or uses terms not recognized as synonyms.|Refine the prompt using more specific language. Refer to the Formula Operators table for supported synonyms. Try selecting an example from the Data Binding popover.|

**Parent Topic:**[Using UI generation](../concept/using-ui-generation.md)

**Related topics**  


[Natural language synonyms for formula operators](../reference/natural-language-synonyms-for-formula-operators.md)

