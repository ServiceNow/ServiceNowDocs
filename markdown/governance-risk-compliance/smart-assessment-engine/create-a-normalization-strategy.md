---
title: Create a normalization strategy
description: You can create a custom normalization strategy as required.
locale: en-US
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Normalization in assessment, Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Create a normalization strategy

You can create a custom normalization strategy as required.

## Before you begin

-   Confirm that the Basic Scoring for Smart Assessments plugin \[com.sn\_smart\_scoring\] is installed.
-   Role required: sn\_smart\_asmt.assessment\_admin and sn\_smart\_asmt.developer

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Normalization Strategies**.

2.  On the Scoring normalization strategies list, select **New** and then fill in the form.

<table id="table_krg_p53_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique meaningful name for the normalization strategy.

</td></tr><tr><td>

Published

</td><td>

Displays checked when the normalization strategy is published.

</td></tr><tr><td>

Retired

</td><td>

Displays checked when the normalization strategy is retired.

</td></tr><tr><td>

Description

</td><td>

Text that helps others to understand the purpose of this normalization strategy.

</td></tr><tr><td>

Strategy

</td><td>

Enables the script for the normalization strategy.**Note:** When ECMAScript 2021 \(ES12\) mode is enabled, you can use the latest supported JavaScript features in your script. If this mode is turned off, your script will be limited to the JavaScript features supported by the application’s default environment.

</td></tr></tbody>
</table>3.  Select **Save**.

    A new related list **Scoring normalization strategy inputs** appears.

4.  On the Scoring normalization strategies inputs list, select **New** and then fill in the form.

<table id="table_gls_gb2_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Normalization strategy

</td><td>

The name of the normalization strategy in which inputs are to be created.

</td></tr><tr><td>

Order

</td><td>

Order of the input.

</td></tr><tr><td>

Type

</td><td>

Type of the input. For example: Number or Choice.

</td></tr><tr><td>

Label

</td><td>

Label of the input.

</td></tr><tr><td>

Name

</td><td>

Name of the input.**Note:** Strategy input names must start with a letter, underscore \(\_\), or dollar sign \($\), and may only contain ASCII letters, digits, underscores, or dollar signs. Avoid using spaces, special characters, or reserved keywords, as these are not permitted.

</td></tr><tr><td>

Description

</td><td>

Text that helps others to understand the purpose of this input.

</td></tr></tbody>
</table>5.  Select **Submit**.

    Continue adding inputs as needed by repeating these steps.

    If the input is **Choice**, then a choice related list appears

6.  To add choices select the corresponding choice label from the Scoring normalization strategy inputs list.

7.  On the related list Scoring normalization strategy input choices list, select **New** and then fill in the form.

    |Field|Description|
    |-----|-----------|
    |Normalization strategy input|The name of the normalization strategy input in which choices are to be created.|
    |Order|Order of the input choice.|
    |Label|Label of the choice.|
    |Value|Value of the choice.|

8.  Select **Update**.

    Continue adding input choices as needed by repeating these steps.

9.  Update the strategy script to incorporate the newly created input values for normalizing raw scores.

    -   You can create scripts to define the transformation logic or formula needed to normalize the raw score effectively.
    -   You can also set up conditions within the script.
    -   You can confirm that the input in **result.value** must always be floating-point number for all question types.
10. Select **Publish**.

    After creating a custom strategy, you can manage it further by moving it back to draft to make edits, retiring it when it's no longer needed, or deleting it permanently.


