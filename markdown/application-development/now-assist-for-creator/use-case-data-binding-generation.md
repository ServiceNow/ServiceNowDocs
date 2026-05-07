---
title: Use case: Generate a data binding and formula
description: Automate data binding configuration without memorizing formula syntax.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Use case, Use, UI generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Use case: Generate a data binding and formula

Automate data binding configuration without memorizing formula syntax.

## Scenario

A developer at a healthcare organization is creating a self-service patient intake portal using UI Builder. The portal features a form that shows dynamic labels based on whether the user is viewing a standard page or a simplified "bare" page layout. The developer needs to configure a label component that changes its text accordingly. Additionally, the developer wants to display the total number of active intake requests submitted that day.

## Problem

The developer is not familiar with UI Builder’s formula syntax. Writing expressions like IF\(@context.props.bare,"bare page","not bare page"\) or LEN\(\[list\]\) requires memorizing the exact syntax, which slows down development and increases the risk of errors. Every time the developer encounters a new binding requirement, they have to look up documentation or ask a colleague.

## Solution

With Data binding generation, the developer describes what they need in plain language directly in the Formula Builder. Now Assist converts the natural language input into the correct formula or data binding syntax automatically. The developer reviews the generated syntax, accepts it, and applies it to the component property in one streamlined flow — without writing a single line of formula code manually.

## Before you begin

Make sure that you install UI generation and that you have the ui\_builder\_admin role. For more information, see [Install UI generation](../task/install-ui-generation.md) and [Grant UI Builder admin role](../task/grant-ui-builder-admin-role.md).

## Configuration steps

Perform the following steps to use Data binding generation:

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.
2.  Navigate to the patient intake experience.
3.  Open the page variant in the Page Editor.
4.  Select the label component and open the Data binding popover.
5.  Select **Get started**.
6.  Enter the prompt: `If the page is bare, show ‘Simplified View’; otherwise, show ‘Standard View’.`

    **Tip:** Refer to the examples in the Data Binding popover to understand which types of natural language prompts are most effective. Prompts that clearly describe the condition and possible outcomes typically yield the most accurate results.

7.  Select the arrow to generate the binding.

    Now Assist generates: `IF(@context.props.bare,"Simplified View","Standard View")`.

8.  Review the syntax, select **Accept and Edit**, then select **Apply**.
9.  Enter a prompt to request count label: `Enter how many active intake requests are there today?`

    Now Assist generates: `LEN([@data.activeIntakeRequests])`.

10. Preview and test the page to confirm both bindings render correctly.

## Outcome

The developer sets up a dynamic binding quickly, without referring to the documentation. This eliminates syntax errors, enabling the developer to focus on experience design rather than writing formulas.

**Parent Topic:**[UI Generation use cases](../task/ui-generation-use-cases.md)

**Related topics**  


[Data binding generation](concept-data-binding-generation.md)

[Generate a data binding and formula](../task/generate-data-bindings-and-formulas.md)

[Natural language synonyms for formula operators](../reference/natural-language-synonyms-for-formula-operators.md)

