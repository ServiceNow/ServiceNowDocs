---
title: Configure Eligibility Rules Engine Policies in Social Benefits Playbook
description: Use the Social Benefits Playbook Eligibility Rules Engine, powered by Policy as Code Engine \(PaCE\), to manage the life cycle of a policy and create, update, review, and execute policies. In the Policy Home of the CSM Configurable Workspace, you can create, remove, and update the policies used for determining eligibility for an application routed through the Social Benefits Playbook.Create an eligibility policy using Social Benefits Playbook Eligibility Rules Engine​.For a eligibility policy to be invoked correctly, it must be mapped to an existing benefit model. Map a published eligibility policy to one or more of the social benefit types that your agency offers.Update an eligibility policy in the Social Benefits Eligibility Framework Engine.Make changes to the policy logic in the Social Benefits Eligibility Framework Engine. The Policy Builder tab allows an admin to test new logic parameters through the test playground.You can edit the mapping settings that map a policy to a benefit model.Create eligibility policy templates for the Social Benefits Playbook policy forms that you use frequently.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Configure Eligibility Rules Engine, Social Benefits Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Eligibility Rules Engine Policies in Social Benefits Playbook

Use the Social Benefits Playbook Eligibility Rules Engine, powered by Policy as Code Engine \(PaCE\), to manage the life cycle of a policy and create, update, review, and execute policies. In the Policy Home of the CSM Configurable Workspace, you can create, remove, and update the policies used for determining eligibility for an application routed through the Social Benefits Playbook.

You can define and manage your eligibility rules engine policies in a single management console, the Policy Management Home in CSM Configurable Workspace.

![Admin view of Policy Home on CSM Configurable Workspace](../image/psds_sbp_policy_home.png)

Here, you can:

-   Create policies.
-   Review existing policies.
-   Assess and implement changes to each policy.
-   Determine if a policy should be used as the template for another policy.
-   Understand why a policy may not be working as expected.

You can create any number of policies, which can be updated as required.

## Create an eligibility policy using the Social Benefits Playbook Policy as Code Engine \(PaCE\) Eligibility Rules Engine​

Create an eligibility policy using Social Benefits Playbook Eligibility Rules Engine​.

### About this task

Use Policy as Code Engine \(PaCE\) policies to build out the logic that will determine eligibility and benefits. Policies can be saved as templates to quick-start policy creation. You can create a policy from scratch using Policy Management, and define the logic for that policy using the Policy Builder tool. Policy logic is a set of conditions that is used for determining whether or not an applicant is eligible for one or more of the social benefit programs offered by your agency. You can set conditions for the policy using the condition fields.

### Before you begin

Role required: admin

### Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

2.  Select **All Policies** &gt; **New**.

3.  Select **New blank policy** to start from a blank policy, or select from the existing policy templates.

4.  Select **Create**.

5.  On the **Create New Policy** form, fill in the fields.

<table id="table_mc2_q1m_zwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

The policy name.**Note:** The policy name must be unique, and is used as the identifier of the policy.

</td></tr><tr><td>

Category

</td><td>

Enables you to group and manage policies more efficiently.

</td></tr><tr><td>

Created

</td><td>

Date and time when the policy was created. Auto-populated.

</td></tr><tr><td>

Updated

</td><td>

Date and time when the policy was updated. Auto-populated.

</td></tr><tr><td>

Description

</td><td>

Additional details for this policy.

</td></tr></tbody>
</table>6.  Select **Save**.

    The newly created policy contains the following tabs:

<table id="table_yck_b1m_zwb"><thead><tr><th>

Tab name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

Displays the details of the policy, including policy name, category, date created, and a description.

</td></tr><tr><td>

Policy builder

</td><td>

When you create a policy, a draft policy version is created, and must be published before it is current and can be used. Each policy version contains version metadata, a policy script, and variable input definitions, all of which can be modified. Under the **Policy builder** tab, you can:-   Edit a policy version.

**Note:** Published policies cannot be edited. To edit a published policy, select **Create a copy**.

-   View version details
-   Create a new version
-   Switch from low-code to the code editor
-   Save the policy as a template
-   Compare versions
-   Duplicate policy versions
For more details, see [Manage PaCE policy versions](https://www.servicenow.com/docs/access?context=pace-policy-versions&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).**Note:** You must publish a policy version to make it current before it can be used.

</td></tr><tr><td>

Version management

</td><td>

Displays previous versions of the policy. You can also create a new version of the policy.

</td></tr><tr><td>

Mappings

</td><td>

Enables you to define the benefit model to which the policy is to be mapped.

</td></tr><tr><td>

Executions

</td><td>

Enables you to review the execution activity for the policy.

</td></tr></tbody>
</table>7.  Set conditions for the policy using the condition fields.

8.  Add a condition set by selecting **New condition set**.

<table id="table_rfb_gpj_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition description

</td><td>

Description of the field.

</td></tr><tr><td>

Source

</td><td>

Variable you want to source for the condition.

</td></tr><tr><td>

Operator

</td><td>

List of operators to filter the source for the condition. The list changes depending on the source selected.

</td></tr><tr><td>

Value

</td><td>

Value to enter text. Select the Data picker icon to concatenate multiple text strings with multiple data pills to select a variable for the log.**Note:** If your Source is choice, you will be unable to select multiple data pills.

</td></tr></tbody>
</table>9.  Add a dependent condition by selecting **or** or **and** next to the condition.

    |Field|Description|
    |-----|-----------|
    |Decision|Decision to determine if the policy is **Compliant** or **Non-compliant**.|
    |Log level|Level of the log.|
    |Log message|Log message field to enter text or select the Data picker icon to concatenate multiple text strings with multiple data pills to select a variable for the log.|
    |Output type|Output type of the log. You can select the plus icon to add multiple output types or the minus icon to delete the output type.|
    |Data|Data field to enter text. Select the Data picker icon to concatenate multiple text strings with multiple data pills to select a variable for the log.|

10. Select **Publish**.


### Result

An eligibility policy is now created, and is ready to be mapped to one of more benefits models of the Social Benefits Playbook. See [Map an PaCE eligibility policy to a benefit model using Social Benefits Playbook Eligibility Framework](psds-sbp-ef-configure-eligibility.md#) for information on how to map the published policy to a specific benefit.

## Map an PaCE eligibility policy to a benefit model using Social Benefits Playbook Eligibility Framework

For a eligibility policy to be invoked correctly, it must be mapped to an existing benefit model. Map a published eligibility policy to one or more of the social benefit types that your agency offers.

### Before you begin

Role required: admin

### Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

2.  Select **Mappings** &gt; **Static Mappings** &gt; **New**.

3.  Select the social benefit model that you wish to map to from the dropdown.

    Objects available for mapping are displayed.

4.  Select the policy that you wish to map the social benefit model to.


### Result

The newly created mapping is valid and active, and the mapping input is added to the list of policy mappings.

## Update an eligibility policy in the Social Benefits Eligibility Framework Engine

Update an eligibility policy in the Social Benefits Eligibility Framework Engine.

### Before you begin

Role required: admin

### Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home**.

2.  Select **All Policies**, and select the policy name.

3.  Do one of the following, depending on what information you want to update.

<table id="choicetable_swn_gw1_3bc"><thead><tr><th align="left" id="d60272e822">

Select...

</th><th align="left" id="d60272e825">

To...

</th></tr></thead><tbody><tr><td id="d60272e831">

**Select the Details tab.**

</td><td>

Edit details such as the policy name, category, date, and description.

</td></tr><tr><td id="d60272e840">

**Select the Policy Builder tab.**

</td><td>

Make changes to the policy logic, and switch between versions to take various actions at the version level. **Note:** Published versions of policies cannot be updated. To make changes to the logic of an existing policy, select **Create a copy** to create a new version of the existing policy that can be updated accordingly.

</td></tr><tr><td id="d60272e854">

**Select the Version Management tab.**

</td><td>

Manage different versions of a policy.

</td></tr><tr><td id="d60272e863">

**Select the Mappings tab.**

</td><td>

Update or review the benefits to which the given policy is mapped.

</td></tr><tr><td id="d60272e873">

**Select the Executions tab.**

</td><td>

Update or review the execution activity for the given policy.

</td></tr></tbody>
</table>
### Update a policy logic in the Social Benefits Eligibility Framework Engine

Make changes to the policy logic in the Social Benefits Eligibility Framework Engine. The Policy Builder tab allows an admin to test new logic parameters through the test playground.

#### Before you begin

Role required: admin

#### Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home** and select **All Policies**.

2.  Select the policy name, and select the **Policy Builder** tab.

3.  Select **Create a copy** to create a new version of the existing policy that can be updated accordingly.

    A new draft is created that changes can be appended to.

4.  Update the value or condition you wish to change, or add a new piece of logic to the eligibility policy.

5.  Select the Test Playground icon ![test playground icon](../image/test-playground-icon.png) in the contextual side panel to test the policy.

6.  Select the parameters of the policy logic and select **Run Test**.

7.  Review the Output log to ensure there are no issues or errors introduced by the new parameters.

8.  Select **Publish**.

9.  Select **Publish** again, if prompted.

    The previous version of the policy is archived, and the newly published version is made the current production version.


### Update policy mapping in the Social Benefits Eligibility Framework Engine

You can edit the mapping settings that map a policy to a benefit model.

#### Before you begin

Role required: admin

#### Procedure

1.  From the CSM Configurable Workspace sidebar, navigate to the **Policy Home** and select **All Policies**.

2.  Select the policy name for the policy that you want to update, and select the **Mappings** tab.

3.  Select the Mapping ID in the Input field.

4.  In the displayed mapping input form, edit the desired details, and select **Save**.

5.  Select **Add** to add a new benefit model to the list of mappings for the policy.


## Create an eligibility policy template

Create eligibility policy templates for the Social Benefits Playbook policy forms that you use frequently.

### Before you begin

Role required: admin

### Procedure

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

    For more information about the parameters and condition fields, see [Passing parameters to PaCE policies](https://www.servicenow.com/docs/access?context=pace-passing-parameters&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and [Policy logic condition fields](https://www.servicenow.com/docs/access?context=pace-policy-logic-fields&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


### What to do next

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

