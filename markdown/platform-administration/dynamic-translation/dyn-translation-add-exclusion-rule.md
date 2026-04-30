---
title: Add new rules to Exclusion Framework
description: Add terms and patterns that shouldn't be machine translated to the Exclusion Rules table. You can create either exact match rules or pattern match rules, and you can edit your rules later.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2024-10-24"
reading_time_minutes: 3
breadcrumb: [Exclusion Framework in Dynamic Translation, Configuring Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Add new rules to Exclusion Framework

Add terms and patterns that shouldn't be machine translated to the Exclusion Rules table. You can create either exact match rules or pattern match rules, and you can edit your rules later.

## Before you begin

Role required: admin

## About this task

By default Exclusion Framework provides several activated rules in the Exclusion Rules table \[sn\_dt\_exclusion\_rule\]. Before creating your own rules, review the default rules to check whether they are appropriate for your requirements. Navigate to **All** &gt; **Dynamic Translation** &gt; **Exclusion Framework** &gt; **Exclusion Rules** and select a rule name to open its record.

Default rules can be deactivated but not edited, and they are in the Dynamic Translation application scope. The rules you create can be deactivated or edited.

There are two types of exclusion rules.

-   Exact match rules search for the term you input. Case sensitivity can be enabled for these rules using the **Ignore Case** check box.
-   Pattern match rules use regular expressions \(regex\) to find text strings such as Sys IDs and KB article numbers. These text strings may contain varying combinations of characters but they follow a defined pattern. The **Add Row** form performs a basic validity check on the regex, displaying the error "The input is not a valid regex pattern" when the check fails.

**Note:** ServiceNow supports only Java regular expressions \(regex\), not Perl or other vendor options.

The **Create New Rules** module opens a record producer that supports adding multiple rules at one time. There is a maximum limit of 50 rules per type per submission. That limit applies only to the submission form, not to the Exclusion Rules table.

Exclusion rules are applied to your text in sequence. When Exclusion Framework finds a match it stops, so later rules are not applied. You can set the order in which rules are applied by filling in the optional **Order** field.

1.  Rules with a value in the **Order** field are evaluated from lowest number first \(such as 1\) to highest number last \(such as 100\).
2.  Next, rules without a value in the **Order** field are evaluated according to age. The oldest rule is evaluated first, and the newest rule is evaluated last.

Exclusion rules must be unique within a domain. An attempted duplicate submission displays a banner with the message "Exclusion term and Domain combination already exists."

## Procedure

1.  Ensure that you are in the application scope that you want for your rules, then navigate to **All** &gt; **Dynamic Translation** &gt; **Exclusion Framework** &gt; **Create New Rules**.![Record producer for Create Exclusion Rules.](../image/dyn-translation-add-exclusion-rule1X.png)

    A modal for a record producer opens, so you can add multiple rules at one time.

2.  From the record producer, select **Add** for either exact match or pattern match, as appropriate. ![Modal for adding an exact match exclusion term.](../image/dyn-translation-add-exclusion-rule2X.png)

3.  On the **Add Row** form, configure the fields according to the following guidance.

<table id="choicetable_kb3_lpm_ddc"><thead><tr><th align="left" id="d270400e188">

Rule type

</th><th align="left" id="d270400e191">

Fields

</th></tr></thead><tbody><tr><td id="d270400e197">

**Exact Match**

</td><td>

-   **Rule name**
-   **Exclusion term \(exact match\)**: You can enter terms that contain spaces.
-   **Order**: Optional. See the previous explanation.


</td></tr><tr><td id="d270400e223">

**Pattern Match**

</td><td>

-   **Rule name**
-   **Rule description**: Describe what the regex pattern is looking for.
-   **Exclusion pattern \(regex only\)**: enter the pattern as a regular expression.
-   **Order**: Optional. See the previous explanation.


</td></tr></tbody>
</table>4.  Edit or delete any rows as needed, then select **Submit**.

    Your rules are added to the Exclusion Rules table and activated.


## What to do next

You can edit and deactivate your rules in the Exclusion Rules table. Navigate to **All** &gt; **Dynamic Translation** &gt; **Exclusion Framework** &gt; **Exclusion Rules**, then select the rule name to open its record.

For exact match rules, you can modify the case sensitivity in its Exclusion Rules record.

-   Select the **Ignore Case** check box to enable case insensitive matching \(for example, the entry "hello" would match "Hello", "hEllo", "helLo" and so forth.\)
-   Clear the **Ignore Case** check box to match the entry exactly as it appears in the table, including its casing.

**Parent Topic:**[Exclusion Framework in Dynamic Translation](../concept/dyn-translation-exclusion-framework.md)

