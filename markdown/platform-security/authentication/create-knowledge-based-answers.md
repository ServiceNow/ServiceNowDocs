---
title: Create KBA answers
description: Create knowledge-based answers for the preconfigured security questions to confirm the user's identity.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 3
breadcrumb: [Configure KBA, Knowledge-based authentication, Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Create KBA answers

Create knowledge-based answers for the preconfigured security questions to confirm the user's identity.

## Before you begin

Role required: auth\_factors\_admin

KBA validates answers against records in ServiceNow AI Platform tables by default. To validate against an external source such as a CRM or order management platform, select **Identification** in the Script Configuration field. External data is never imported or stored in ServiceNow AI Platform; the script handles all interaction with the external system. For the caller to be eligible for authentication, the script output must return `sys_user` table.

The User Column field determines whether an identified caller can proceed to authentication. When populated with a field that links to a system user account, the caller is eligible for authentication. When left empty or mapped incorrectly, the caller is treated as a guest — the caller can access personalized, non-sensitive information but cannot be authenticated.

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Answers**.

2.  Select **New** on the Knowledge Based Answers page.

3.  Specify the following fields on the form:

<table id="table_ucp_d5x_l3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script Configuration

</td><td>

Select the type of script-based validation. Options:

-   **None** \(validate against a ServiceNow table\)
-   **Identification** \(validate a caller’s identity via a custom script against an external system\).
 **Note:** When the Script Configuration set to **Identification**, the Answer Table, Answer Column, and User Column fields are replaced by a Script editor.

</td></tr><tr><td>

Description

</td><td>

Define a description for the answer. For example: Business Phone Number.

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr></tbody>
</table>4.  Specify the following fields for configuring internal source:

    **Note:** The following fields are available when Script Configuration is set to **None**.

<table id="table_gtp_xb1_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Answer Table

</td><td>

Select the answer table.**Note:** The selected table should have a field referenced to the `sys_user` table.

</td></tr><tr><td>

Answer Column

</td><td>

Select the answer column from the **Available** list. Example: `Business phone`.

</td></tr><tr><td>

User Column

</td><td>

Select the field that links records in the Answer Table to a system user account. For example: sys\_user.**Note:**

-   All fields from the Answer Table are displayed, but only fields that reference a system user account can be selected. If the Answer Table is `sys_user`, the `sys_id` field can also be selected.
-   When populated with a valid `sys_user` reference, the answer supports identification and authentication. When left empty, the answer supports guest identification only.
-   Whether this field is required is controlled by the `glide.auth_factors.kba.enable_user_column` property. To know more about the properties, see [System Properties](create-knowledge-based-answers.md#system-properties).


</td></tr></tbody>
</table>    ![Knowledge Based Answer - Script Configuration as None](../images/kba-answers-1.png "Knowledge Based Answer - Script Configuration: None")

5.  Specify the following fields for configuring external source:

    **Note:** The following field is available when Script Configuration is set to **Identification**.

<table id="table_zgj_dvx_l3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script

</td><td>

Define the custom script to validate the answer against an external system. Script requirements are as follows:-   The script must be scoped.
-   The system receives the caller's answer as `user_input` and must return the **table\_name** and matched record’s `sys_id` as the output.
-   For records in tables other than `sys_user`, the **table\_name** must also be returned.
-   Script execution is limited to 15 seconds by default. This is to avoid long wait times for the caller. To adjust, configure the `glide.auth_factors.kba.script_execution_time_outproperty`. To learn more see, [System Properties](create-knowledge-based-answers.md#system-properties).


</td></tr></tbody>
</table>    ![Knowledge Based Answer - Script Configuration as None](../images/kba-answers-2.png "Knowledge Based Answer - Script Configuration: Identification")

    **Note:** One question can have many answers. All answers for that question must follow the same rule:

    -   Either all answers support identification only
    -   Or all answers support identification and authentication
    You cannot have some answers that authenticate users and others that don't for the same question.

6.  Select **Submit**.


## Result

You're redirected to the Knowledge Based Answers list view. Verify if your answer is successfully added.

![Knowledge Based Answers - list](../images/kba-answers-3.png "Knowledge Based Answers - list")

The following properties control the behavior of knowledge-based authentication \(KBA\), including security question validation, answer matching, and user identification settings.

<table id="table_zyt_2xc_m3c"><thead><tr><th>

System properties

</th><th>

Description

</th><th>

Value

</th></tr></thead><tbody><tr><td>

`glide.auth_factors.kba.enable_user_column`

</td><td>

Controls whether the User Column field is mandatory when creating or updating an answer.

 **Note:** All answers mapped to the same question must follow the same pattern — either all supporting identification and authentication, or all supporting identification only. Mixing is not supported.

</td><td>

`false`

</td></tr><tr><td>

`glide.auth_factors.kba.script_execution_time_out`

</td><td>

Controls the script execution time limit in seconds for external source validation. Minimum: 1 second, Maximum: 30 seconds.

</td><td>

`15`

</td></tr></tbody>
</table>