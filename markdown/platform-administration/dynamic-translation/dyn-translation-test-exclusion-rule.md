---
title: Test Exclusion Rule
description: Test Exclusion Rule in Dynamic Translation enables you to test your exclusion pattern manually. You can check whether the pattern accurately excludes a text string from translation.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Exclusion Framework in Dynamic Translation, Configuring Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Test Exclusion Rule

Test Exclusion Rule in Dynamic Translation enables you to test your exclusion pattern manually. You can check whether the pattern accurately excludes a text string from translation.

## Before you begin

At least one additional language must be available on your instance. For more information about installing languages, see [Activate a language](../../localization/task/t_ActivateALanguage.md).

Role required: admin

## About this task

Test Exclusion Rule opens a record producer where your exclusion pattern can be tested manually on a text string that you enter. Several of the fields on the record producer change depending on the following choices.

-   You can test an exclusion pattern before or after you create an exclusion rule \(New or Existing rule\).
-   You can test either type \(Exact match or Pattern match\).

If you choose New exclusion rule, you can opt to create a new rule based on your test pattern.

You can select a target language from among the languages enabled on the instance. The target language is the language you want to translate into. The output shows the translation with the matching sequence displayed in bold font.

You can test iteratively to refine your exclusion pattern.

![Test Exclusion Rule is highlighted in the navigation.](../image/dyn-translation-test-exclusion-rule1Z.png "Navigation for Test Exclusion Rule")

## Procedure

1.  Navigate to **All** &gt; **Dynamic Translation** &gt; **Test Exclusion Rule**.

    A record producer opens.

2.  Select the appropriate option for the first question, **Do you want to test an existing or new exclusion rule?**

<table id="choicetable_smp_tfm_tfc"><thead><tr><th align="left" id="d189800e136">

Option

</th><th align="left" id="d189800e139">

Description

</th></tr></thead><tbody><tr><td id="d189800e145">

**Existing exclusion rule**

</td><td>

If you choose this option, the next field opens: **Which exclusion pattern would you like to test?** Select your pattern from the list, or use the field's search function.The information icon \(![Information icon.](../../localization-framework/image/information-icon.png)\) offers a read-only summary of the selected rule.

</td></tr><tr><td id="d189800e163">

**New exclusion rule**

</td><td>

If you choose this option, two fields and a button appear on the form. 1.  **Rule type**: Choose from
    -   **Exact match**
    -   **Pattern match** \(regex\)
2.  **Exclusion term** \(for Exact match\): enter a text string.

**Exclusion pattern** \(for Pattern match\): enter a regular expression \(regex\) pattern.

3.  **Create Rule**: You can optionally use this button to open a form for a new exclusion rule. The most recent exclusion pattern that you tested is imported into this form.


</td></tr></tbody>
</table>    ![The Test Exclusion Rule form with New exclusion rule and Pattern Match selected.](../image/dyn-translation-test-exclusion-rule2Z.png "Use Pattern match for regular expressions")

3.  **Target language**: Select a language from the languages installed on your instance.

    This is the language you want to translate into.

4.  **Input**: In the source language, enter text containing the string that you want your exclusion pattern or term to match, then select **Submit**.

    ![The Test Exclusion Rule form with an Existing exclusion rule selected and a sample utterance in the Input field.](../image/dyn-translation-test-exclusion-rule3Z.png "Testing an Existing exclusion rule (exact match)")


## Result

The input is translated into the target language, but the part that matched the exclusion pattern remains in the source language. The result is a mix of translated and untranslated text. The match is highlighted in bold font.

![The sample input is translated from English to Spanish. The match is highlighted with bold font.](../image/dyn-translation-test-exclusion-rule4Z.png "Results of Test Exclusion Rule")

If your test pattern did not match any part of the input, the result displays a translation with no bold font.

**Note:** Your input might match other exclusion rules active on your instance. If this occurs, the result displays a mix of translated and untranslated text without bold font. Only matches to the current test pattern display bold font.

When testing variations of existing rules, temporarily deactivating similar rules could help focus on the test pattern.

## What to do next

If you chose **New exclusion rule**, you can create a rule based on the exclusion pattern that you tested. For more information see [Add new rules to Exclusion Framework](dyn-translation-add-exclusion-rule.md).

**Parent Topic:**[Exclusion Framework in Dynamic Translation](../concept/dyn-translation-exclusion-framework.md)

