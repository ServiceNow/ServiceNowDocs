---
title: Create KBA answers
description: Create knowledge-based answers for the preconfigured security questions to confirm the user's identity.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure KBA, Knowledge-based authentication, Configure authentication factors, Authentication factors, Authentication, Access Management]
---

# Create KBA answers

Create knowledge-based answers for the preconfigured security questions to confirm the user's identity.

## Before you begin

Role required: auth\_factors\_admin

## Procedure

1.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Answers**.

2.  Select **New** on the Knowledge Based Answers page.

3.  Specify the following fields on the form:

<table id="table_gtp_xb1_jhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Define a description for the answer. Example: `Business Phone Number`.

</td></tr><tr><td>

Application

</td><td>

Global application scope is selected by default.

</td></tr><tr><td>

Answer Table

</td><td>

Select the answer table.**Note:** The selected table should have a field referenced to the `sys_user` table.

</td></tr><tr><td>

User Column

</td><td>

Select the field.**Note:** The User Column must reference the `sys_user` table. Example: **Sys ID**.

</td></tr><tr><td>

Answer Column

</td><td>

Select the answer column from the **Available** list. Example: `Business phone`.

</td></tr></tbody>
</table>    ![Knowledge Based Answer](../images/configure-kba-answer.png "Knowledge Based Answer")

4.  Select **Submit**.


## Result

You're redirected to the Knowledge Based Answers list view. Verify if your answer is successfully added.

![Knowledge Based Answer - list](../images/configure-kba-answer-result.png "Knowledge Based Answers - list")

