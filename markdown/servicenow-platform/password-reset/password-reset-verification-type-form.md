---
title: Password Reset Verification Type form
description: Description of the fields on the Password Reset Verification Type form.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset Verification Type form

Description of the fields on the Password Reset Verification Type form.

<table id="table_p5w_mgz_h1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enrollment check

</td><td>

Script that determines whether a user is enrolled for verification. Automatic enrollment requires an enrollment check. If no script is specified when **Automatic Enrollment** is selected, a default script is provided.

</td></tr><tr><td>

Automatic enrollment

</td><td>

Select the check box to auto-enroll users. If **Automatic enrollment** is not selected, then you must provide an enrollment UI macro and enrollment processor script.For SMS and email verification, if the **Automatic enrollment** check box is selected and the user's mobile number and email address already appear in the sys\_user table record, the user is enrolled for the corresponding verification.

 If the user’s mobile number and email address aren’t mentioned in the sys\_user table, the user is not enrolled.

 **Note:** If the **Automatic enrollment** check box isn’t selected, then even if the user's mobile number and email address appear in the sys\_user table record, the user is not enrolled. The user must enroll manually by using the password reset enrollment process.

</td></tr><tr><td>

Enrollment UI

</td><td>

Enrollment UI macro that provides the UI for the enrollment.

</td></tr><tr><td>

Enrollment processor

</td><td>

Enrollment processor script that processes the enrollment.

</td></tr><tr><td>

Verification UI

</td><td>

Verification UI macro that provides the UI for the verification.

</td></tr><tr><td>

Verification processor

</td><td>

Verification processor script \(extension scripts\) that processes the verification.

</td></tr></tbody>
</table>**Related topics**  


[Create a custom Password Reset verification type](../task/create-verification-type.md)

