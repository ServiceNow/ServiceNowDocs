---
title: Create KBA questions
description: Create knowledge-based questions to use for caller identification and authentication in AI voice agent interactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/create-knowledge-based-questions.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure KBA, Knowledge-based authentication, Authentication factor configuration for AI voice agents, Authentication factors, Authentication, Access Management]
---

# Create KBA questions

Create knowledge-based questions to use for caller identification and authentication in AI voice agent interactions.

## Before you begin

Role required: auth\_factors\_admin

-   **Default questions**

    A default set of KBA questions is available to all AI voice assistants in AI Voice Assistant Designer. You can use these questions as-is or edit them.

    |Question|Default answer source|Type|Category|
    |--------|---------------------|----|--------|
    |Phone Number|sys\_user.mobile\_phone|Identification|Phone, triggers Automatic Number Identification \(ANI\)|
    |Employee ID|sys\_user.employee\_number|Identification or Authentication|Others|
    |Email|sys\_user.email|Identification or Authentication|Others|
    |Manager|sys\_user.manager|Identification or Authentication|Others|
    |Zip Code|sys\_user.zip|Identification or Authentication|Others|


## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Questions**.

2.  Select **New** on the Knowledge Based Questions page.

3.  Specify the following fields on the form.

<table id="table_gtp_xb1_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Security question to use for user identity verification. Example: `What is your business phone number?`

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr><tr><td>

Keyword

</td><td>

Primary keyword that best describes the question. Example: `business_phone`.

</td></tr><tr><td>

Category

</td><td>

Category of the question. Options:-   Phone Number: Enables partial phone number matching and makes the caller's ANI \(automatic number identification\) available by default for identification.
-   Others: Standard matching; ANI is not used.
**Note:** Phone Number category can't be used for authentication.

</td></tr><tr><td>

Channel

</td><td>

Channel for which the question is configured. Currently, only **Voice** is supported.

</td></tr><tr><td>

Input Type

</td><td>

How the user provides their answer. Options: -   **Text**: The caller enters a response by using the phone keypad.
-   **Voice**: The callers speak their response.


</td></tr><tr><td>

Type

</td><td>

Availability of the question for use. Options: -   **Identification**: The question is available for identification configuration only.
-   **Authentication**: The question is available for authentication configuration only.
-   **Identification or Authentication**: The question is available for both.


</td></tr></tbody>
</table>4.  Select the Input Type:

    1.  Input Type as **Text**: No additional fields are required.

        \[Omitted image "kba-question-1.png"\] Alt text: Knowledge Based Question - Text

        **Note:** If Input Type is set to **Text**, no additional fields are required.

    2.  Input Type as **Voice**: Specify the following additional fields.

<table id="table_nvb_m4x_l3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input Format Description

</td><td>

Expected format and structure of the spoken response. For example: `5-character alphanumeric employee ID starting with the letter E.`

</td></tr><tr><td>

Input Format Example

</td><td>

Comma-separated examples of valid spoken responses. For example: `E372B, E481K, E529D.`

</td></tr><tr><td>

Input Validation Pattern

</td><td>

Regular expression pattern that validates the spoken response against the expected format. For example: `^E[0-9]{3}[A-Z]$`.

</td></tr></tbody>
</table>    \[Omitted image "kba-question-2.png"\] Alt text: Knowledge Based Question - Voice

5.  Select **Submit**.


## Result

You’re redirected to the Knowledge Based Questions list view. Verify if your question is successfully added.

\[Omitted image "kba-question-3.png"\] Alt text: Knowledge Based Question - list

