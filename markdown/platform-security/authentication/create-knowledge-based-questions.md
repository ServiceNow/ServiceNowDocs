---
title: Create KBA questions
description: Create knowledge-based questions that can be preconfigured as security questions to confirm the user's identity.
locale: en-US
release: yokohama
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

Define a security question to be used for user identity verification. Example: `What is your business phone number?`**Note:** Only numeric questions are allowed.

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
**Note:** You can choose **Phone Number** if specifying the phone number, otherwise choose **Others**.

</td></tr></tbody>
</table>    ![Knowledge Based Question](../images/configure-kba-questions.png "Knowledge Based Question") ![]( "Knowledge Based Question")

4.  Select **Submit**.


## Result

You’re redirected to the Knowledge Based Questions list view. Verify if your question is successfully added.

![Knowledge Based Question - list](../images/configure-kba-questions-result.png "Knowledge Based Questions - list")

