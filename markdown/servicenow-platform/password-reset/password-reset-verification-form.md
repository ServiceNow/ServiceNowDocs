---
title: Password Reset Verification form
description: Description of the fields on the Password Reset Verification form.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset Verification form

Description of the fields on the Password Reset Verification form.

<table id="table_wrf_xnb_pp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Create verifications based on one of the verification types in the base system. Password Reset supports the following types. You can create multiple instances of any type.

 -   Personal Data Confirmation Verification
-   Personal Data Verification
-   Security Question Verification
-   SMS Code Verification

 The Password Reset Windows Application supports the following types:

-   Personal Data Verification. You can create only a single instance.
-   Security Question Verification. You can create multiple instances.
-   SMS Code Verification. You can create only a single instance.

</td></tr><tr><td>

Order

</td><td>

Position of the verification as it appears on the Enrollment form and Password Reset form.

</td></tr><tr><td>

Password Reset Verification Parameters

</td><td>

Parameters used by a verification to configure specific behaviors, like number of questions required to enroll, request expiration time, and columns used. Set parameters for any behavior that should be different from the value that is specified in the Password Reset properties. The available parameters are described separately for each verification type.

</td></tr></tbody>
</table>**Related topics**  


[Create a custom Password Reset verification](../task/t_CreatePWRVerFromVerType.md)

