---
title: Create a guidance in the Core UI
description: Create a guidance in the Core UI so that you can link the guidance to the guidance node of a decision tree. For example, your agent may attach a knowledge article or propose a solution to a customer to help resolve an issue.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Configuring guidances and decision trees, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a guidance in the Core UI

Create a guidance in the Core UI so that you can link the guidance to the guidance node of a decision tree. For example, your agent may attach a knowledge article or propose a solution to a customer to help resolve an issue.

## Before you begin

Role required: sn\_gd\_guidance.guidance\_manager

## About this task

The preview information appears on the Recommended Actions card in the contextual side panel. The preview experience is applicable only for Recommended Actions, where agents can see previews of recommendations before launching them.

Playbooks don’t have a preview experience because decision trees are embedded and considered launched already in playbooks.

## Procedure

1.  Navigate to **All** &gt; **Guided Decisions** &gt; **Guidances**.

2.  Create a guidance.

    1.  Select **New** in the Guidances list.

    2.  On the form, fill in the fields.

<table id="table_pkc_2xq_52c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the guidance.

</td></tr><tr><td>

Description

</td><td>

Brief description of the guidance.

</td></tr><tr><td>

Action available to multiple users

</td><td>

Makes the guidance available to multiple agents working on the case.When this option isn’t selected, only one agent can work on any guidance. When the first agent works on the guidance and the state is In-progress, Completed, or Error, the other agents can't see this guidance.

</td></tr><tr><td>

Allow users to re-run the guidance

</td><td>

Enables agents to go back to the previous node, edit the previous nodes, or re-execute the guidance in the runtime experience of a decision tree.

</td></tr><tr><td>

Hide completed guidance

</td><td>

Hides the guidance recommended for a case resolution.

In other words, the completed guidance in the View my response section of a Decision Tree is not displayed for the agent.

**Note:** This field is visible only when the Guided Decision Experience plugin is installed. You may need to configure the form to add this field.

</td></tr></tbody>
</table>    3.  Select **Submit**.

3.  Open the guidance that you want to update.

4.  Create one or more inputs for the guidance.

    Inputs are the variables or information that the system needs to perform the guidance. You can use inputs in multiple places such as the guidance preview experience and the guidance actions.

    1.  In the Guidance Input tab, select **New**.

    2.  On the form, fill in the fields.

<table id="table_gzc_lc3_q2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Field type of the input.Depending on the field type that you select, you might need to configure additional settings. For example, if you select Reference as the field type, you need to select a reference table.

</td></tr><tr><td>

Label

</td><td>

Name for the guidance input.

</td></tr><tr><td>

Column name

</td><td>

 

</td></tr><tr><td>

Is form field

</td><td>

If the guidance input requires an action by the agent, such as adding information to a field, select the **Is form field** check box.

</td></tr><tr><td>

Order

</td><td>

Sequence in which the guidance input is displayed when more than one guidance input is defined.

</td></tr><tr><td>

Choice List Specification

</td><td>

Choices are:-   Dropdown without --None-- \(must specify a default value\)
-   None
-   Dropdown with --None--

None is the default value.

-   Suggestion
This tab appears when you select a value in the **Type** field.

</td></tr><tr><td>

Default value

</td><td>

Specifies the default value of the field for any new record. Ensure that this value uses the correct field type. For example, an integer field uses a default value of 2 but cannot use a default value of two.

</td></tr></tbody>
</table>    3.  Select **Submit**.

5.  Create one or more outputs for the guidance.

    Outputs are the desired result of the guidance action. For example, if a guidance action creates a case task, the output of that action can return a reference to the case task that was created.

    1.  In the Guidance Output tab, select **New**.

    2.  On the form, fill in the fields.

<table id="table_krb_sn3_q2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Field type of the output.Depending on the field type that you select, you might need to configure additional settings. For example, if you select Reference as the field type, you need to select a reference table.

</td></tr><tr><td>

Label

</td><td>

Defines a unique label for the guidance output. The label appears on list headers and form fields for the output.

</td></tr><tr><td>

Column name

</td><td>

Defines the field name of the column. When you create a new field, this name is populated automatically based on the label.

</td></tr><tr><td>

Order

</td><td>

Sequence in which the guidance output is displayed when more than one guidance outputs is defined.

</td></tr><tr><td>

Default value

</td><td>

Specifies the default value of the field for any new record. Ensure that this value uses the correct field type. For example, an integer field uses a default value of 2 but cannot use a default value of two.

</td></tr></tbody>
</table>    3.  Select **Submit**.

6.  Configure the preview experience.

    1.  Select the **Preview Experience** tab.

    2.  In the **Preview Title** field, add a title for the guidance preview as either static text, dynamic content \(field values from guidance inputs\), or a combination of static text and dynamic content.

        -   To enter static text, type the text into the field.
        -   To enter dynamic content, select the Pill-picker icon \(![Pill-picker icon](../image/icon-pill-picker.png)\) next to the field and select a guidance input from the list.

            You can drill down to find the specific input you want.![Guidance input details for a predicted knowledge base article that references a user table with fields showing the published date, rating, article retiring date, roles, and short description.](../image/ra-csm-guidance-preview-title.png)

        This field can contain static text, dynamic content, or a combination of static text and dynamic content. To select dynamic content as a field value:

        1.  Select the Pill-picker icon \(![Pill-picker icon](../image/icon-pill-picker.png)\) next to the **Preview Title** field.
        2.  Select a guidance input from the list. You can drill down to another level to find the input you want.

            ![Guidance input selected is predicted knowledge base article that references to a user table with fields published date, rating, article retiring date, roles and short description.](../image/ra-csm-guidance-preview-title.png)

    3.  In the **Fields To Display** field, select fields to display in the guidance preview.

    4.  In the **Message** field, create a message for the guidance preview.

        You can use the tools available in the rich text editor to create and format the message. This field can include text and HTML content like images, videos, and links.

7.  Select **Submit**.


## What to do next

[Configure guidance detail experience](configure-guidance-preview-detail-experiences-ga.md) for Recommended Actions cards.

