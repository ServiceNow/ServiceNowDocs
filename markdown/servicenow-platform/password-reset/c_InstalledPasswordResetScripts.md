---
title: Password Reset script includes
description: The Password Reset plugin installs script includes that implement password reset processes. To enable you to extend functionality, each base-system script include provides extension points that you can use to invoke "extension scripts" that you customized.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset script includes

The Password Reset plugin installs script includes that implement password reset processes. To enable you to extend functionality, each base-system script include provides extension points that you can use to invoke "extension scripts" that you customized.

The [extension script category](pw-reset-extension-script.md) refers to the specific types of behavior for an extension script \(for example, credential store, verification, identification type, or as a post-processor\).

## 'Enrollment check' script includes

All enrollment check script includes take the following parameters and return a boolean indicating whether the user is enrolled for Password Reset.

-   params.userId: The sys\_id of the user being checked \(table: \[sys\_user\]\).
-   params.verificationId: The sys\_id of the verification being checked \(table: \[pwd\_verification\]\).

|Name|Description|
|----|-----------|
|PwdAlwaysEnrolled|Default check of whether a user is enrolled that always returns true.|
|PwdMockIsEnrolled|Default check of whether a user is enrolled that always returns true.|
|PwdQuestionsEnrollmentCheck|Determines whether a user has enrolled for Password Reset using security question verification.|
|PwdSMSEnrollmentCheck|Determines whether a user has enrolled for Password Reset using SMS verification.|

## 'Identification form processor' script includes

Identification form processor script includes provide functionality for extending identification processing.

All identification form processor script includes take the following parameters, and return the sys\_id of the user that corresponds to the requested input. If the user was not identified, it returns null.

-   params.processId: The sys\_id of the calling Password Reset process \(table: \[pwd\_process\]\).
-   param request: The form request object. Fields in the form can be accessed with request.getParameter\('&lt;element-id&gt;'\). The supported request parameter is sysparm\_user\_id, the user identifier value entered in the form.

|Name|Description|
|----|-----------|
|PwdIdentifyViaEmail|Verifies a user's identity by checking the email address.|
|PwdIdentifyViaUsername|Verifies a user's identity by checking the user name.|

## 'Enrollment form processor' script includes

Enrollment form processor script includes provide functionality for extending enrollment form processing.

All enrollment form processor script includes take the following parameters, and return a boolean indicating whether the user was successfully enrolled.

-   params.userId: The sys\_id of the user trying to enroll \(table: \[sys\_user\]\).
-   params.verificationId: The sys\_id of the verification used to enroll \(table: \[pwd\_verification\]\).
-   params.enrollmentId: The sys\_id of this enrollment process.
-   request: The form request object. Fields in the form can be accessed with request.getParameter\('&lt;element-id&gt;'\).

You should add the following information to the state of the enrollment process:

-   gs.getSession\(\).putProperty\("result.status",status\): Whether the user was successfully enrolled.
-   gs.getSession\(\).putProperty\("result.message",message\): An associated message to be returned to the UI, such as a detailed error message.
-   gs.getSession\(\).putProperty\("result.value",value\): A custom value associated with the enrollment.

|Name|Description|
|----|-----------|
|PwdEnrollQuestionsProcessor|Handles questions and answers for verification.|
|PwdEnrollSampleProcessor|Provides an enrollment processor for sample verification.|
|PwdEnrollSMSProcessor|Provides an enrollment processor for SMS verification.|

## 'User account lookup' script includes

User account lookup script includes return the credential store account\_id for a given user.

The following parameter returns the credential store account\_id for a given user. params.userId: The sys\_id of the user being checked \(table: \[sys\_user\]\).

|Name|Description|
|----|-----------|
|PwdDefaultUserAccountLookup|Provides a default script for user account lookup from a user\_id to the account in a credential store. The default mapping is to use the user name as the account name.|

## 'Password generator' script includes

Password generator script includes take the following parameter, and return an auto-generated string password.

params.credentialStoreId: The sys\_id of the calling Password Reset process \(table: \[pwd\_process\]\).

|Name|Description|
|----|-----------|
|PwdDefaultAutoGenPassword|Generates a password from a random word and 4 digits.|

## 'Verification processor' script includes

If the user identity is verified, the verification processor script includes return `true`.

Verification processor script includes take the following parameters:

-   params.resetRequestId: The sys\_id of the current Password Reset request \(table: \[pwd\_reset\_request\]\).
-   params.userId: The sys\_id of the user to be verified \(table: \[sys\_user\]\).
-   params.verificationId: The sys\_id of the verification \(table: \[pwd\_verification\]\).
-   request: The form request object. Access the fields in the form with request.getParameter\('&lt;element-id&gt;'\).

|Name|Description|
|----|-----------|
|PwdVerifyPersonalDataConfirmationProcess|Verifies that the user accepts the answer.|
|PwdVerifyPersonalDataProcessor|Verifies that the user's answers match the expected data in the system.|
|PwdVerifyQuestionsProcessor|Provides question and answer verification of user input on the second page of the verification form.|
|PwdVerifySimpleProcessor|Provides simple verification of user input on the second page of the verification form.|
|PwdVerifySMSProcessor|Provides SMS verification of user input on the second page of the verification form.|

## 'Post processor' script includes

Post processor script includes execute custom actions after the Password Reset process has completed.

All post processor script includes take the following parameters.

-   params.resetRequestId: The sys\_id of the current Password Reset request \(table: \[pwd\_reset\_request\]\).
-   params.wfSuccess: A flag indicating whether the workflow completed successfully: True if, and only if, successful.

|Name|Description|
|----|-----------|
|PwdPostProcessor|Executes actions after the process completes for success, failure, or both conditions.|

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US)

