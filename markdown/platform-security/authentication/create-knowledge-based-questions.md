---
title: Create KBA questions
description: Create knowledge-based questions that can be preconfigured as security questions to confirm the user's identity.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure KBA, Knowledge-based authentication, Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Create KBA questions

Create knowledge-based questions that can be preconfigured as security questions to confirm the user's identity.

## Before you begin

Role required: auth\_factors\_admin

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Questions**.

2.  Select **New** on the Knowledge Based Questions page.

3.  Specify the following fields on the form:

<table id="table_gtp_xb1_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Question

</td><td>

Define a security question to be used for user identity verification. Example: `What is your business phone number?`

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr><tr><td>

Keyword

</td><td>

Enter the primary keyword that best describes the question. Example: `business_phone`.

</td></tr><tr><td>

Category

</td><td>

Select the category. Options:-   Others
-   Phone Number
**Note:** Selecting **Phone Number** enables partial matching against the stored phone number, for example, matching even if the area code is not included.

</td></tr><tr><td>

Input Type

</td><td>

Select how the user provides their answer. Options: -   **Text** \(user enters a numeric response via phone keypad\)
-   **Voice** \(user speaks their response\).


</td></tr></tbody>
</table>4.  Select the Input Type:

    1.  Option A: Input Type as **Text**.

        ![Knowledge Based Question - Text](../images/kba-question-1.png "Knowledge Based Question - Text")

        **Note:** If Input Type is set to **Text**, no additional fields are required.

    2.  Input Type as **Voice**.

    ![Knowledge Based Question - Text](../images/kba-question-2.png "Knowledge Based Question - Voice")

    **Note:** The following fields available as a mandatory field when Input Type is set to **Voice**.

<table id="table_nvb_m4x_l3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Input Format Description

</td><td>

Describe the expected format and structure of the spoken response. For example: 5-character alphanumeric employee ID starting with the letter E.

</td></tr><tr><td>

Input Format Example

</td><td>

Specify comma-separated examples of valid spoken responses. For example: E372B, E481K, E529D.

</td></tr><tr><td>

Input Validation Pattern

</td><td>

Specify a regular expression pattern to validate the spoken response against the expected format. For example: ^E\[0-9\]\{3\}\[A-Z\]$.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

You’re redirected to the Knowledge Based Questions list view. Verify if your question is successfully added.

![Knowledge Based Question - list](../images/kba-question-3.png "Knowledge Based Questions - list")

