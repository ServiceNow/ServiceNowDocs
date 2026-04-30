---
title: Personal data identification types and confirmation type verifications
description: Personal data verifications allow users to verify their identity by providing answers to questions that are generated from personal information stored in the User table \[sys\_user\].
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Password Reset verifications, Configure your Password Reset process, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Personal data identification types and confirmation type verifications

Personal data verifications allow users to verify their identity by providing answers to questions that are generated from personal information stored in the User table `[sys_user]`.

## User experience

For an example of how a user might enroll for Personal data verification, see [Enroll for the Password Reset program using questions and answers](../task/t_EnrollUsingASecurityQuestion.md).

## Personal data identification types

The Password Reset application provides the email and username identification types. You can use either type as provided or as a model to create a custom identification type.

|Name|Description|
|----|-----------|
|Email Identification|Identifies users by their email addresses.|
|Username Identification|Identifies users by their user names.|

## Personal data confirmation verifications

-   **Personal data verification:** If users are associated with a Password Reset process that uses a personal data verification, the users are typically not required to enroll for Password Reset.
-   **Personal data confirmation verifications** allow employees with the password\_reset\_service\_desk role to access personal data from the sys\_user table when assisting a user with a password reset request.

To configure personal data and personal data confirmation verifications, you specify parameters as name/value pairs that correspond to a particular piece of user information. For example, to verify users by their email address:

1.  Set the **label** parameter \(the text that the end user should see\) to Email \(that is, `label=Email`\).
2.  Set the **column** parameter \(the column in the table that holds the verification data\) to email \(that is, `column=email`\).

**Note:** You can use only one set of name/value pair parameters per verification. Additional parameters are ignored.

To use multiple pieces of personal information for user verification, create more personal data or personal data confirmation verifications and add the verifications to the related Password Reset process.

## Personal data and personal data confirmation type verifications

<table id="table_jjf_xwb_pp"><thead><tr><th>

Parameter Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

label

</td><td>

Text to display as a label for the field that the user fills in during the password reset request.Data Type: string

 Default Value: n/a

</td></tr><tr><td>

column

</td><td>

Column of the sys\_user table that provides the data that is used to verify the identity of the user.Data Type: string

 Default Value: n/a

</td></tr></tbody>
</table>**Parent Topic:**[Password Reset verifications](c_PWRVerifications.md)

**Related topics**  


[Create a custom identification type for Password Reset](../task/t_CreateAnIdentificationType.md)

