---
title: Create an eligibility policy in Grants Management using PaCE
description: Create an eligibility policy using Grants Management Eligibility Rules Engine​ to model eligibility rules that can be used to evaluate grants cases.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure Eligibility Rules Engine Policies, Configure PaCE Eligibility Framework Engine, Grants Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Create an eligibility policy in Grants Management using PaCE

Create an eligibility policy using Grants Management Eligibility Rules Engine​ to model eligibility rules that can be used to evaluate grants cases.

## About this task

Use Policy as Code Engine \(PaCE\) policies to build out the logic that will determine eligibility and grants. Policies can be saved as templates to quick-start future policy creation. You can create a policy from scratch using Policy Management, and define the logic for that policy using the Policy Builder tool. Policy logic is a set of conditions that is used for determining whether or not an applicant is eligible for one or more of the grant programs offered by your agency. You can set conditions for the policy using the condition fields.

## Before you begin

Role required: admin

## Procedure

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

The name of the policy.**Note:** The policy name must be unique, and is used as the identifier of the policy.

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
For more details, see [Manage PaCE policy versions](https://www.servicenow.com/docs/access?context=pace-policy-versions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).**Note:** You must publish a policy version to make it current before it can be used.

</td></tr><tr><td>

Version management

</td><td>

Displays previous versions of the policy. You can also create a new version of the policy.

</td></tr><tr><td>

Mappings

</td><td>

Enables you to define the grant model to which the policy is to be mapped.

</td></tr><tr><td>

Executions

</td><td>

Enables you to review the execution activity for the policy.

</td></tr></tbody>
</table>7.  Select **Policy Builder** &gt; **Record References**, then select **Add** to add variables for the policy.

8.  On the **Record Reference** form, fill in the fields.

    |Record Reference Field|Description|
    |----------------------|-----------|
    |Label| |
    |Name| |
    |Table| |

9.  To set qualifier conditions for the policy, select **New condition set** and enter the following information:

<table id="table_rfb_gpj_pwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition description

</td><td>

Case constituent is empty.

</td></tr><tr><td>

Source

</td><td>

**API variables** &gt; **Case Reference** &gt; **Constituent**

</td></tr><tr><td>

Operator

</td><td>

is empty

</td></tr><tr><td>

Value

</td><td>

Value to enter text. Select the Data picker icon to concatenate multiple text strings with multiple data pills to select a variable for the log.**Note:** If your Source is choice, you will be unable to select multiple data pills.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Decision|Non-Compliant|
    |Output type|Result|
    |Data|This case does not have a constituent.|

10. Add a dependent condition by selecting **Add else**, then fill in the fields with the following information.

    |Field|Description|
    |-----|-----------|
    |Decision|Compliant|
    |Output type|Info|
    |Data|This case has a constituent.|

11. Select **Publish**.

12. Do one of the following.

    -   To publish this eligibility policy for immediate use evaluating Grants applications:
        1.  Select **Publish**.
        2.  Select **Activate this policy** then select **Publish without testing**.
        3.  Verify that the state of the policy has changed to **Current**.

            Your eligibility policy is now published and can be used to evaluate any active grants cases. Verify the policy appears in the Policy Home by navigating to **Policy Home** in the CSM Configurable Workspace sidebar, and selecting**Policies** &gt; **All Policies**.

    -   To save this policy as a template for future use:
        1.  Select **Save as Template** &gt; **New Template**.
        2.  On the form, fill in the fields.

            |Policy Template form|Description|
            |--------------------|-----------|
            |Name|Primary Applicant|
            |Template Type|Data Source|
            |Description|Predefined data source for applicant information|

        3.  Select **Save**

            Your policy template has been created, and can be used to quick-start future policy creation. For more information on creating PaCE policy templates, see . For more information on creating a new PaCE policy from a template, see [Create a PaCE Eligibility Policy from a template](psds-config-sbp-pace-policy-from-template.md).

            .


## Result

An eligibility policy is now created, and is ready to be mapped to one of more grant models of the Grants Management. See [Map an PaCE eligibility policy to a grant model using Grants Management Eligibility Framework](psds-config-gmp-map-eligibility-policy.md) for information on how to map the published policy to a specific grant.

**Parent Topic:**[Configure Eligibility Rules Engine Policies in Grants Management](psds-config-gmp-eligibility.md)

