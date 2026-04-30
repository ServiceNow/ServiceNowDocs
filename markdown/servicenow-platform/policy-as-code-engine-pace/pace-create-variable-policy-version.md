---
title: Create a new variable for a policy version
description: Create an API Variable, Config Parameter, or Record Reference for the policy version in the Define Variables section of the Policy Builder.
locale: en-US
release: yokohama
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Passing parameters to PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Create a new variable for a policy version

Create an API Variable, Config Parameter, or Record Reference for the policy version in the Define Variables section of the Policy Builder.

## Before you begin

If you want to create a variable that will apply to all of your policies, then do the following:

1.  Go to the Variable Definition section on the main page.
2.  Select the variable section that you want to create.
3.  Select **Add**.

When you save the variable, it will show up in the Define Variables section on the Policy Builder of the policy.

Role required: sn\_pace.code\_editor

## Procedure

1.  In the **Policy builder** tab, select the version of the policy you want to add a new variable to, then the Data sources icon ![Data source icon](../image/pace-data-source-icon.jpg).

2.  Select the variable tab that you want to create a variable from then select **Add**.

    ![Data source tab.](../image/pace-data-source-tab-3.jpg)

    ![Create new API variable window.](../image/pace-create-new-variable-window-2.jpg)

    A pop-up window appears titled with the variable you want to create.

3.  On the form, fill in the fields as needed.

<table id="table_ebc_dmk_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Label name of the variable.

</td></tr><tr><td>

Name

</td><td>

Name of the variable.

</td></tr><tr><td>

Type

</td><td>

Drop-down list of input types:-   Basic Date/Time
-   Basic Time
-   Choice
-   Data Array
-   Data Object
-   Decimal
-   Email
-   Integer
-   IP Address
-   JSON
-   Other Date
-   Reference
-   String
-   Sys ID \(GUID\)
-   True/False
Depending on the input you choose, the Advanced Options provides different fields for some inputs. For more information, see the [Data type descriptions](../reference/pace-data-type-descriptions.md) topic.

**Note:** The list only shows the most common used data types.

</td></tr><tr><td>

Mandatory

</td><td>

Option to make this variable mandatory.When the variable is mandatory, a value must be provided when mapping the policy. Otherwise the policy can’t be executed.

</td></tr><tr><td>

Description

</td><td>

Description of the variable.**Note:** When you add a description for a Config Parameter variable, it will show up under the tool tip icon ![Tool tip icon.](../image/pace-info-icon.jpg) in the Test Parameters tab.

</td></tr><tr><td>

Default Value

</td><td>

Default value for the variable.**Note:** When you create a record reference, select a reference in the Table field, this field enables you to select a dependent document from the reference.

</td></tr><tr><td>

Function \(Optional\)

</td><td>

Functions to aggregate your condition. Choices are as follows:-   Average: Average value of the condition.
-   Count: Count of the number of non-null values.
-   Maximum: Largest or maximum value.
-   Minimum: Minimum value.
-   Standard deviation: Population of standard deviation.
-   Sum: Sum of all values.
**Note:** This field will only show up in the Record Reference variable form with the qualifier condition fields.

</td></tr><tr><td>

Match criteria

</td><td>

A match criteria for your record reference. Choices are as follows.-   Select first match
-   Error on multiple
When you create a Record Reference, it will query multiple answers. The match criteria enables you to filter out the match by selecting the first match or return an error if there are multiple answers.

**Note:** This field will only show up in the Record Reference variable form with the qualifier condition fields. For more information about condition fields, see [Policy logic condition fields](../reference/pace-policy-logic-fields.md).

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

You can add your variables into the Policy Builder as needed. Additionally, you can delete a variable by selecting it and selecting the **Delete** button.

