---
title: Verification types in the base system
description: Use a verification type in the base system as a template to design a custom verification.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Verification types in the base system

Use a verification type in the base system as a template to design a custom verification.

<table id="table_ypq_fnz_f1b"><thead><tr><th>

Verification type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Personal Data Confirmation

</td><td>

Verifies user identity using data from the User \[sys\_user\] table. The user data is displayed to a service desk agent. The agent verifies the data. Enrollment is not required for this type.

Recommended for service desk-assisted processes.**Note:** The Password Reset Windows Application does not support the Personal Data Confirmation Verification type.

 See [Personal data identification types and confirmation type verifications](../concept/c_PersonalDataAndPDConfirmVerifs.md).

</td></tr><tr><td>

Personal Data

</td><td>

Verifies user identity using data from the User \[sys\_user\] table. The user is required to answer questions. Enrollment is not required for this type.

 **Note:** The Password Reset Windows Application allows you to define and use multiple verifications of the Personal Data type.

See [Personal data identification types and confirmation type verifications](../concept/c_PersonalDataAndPDConfirmVerifs.md).

</td></tr><tr><td>

Email Code

</td><td>

When a user requests password reset, the system sends a verification code to the email address in the user profile or to an email address that the user authorized during enrollment. To verify identity, the user then submits the code on the Password Reset **Verify** page. **Note:** The Password Reset Windows Application allows you to define and use multiple verifications of the Email Code type.

See [Personal data identification types and confirmation type verifications](../concept/c_PersonalDataAndPDConfirmVerifs.md).

</td></tr><tr><td>

Google Authenticator

</td><td>

While requesting password reset, the user reads a code from the Google Authenticator app on a device that the user has paired. To verify identity, the user then submits the code on the Password Reset **Verify** page. **Note:** The Password Reset and Password Reset Windows Application support only a single verification of the SMS Code type.

</td></tr><tr><td>

Security Questions

</td><td>

Verifies user identity by presenting personal security questions that the user must answer correctly. **Note:** The Password Reset and Password Reset Windows Application support only a single verification of the Security Questions type.

 See [Add a custom question to the Security Questions verification](../task/t_CreateQAVerificationQs.md).

</td></tr><tr><td>

SMS Code

</td><td>

When a user requests password reset, the system sends a code to an SMS-capable device that the user has authorized. To verify identity, the user then enters the code on the Password Reset web page. **Note:** The Password Reset and Password Reset Windows Application support only a single verification of the SMS Code type.

See [SMS Code Verification type for Password Reset](../concept/c_SMSCodeTypeVerifications.md).

</td></tr><tr><td>

Mock

</td><td>

Not a functional identity verification. Demonstrates how to add a verification type in a Password Reset process. **Note:** The Password Reset Windows Application does not support the Mock verification type.

 -   The enrollment UI macro for this verification gets the user input and returns the entered value in the enrollment processor.
-   The Password Reset UI macro for this verification gets input from the user and returns the entered value through the verification processor.

</td></tr></tbody>
</table>**Related topics**  


[Create a custom Password Reset verification](../task/t_CreatePWRVerFromVerType.md)

[Create a custom Password Reset verification type](../task/create-verification-type.md)

