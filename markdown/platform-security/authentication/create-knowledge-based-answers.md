---
title: Create KBA answers
description: Create knowledge-based answers for the preconfigured security questions to confirm the user's identity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/authentication/create-knowledge-based-answers.html
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure KBA, Knowledge-based authentication, Configure authentication factors for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Create KBA answers

Create knowledge-based answers for the preconfigured security questions to confirm the user's identity.

## Before you begin

Role required: auth\_factors\_admin

KBA validates answers against records in ServiceNow AI Platform tables by default. To  validate against  an external source such as a CRM or order management platform, select Identification or Authentication in the Script Configuration field. External data is never imported or stored in ServiceNow AI Platform.

The User Column field determines whether an identified caller can proceed to authentication. When populated with a field that links to a system user account, the caller is eligible for authentication. When left empty or mapped incorrectly, the caller is treated as a guest — the caller can access personalized, non-sensitive information but can't be authenticated.

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

Select the type of script-based validation. Options: -   **None**: Validate the caller's answer against a ServiceNow AI Platform table.
-   **Identification**: Validate a caller's identity via a custom script against an external system.
-   **Authentication**: Validate a caller's authentication via a custom script against an external system.
**Note:** When Script Configuration is set to **Identification** or **Authentication**, the Answer Table, Answer Column, and User Column fields are replaced by a script editor.

</td></tr><tr><td>

Description

</td><td>

Define a description for the answer. For example: Business Phone Number.

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr></tbody>
</table>4.  Specify fields based on the Script Configuration selected:

    1.  Script Configuration as **None**: Validate against a ServiceNow AI Platform table:

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

Select the field that links records in the Answer Table to a system user account. For example: sys\_user.All fields of type reference from the Answer Table are displayed and can be selected.

When populated with a valid `sys_user` reference, the answer supports identification and authentication. When left empty, the answer supports guest identification only and the caller can't be authenticated.

Whether this field is required is controlled by the property. To know more, see [System Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-knowledge-based-answers.md).

</td></tr></tbody>
</table>        \[Omitted image "kba-answers-1.png"\] Alt text: Knowledge Based Answer - Script Configuration as None

    2.  Script Configuration as **Identification**: Validate against an external system during identification:

        **Note:** KBA Answers - **Script Configuration**: Works for only users with `snc_external`role users.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script

</td><td>

Define the custom script to validate the caller's answer against an external system and return the location of the matched ServiceNow AI Platform record.

 Script input: `user_input`, the caller's answer.

 Script output:

 -   `table_name`: The ServiceNow AI Platform table where the matched record is located.
-   `sys_id`: The `sys_id` of the matched record within the specified table.
 For script execution time limits, see [System Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-knowledge-based-answers.md).

</td></tr></tbody>
</table>        \[Omitted image "kba-answers-1-2.png"\] Alt text: Script Configuration as Identification

    3.  Script Configuration as **Authentication**: Validate against an external system during authentication:

        **Note:** KBA Answers - **Script Configuration**: Works for only users with `snc_external`role users.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Script

</td><td>

Define the custom script to verify the caller's answer against an external system and return a pass or fail result.

 Script input:

 -   `user_id`: The sys\_id of the user being authenticated.
-   `user_input`: The caller's answer.
-   `kba_session_context`: a JSON object containing questions presented to the caller and the answers they provided, captured across identification and authentication steps in the current session. Only questions configured with a scripted answer are included. This allows the script to reference prior responses when validating the current answer — for example, to cross-check answers or apply multi-field logic. Example:

    ```
{ 
"employee_id":"EMP12345", 

"date_of_birth":"1Jan2026" 
} 
    ```

 Script output: `kb_auth_result`, set to `true` if the answer matches, `false` if it does not.

 For script execution time limits, see [System Properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/authentication/create-knowledge-based-answers.md).

</td></tr></tbody>
</table>        \[Omitted image "kba-answers-1-1.png"\] Alt text: External source fields \(Authentication\)

        **Note:**

        -   If a question uses scripted answers, only one answer is permitted.
        -   If the answers are non-scripted, then multiple answers are allowed for that question.
        However, for any given question, all associated answers must consistently follow the same approach: either all answers must support identification only, or all must support both identification and authentication. You can't mix answer types for the same question.

5.  Select **Submit**.


## Result

You're redirected to the Knowledge Based Answers list view. Verify if your answer is successfully added.

\[Omitted image "kba-answers-3.png"\] Alt text: Knowledge Based Answers - list

The following properties control the behavior of knowledge-based authentication \(KBA\), including security question validation, answer matching, and user identification settings.

<table id="table_zyt_2xc_m3c"><thead><tr><th>

System properties

</th><th>

Description

</th><th>

Default Value

</th></tr></thead><tbody><tr><td>

`glide.auth_factors.kba.enable_user_column`

</td><td>

Controls whether the User Column field is mandatory when creating or updating an answer.

 **Note:** All answers mapped to the same question must follow the same pattern — either all supporting identification and authentication, or all supporting identification only.

</td><td>

`true`

</td></tr><tr><td>

`glide.auth_factors.kba.script_execution_time_out`

</td><td>

Controls the script execution time limit in seconds for external source validation. Minimum: 1 second, Maximum: 30 seconds.

</td><td>

`15`

</td></tr></tbody>
</table>