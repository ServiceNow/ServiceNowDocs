---
title: Create an eligibility policy template
description: Create eligibility policy templates for the Social Benefits Playbook policy forms that you use frequently.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create an eligibility policy, Configure Eligibility Rules Engine Policies, Configure Eligibility Rules Engine, Social Benefits Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create an eligibility policy template

Create eligibility policy templates for the Social Benefits Playbook policy forms that you use frequently.

## About this task

You can save some policies as templates to quick start the creation of other policies.

## Before you begin

Role required: admin

## Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

2.  Navigate to **Templates** &gt; **All Templates**.

3.  Select **New**.

4.  In the Create New Template form, fill in the fields.

<table id="table_dty_cpg_qxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the policy template.

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

</td></tr><tr><td>

Updated

</td><td>

Date and time when the policy template was updated.

</td></tr><tr><td>

Updated by

</td><td>

User who updated the policy template.

</td></tr><tr><td>

Created

</td><td>

Date and time when the policy template was created.

</td></tr></tbody>
</table>5.  Select **Save**.

    New templates are inactive by default. Select the inactive filter box on the new policy page to view the inactive template.

6.  Select the **Template Builder** tab and fill in the conditions in the Policy logic section, then select **Save**.

    For more information about the parameters and condition fields, see [Passing parameters to PaCE policies](https://www.servicenow.com/docs/access?context=pace-passing-parameters&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Policy logic condition fields](https://www.servicenow.com/docs/access?context=pace-policy-logic-fields&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).


## What to do next

Before you activate your template, you can create a policy to test the template.

1.  Navigate to **Policies** &gt; **My Policies**.
2.  Select **New**.
3.  Select **Preview** to verify the information is correct.
4.  Select **Save**.
5.  Select the template that you wish to create a policy with, then select **Create**.
6.  Fill in the fields, then select **Save**.
7.  Select the new draft of the policy and select the **Test Playground** tab to test the policy.
8.  Navigate back to **Templates** &gt; **All Templates**. Select the template that you tested, then **Activate**.

**Note:** Updating a template won’t affect policies created previously with that template.

## Activate a Pace policy template

### Before you begin

Role required: admin

### Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

2.  Select **Templates** &gt; **All Templates**.

3.  Select the desired template.

4.  Select **Activate**.

5.  On the **Activate Template** pop-up modal, select **Activate**.


