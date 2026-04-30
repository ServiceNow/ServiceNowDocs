---
title: Create a PaCE policy template
description: Create PaCE templates for the PaCE policy forms that you use frequently.
locale: en-US
release: xanadu
product: Policy as Code Engine \(PaCE\)
classification: policy-as-code-engine-pace
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage PaCE policies, Administer PaCE policies, Policy as Code Engine \(PaCE\), Extend ServiceNow AI Platform capabilities]
---

# Create a PaCE policy template

Create PaCE templates for the PaCE policy forms that you use frequently.

## Before you begin

Role required: sn\_pace.code\_editor

## Procedure

1.  Navigate to **Templates** &gt; **All Templates**.

2.  Select **New**.

3.  In the Create New Template form, fill in the fields.

<table id="table_dty_cpg_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy template.

</td></tr><tr><td>

Document type

</td><td>

Select a document type for the table of items for the template to be applied to.

</td></tr><tr><td>

Template type

</td><td>

Template type organized by category. Template types enable you to select a category, if you have multiple types of policy templates. You can create a template type by following these steps:1.  Navigate to **Templates** &gt; **Template Type**.
2.  Select **New**.
3.  Fill in the **Name** and **Description** field.
4.  Select **Save**.
The type can be selected from the **Template type** field.

</td></tr><tr><td>

Description

</td><td>

Additional details for this template.

</td></tr><tr><td>

Is low code

</td><td>

Select this check box if the policy template will be written in low-code.**Note:** You can switch to the code editor from low-code when you create the conditions, but you’ll be unable to switch back to low-code.

</td></tr></tbody>
</table>    ![Create New Template form.](../image/pace-create-template-2.jpg)

4.  Select **Save**.

    By default, when you create a template it’s inactive and it will be filtered out on the New policy page. You can select the inactive filter box on the New policy page to see the inactive template.

5.  Select the **Template Builder** tab and fill in the conditions in the Policy logic section, then **Save**.

    For more information about the parameters and condition fields, see the [Passing parameters to PaCE policies](../concept/pace-passing-parameters.md) and [Policy logic condition fields](../reference/pace-policy-logic-fields.md) topic.


## What to do next

Before you activate your template, you can create a policy to test the template.

1.  Navigate to **Policies** &gt; **My Policies**.
2.  Select **New**.
3.  Select **Preview** on the template that you created to see if the information is correct.
4.  Select **Save**.
5.  Select the template that you want to create a policy with, then **Create**.
6.  Fill in the fields, then select **Save**.
7.  Select the new draft of the policy and select the **Test Playground** tab to test the policy.
8.  When you're finished, navigate back to **Templates** &gt; **All Templates**. Select the template that you tested, then **Activate**.

If you make any updates to a template, it won’t affect previous policies that you created using the template.

