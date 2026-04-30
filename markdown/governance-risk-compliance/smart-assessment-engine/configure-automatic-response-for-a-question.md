---
title: Configure an automatic response for a question
description: Set up automatic responses for assessment questions using either static responses or script-based responses based on specific conditions. You can configure default responses for text, drop-down list, radio button, check box, date, and number question types. This feature helps save assessors time and effort by reducing the number of questions that require answers.
locale: en-US
release: yokohama
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Automate response, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Configure an automatic response for a question

Set up automatic responses for assessment questions using either static responses or script-based responses based on specific conditions. You can configure default responses for text, drop-down list, radio button, check box, date, and number question types. This feature helps save assessors time and effort by reducing the number of questions that require answers.

## Before you begin

The Advanced Response Automation for Smart assessment plugin \(com.sn\_smart\_resp\_auto\) must be installed.

**Note:** If you have the assessment admin or template manager role, you can configure a default or conditional default response for a question. To create scripts, you need the developer role in addition to the assessment admin or template manager role.

Role required: sn\_smart\_asmt.assessment\_admin or sn\_smart\_asmt.template\_manager and sn\_smart\_asmt.developer

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace** to access the Assessment Workspace landing page.

2.  Create an assessment template or open an existing assessment template that is in the Draft state.

    For more information on creating a template, see [Create an assessment template](sae-asmnt-template-create.md).

3.  Select a question for which you want to configure an automatic response.

4.  Select the ![ellipsis icon.](../../../reuse/icons/product-icons/ellipsis-vertical-fill-24.svg) **Configuration options**, then select **Automated response**.

5.  In the **Default response is** field of the **Automated response** pop-up window, select a default response for the question based on the question type or create a script.

    1.  Create a script for a dynamic response by selecting the script icon ![script icon](../image/script-icon.jpg).

    2.  Update the `result.value = <null>` with the required input.

        In the script, **result.value** holds the response. The input in **result.value** must match the corresponding question type. For example, a text-type question should have a string value and while a number-type question should have an integer value.

6.  Set up a condition by selecting **Add If-then condition**.

7.  Select **+ New condition set** under **If** condition to set the condition.

    -   Add details to **If** and **Then** conditions using the condition builder. For more information, refer to [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
    -   You can set up multiple conditions within a single **If** condition by selecting **+ New condition set**. Within a single condition row, you can combine multiple conditions using **and** or **or** logical operators.
8.  Set up one or more subsequent if-then conditions by selecting **Add If-then condition**.

    -   Add details to **Otherwise if** and **Then** conditions using the condition builder. For more information, refer to [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
    -   The first condition that meets the criteria triggers the default response. Priority is determined by the order of the conditions. For instance, if you have three conditions and the first one is true, the system doesn't check the remaining two.
9.  In the **Default response is** field in the **If nothing matches** section, set the default response for situations where none of the condition sets meet the set criteria.

    ![Screen of the Automate response pop-up window, which shows the If section, Then section, and If nothing matches section.](../image/automate-response-add-condition.jpg)

10. Create a script for a dynamic response by selecting the script icon ![](../image/script-icon.jpg).

11. Update the **result.value** field with the required input.

    In the script, **result.value** holds the response. The input in **result.value** must match the corresponding question type. For example, a text-type question should have a string value and while a number-type question should have an integer value.

12. Under **Additional options**, select the **Set response as editable** option.

    -   Selecting the **Set response as editable** option enables the assessors to edit the response. If cleared, the response becomes read-only.
    -   For a question to be marked as required, the **Set response as editable** option must be selected. If **Set response as editable** is cleared, the **Required** option is automatically turned off.
13. Select **Save**.


