---
title: Installed with Password Reset
description: Tables, roles, business rules, scripts, and workflows are installed with the Password Reset application.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Password Reset reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Installed with Password Reset

Tables, roles, business rules, scripts, and workflows are installed with the Password Reset application.

## Password Reset tables

<table id="table_Tables"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Password Reset Active Answer \[pwd\_active\_answer\]

</td><td>

Security questions and associated answers, in an encrypted state, that users selected while going through the enrollment process.

</td></tr><tr><td>

Password Reset Active Question \[pwd\_active\_question\]

</td><td>

Security questions that users selected while going through the enrollment process.

</td></tr><tr><td>

Password Reset Activity Log \[pwd\_reset\_activity\]

</td><td>

All Password Reset requests.

</td></tr><tr><td>

Password Reset Activity Monitor \[pwd\_activity\_monitor\]

</td><td>

Password Reset lockout activity.

</td></tr><tr><td>

Password Reset Credential Store \[pwd\_cred\_store\]

</td><td>

Password Reset credential stores that are available.

</td></tr><tr><td>

Password Reset Credential Store Parameters \[pwd\_cred\_store\_param\]

</td><td>

User-created credential store parameters.

</td></tr><tr><td>

Password Reset Credential Store Types \[pwd\_cred\_store\_type\]

</td><td>

Password Reset credential store types that are available.

</td></tr><tr><td>

Password Reset Desktop Access Control\[pwd\_access\_control\]

</td><td>

Password Reset Windows Application access control.

</td></tr><tr><td>

Password Reset Desktop Access Log\[pwd\_access\_log\]

</td><td>

Password Reset Windows Application access logs.

</td></tr><tr><td>

Password Reset Device Enrollment Code \[pwd\_dvc\_enrollment\_code\]

</td><td>

Device enrollment codes that were sent to users during SMS code enrollment.

</td></tr><tr><td>

Password Reset Devices \[pwd\_device\]

</td><td>

User SMS devices that are in a state of verified.

</td></tr><tr><td>

Password Reset Email Verification Code\[pwd\_email\_code\]

</td><td>

Verification codes that were sent to users via email for password reset or email address enrollment.

</td></tr><tr><td>

Password Reset Enrollment for Verification \[pwd\_enrollment\]

</td><td>

Information about user enrollment by verification.

</td></tr><tr><td>

Password Reset Enrollment Snapshot \[pwd\_enrollment\_snapshot\]

</td><td>

Snapshot of user enrollment by verification.

 This table is used for the reporting purpose.

 The Sync Password Reset Enrollment Snapshot Data Monthly scheduled job runs once a month to generate or sync snapshot data in this table. The data, such as sys\_user creation or deletion, verification to process creation or deletion, and so on, is synchronized.

 Password Reset DB listener is used to create or update the data in this table which is managed by the **pwd\_reset.enable.dbListener** property with default value as true.

 If you’re an admin and want to manually sync the data in this table related to an active process, select **Sync Enrollment Snapshot Data** on that Password Reset process.

 You can turn off the data synchronization in this table through the DB listener or the monthly scheduled job by setting the **pwd\_reset.enable.enrollment\_snapshot** property to false.

 **Note:** Initially, an inactive record is created by the DB listener for a user-verification pair. When the users enrol themselves on the Password Reset Enrolment page, the record becomes active in this table.

</td></tr><tr><td>

Password Reset Extension Type \[pwd\_extension\_type\]

</td><td>

Extension types that are available.

</td></tr><tr><td>

Password Reset History\[pwd\_history\]

</td><td>

History of passwords that users reset.

</td></tr><tr><td>

Password Reset Identification Type \[pwd\_identification\_type\]

</td><td>

Password Reset identification types that are available.

</td></tr><tr><td>

Password Reset Process \[pwd\_process\]

</td><td>

Password Reset processes that are available.

</td></tr><tr><td>

Password Reset Process Credential Store \[pwd\_map\_proc\_to\_cred\_store\]

</td><td>

Credential stores and the associated Password Reset processes that the application is using.

</td></tr><tr><td>

Password Reset Process User Group \[pwd\_map\_proc\_to\_group\]

</td><td>

Groups and the associated Password Reset processes that the application is using.

</td></tr><tr><td>

Password Reset Process Verification \[pwd\_map\_proc\_to\_verification\]

</td><td>

Verifications and the associated Password Reset processes that the application is using.

</td></tr><tr><td>

Password Reset Question \[pwd\_question\]

</td><td>

Questions that the application uses for security question verifications.

</td></tr><tr><td>

Password Reset Request \[pwd\_reset\_request\]

</td><td>

Information about Password Reset requests.

</td></tr><tr><td>

Password Reset Request Verification\[pwd\_map\_request\_to\_verification\]

</td><td>

Password reset requests and the associated verification that the application is using.

</td></tr><tr><td>

Password Reset SMS Verification Code \[pwd\_sms\_code\]

</td><td>

SMS verification codes that were sent to users for a password reset.

</td></tr><tr><td>

Password Reset User Lockout \[pwd\_user\_lockout\]

</td><td>

Users that are locked out of Password Reset.

</td></tr><tr><td>

Password Reset Verification \[pwd\_verification\]

</td><td>

Verifications that are available.

</td></tr><tr><td>

Password Reset Verification Param \[pwd\_verification\_param\]

</td><td>

User-created verification parameters.

</td></tr><tr><td>

Password Reset Verification Type \[pwd\_verification\_type\]

</td><td>

Password Reset verification types that are available.

</td></tr></tbody>
</table>## Password Reset roles

**Note:** Only the user with the following roles can have access to Password Reset tables. The deny unless authenticated ACLs restrict access to the Password Reset tables for any unauthenticated role such as public role user.

For more information, see [Deny-Unless ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/access-control/acl-denial-behavior.md).

<table id="table_vqc_jvj_sr"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

password reset administrator \[password\_reset\_admin\]

</td><td>

Configures and maintains Password Reset and Password Change.

</td></tr><tr><td>

service desk agent \[password\_reset\_service\_desk\]

</td><td>

Resets passwords on behalf of users, tracks password reset requests, and views logs.

</td></tr><tr><td>

credentials manager \[password\_reset\_credential\_manager\]

</td><td>

Determines which credential stores are valid for use with Password Reset.

</td></tr></tbody>
</table>## Password Reset business rules

<table id="table_BusinessRules"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Abort if password history limit exceeds

</td><td>

Password Reset Credential Store Parameters\[pwd\_cred\_store\_param\]

</td><td>

Prevents setting password history limit that exceeds the value of the **password\_reset.history.limit** property.You can set a password reset history value in the **password\_reset.history.limit** property. This system property checks the history of previous passwords based on the specified value. By default, the value is 10. But you can set it based on your organizational needs.

**Note:** Currently, this property is applicable only to the ServiceNow credential store.

</td></tr><tr><td>

Add default parameters QA verification

</td><td>

Password Reset Verification \[pwd\_verification\]

</td><td>

If no parameters for Security Question verifications are specified, generates parameters.

</td></tr><tr><td>

Add default parameters SMS verification

</td><td>

Password Reset Verification \[pwd\_verification\]

</td><td>

If there are no parameters specified, generates SMS code verifications parameters.

</td></tr><tr><td>

Add params personal confirm verification

</td><td>

Password Reset Verification \[pwd\_verification\]

</td><td>

If there are no parameters specified, generates personal data confirmation verifications parameters.

</td></tr><tr><td>

Add params personal verification

</td><td>

Password Reset Verification \[pwd\_verification\]

</td><td>

If there are no parameters specified, generates parameters for personal data verification.

</td></tr><tr><td>

Check unique verifications

</td><td>

Password Reset Process Verification \[pwd\_map\_proc\_to\_verification\]

</td><td>

Prevents a verification from being assigned multiple times to a specific Password Reset process.

</td></tr><tr><td>

Clear parameters for Mock verification

</td><td>

Password Reset Verification\[pwd\_verification\]

</td><td>

Clears parameters for the Mock verification.

</td></tr><tr><td>

Deactivate process with no group

</td><td>

Password Reset Process User Group \[pwd\_map\_proc\_to\_group\]

</td><td>

Deactivates the process if it does not apply to all users or if the groups associated with it are removed.

</td></tr><tr><td>

Deactivate process with no min ver

</td><td>

Password Reset Process Verification\[pwd\_map\_proc\_to\_verification\]

</td><td>

Deactivates the process if the verifications associated with the process are less than the minimum value for the process.

</td></tr><tr><td>

Deactivate process with no verification

</td><td>

Password Reset Process Verification \[pwd\_map\_proc\_to\_verification\]

</td><td>

Deactivates the process if the verifications associated with it are removed.

</td></tr><tr><td>

Delete history passwords if needed

</td><td>

Password Reset Credential Store\[pwd\_cred\_store\]

</td><td>

Deletes history passwords if needed.

</td></tr><tr><td>

Enforce password history message

</td><td>

Password Reset Credential Store\[pwd\_cred\_store\]

</td><td>

Passes enforce password history related messages to the client side.

</td></tr><tr><td>

Google Auth Enabled Check

</td><td>

Password Reset Process\[pwd\_process\]

</td><td>

Deactivates the process with Google Authenticator verification if the Google authenticator is disabled.

</td></tr><tr><td>

GoogleAuthSysPropertyCheck

</td><td>

Password Reset Process Verification\[pwd\_map\_proc\_to\_verification\]

</td><td>

Deactivates the process with the Google Authenticator verification if the Google authenticator is disabled.

</td></tr><tr><td>

Handle req\_enroll validation/default val

</td><td>

Password Reset Process Verification\[pwd\_map\_proc\_to\_verification\]

</td><td>

Handles requires\_enrollment and auto\_enroll values for the process.

</td></tr><tr><td>

Insert/update scheduled job for reminder

</td><td>

Password Reset Process\[pwd\_process\]

</td><td>

Inserts/updates the scheduled job for enrollment reminder.

</td></tr><tr><td>

Order must be unique

</td><td>

Password Reset Desktop Access Control\[pwd\_access\_control\]

</td><td>

Enforces order to be unique.

</td></tr><tr><td>

Parameter Names Cannot Be Updated

</td><td>

Password Reset Verification Param \[pwd\_verification\_param\]

</td><td>

Prevents parameter name changes.

</td></tr><tr><td>

Password Reset Activity Monitor

</td><td>

Password Reset User Lockout \[pwd\_user\_lockout\]

</td><td>

Creates an event when the number of users locked out of Password Reset during a specific interval exceeds the threshold value.

</td></tr><tr><td>

Password Reset Validate Auto-generate

</td><td>

Password Reset Process \[pwd\_process\]

</td><td>

Checks that either **Email/SMS password** or **Display password** is selected when the **Auto-generate password** check box is selected.

</td></tr><tr><td>

Personal Data Confirm Param Validation

</td><td>

Password Reset Verification Param \[pwd\_verification\_param\]

</td><td>

Checks that a column exists in the sys\_user table for the parameter used in a personal data confirmation verification.

</td></tr><tr><td>

Personal Data Param Validation

</td><td>

Password Reset Verification Param \[pwd\_verification\_param\]

</td><td>

Checks that a column exists in the sys\_user table for the parameter used in a personal data verification.

</td></tr><tr><td>

Prevent against deletion

</td><td>

Password Reset Credential Store \[pwd\_cred\_store\]

</td><td>

Checks whether the credential store is part of an active process before allowing deletion.

</td></tr><tr><td>

Prevent against deletion

</td><td>

Password Reset Identification Type \[pwd\_identification\_type\]

</td><td>

If an identification type is part of an active process, prevents the identification type from being deleted.

</td></tr><tr><td>

Prevent against deletion

</td><td>

Password Reset Verification \[pwd\_verification\]

</td><td>

If the verification is part of an active process, prevents it from being deleted.

</td></tr><tr><td>

Prevent against deletion when in use

</td><td>

Password Reset Credential Store Types\[pwd\_cred\_store\_type\]

</td><td>

Prevents deletion when the type is in use.

</td></tr><tr><td>

Prevent against deletion when in use

</td><td>

Password Reset Verification Type\[pwd\_verification\_type\]

</td><td>

Prevents deletion when the type is in use.

</td></tr><tr><td>

Queue event if history limit decreases

</td><td>

Password Reset Credential Store Parameters\[pwd\_cred\_store\_param\]

</td><td>

Queues the pwd.credStore.history.limit.decrease event if history limit decreases.

</td></tr><tr><td>

Security Questions Param Validation

</td><td>

Password Reset Verification Param \[pwd\_verification\_param\]

</td><td>

Checks for valid parameters in security question verifications.

</td></tr><tr><td>

Send SMS code

</td><td>

Password Reset Device Enrollment Code \[pwd\_dvc\_enrollment\_code\]

</td><td>

Sends an enrollment code to a device.

</td></tr><tr><td>

Set new record flag

</td><td>

Password Reset Process \[pwd\_process\]

</td><td>

Sets a new record flag for the client to take appropriate action.

</td></tr><tr><td>

Send SMS Verification Code Via Notify

</td><td>

Password Reset SMS Verification Code

 \[pwd\_sms\_code\]

</td><td>

Sends out SMS authentication code via Notify if the Notify plugin is active.

</td></tr><tr><td>

Single credential store per process

</td><td>

Password Reset Process Credential Store \[pwd\_map\_proc\_to\_cred\_store\]

</td><td>

Prevents having more than one credential store per process.

</td></tr><tr><td>

SMS Code Param Validation

</td><td>

Password Reset Verification Param \[pwd\_verification\_param\]

</td><td>

Checks for valid parameters in SMS code verifications.

</td></tr><tr><td>

Update action based on access conditions

</td><td>

Password Reset Desktop Access Log\[pwd\_access\_log\]

</td><td>

Updates the “action” field of this log record based on the access control conditions.

</td></tr><tr><td>

Update proc\_to\_cred\_store

</td><td>

Password Reset Process \[pwd\_process\]

</td><td>

Enforces a one-to-one relation between a Password Reset process and a credential store.

</td></tr><tr><td>

Validate Process

</td><td>

Password Reset Process \[pwd\_process\]

</td><td>

Verifies that a Password Reset process is configured correctly.

</td></tr><tr><td>

Validate Pwd Cred Store Name

</td><td>

Password Reset Credential Store\[pwd\_cred\_store\]

</td><td>

Enforces the name to be unique.

</td></tr><tr><td>

Validate Pwd Cred Store Type Name

</td><td>

Password Reset Credential Store Types\[pwd\_cred\_store\_type\]

</td><td>

Enforces the name to be unique.

</td></tr><tr><td>

Validate Pwd Extension Type Name

</td><td>

Password Reset Extension Type\[pwd\_extension\_type\]

</td><td>

Enforces the name to be unique.

</td></tr><tr><td>

Validate Pwd Identification Type Name

</td><td>

Password Reset Identification Type\[pwd\_identification\_type\]

</td><td>

Enforces the name to be unique and not empty.

</td></tr><tr><td>

Validate Pwd Process Name

</td><td>

Password Reset Process\[pwd\_process\]

</td><td>

Enforces the name to be unique.

</td></tr><tr><td>

Validate Pwd Verification Name

</td><td>

Password Reset Verification\[pwd\_verification\]

</td><td>

Enforces the name to be unique.

</td></tr><tr><td>

Validate Pwd Verification Type Name

</td><td>

Password Reset Verification Type\[pwd\_verification\_type\]

</td><td>

Enforces the name to be unique.

</td></tr><tr><td>

Validate Security Question

</td><td>

Password Reset Question \[pwd\_question\]

</td><td>

Validates rules for security questions such as no duplicates or empty questions.

</td></tr><tr><td>

Verify Account Lookup Script

</td><td>

Password Reset Credential Store \[pwd\_cred\_store\]

</td><td>

Checks whether the account lookup script has the correctly named function.

</td></tr><tr><td>

VerifyAutoEnroll

</td><td>

Password Reset Verification Type \[pwd\_verification\_type\]

</td><td>

Checks whether auto-enroll is selected and ensures that an enrollment check script is provided.

</td></tr></tbody>
</table>## Password Reset UI pages

|Name|Description|
|----|-----------|
|$pwd\_reset|First page of self-service reset process \(asks for user ID\).|
|$pwd\_reset\_serviceDesk|First page of service desk assisted reset process \(asks for user ID\).|
|$pwd\_verify|Second page of reset process \(asks user to verify identity\).|
|$pwd\_new|Last page of password change process \(asks for new password\).|
|$pwd\_success|Page that appears when password is reset successfully.|
|$pwd\_error|Page that appears on error during reset process.|
|$pwd\_confirm|For processes configured to email or SMS password reset URL: After successful verification, this page displays message about sending link to user.|
|$pwd\_change|Page for changing password.|
|$pwd\_change\_success|Page that appears when password is changed successfully.|
|$pwd\_change\_error|Page that appears on error during password change process.|
|$pwd\_enrollment\_form\_container|Enrollment page for all verifications.|
|$pwd\_enrollment\_success|Page that appears when enrollment is successful.|
|$pwd\_enroll\_error|Page that appears when any error happens during enrollment.|
|$pwd\_unlock\_success|Page that appears when locked user is successfully unlocked.|
|$pwd\_reset\_downloads\_ui|Page for downloading Password Reset Windows Application.|

## Password Reset UI macros

|Name|Description|
|----|-----------|
|$pwd\_csrf\_validation|CSRF validation for Password Reset Application. If violation is detected, the page will be redirected to the error page.|
|$pwd\_display\_password|Displays a temporary password on the success page if the process is configured to auto-generate.|
|$pwd\_enroll\_email\_ui and $pwd\_verify\_email\_ui|UI for email enrollment and verification.|
|$pwd\_enroll\_google\_auth\_ui and $pwd\_verify\_google\_auth\_ui|UI for Google Authentication enrollment and verification.|
|$pwd\_enroll\_questions\_ui|UI for question and answer security validation enrollment.|
|$pwd\_enroll\_questions\_ui\_js|JavaScript code that requires server-side data for security question and answer enrollment.|
|$pwd\_enroll\_sample\_ui|Sample UI macro for enrollment for Mock Verification Type.|
|$pwd\_enroll\_sms\_ui and $pwd\_verify\_sms\_ui|UI for SMS enrollment and verification.|
|$pwd\_enrollment\_form\_title|Jelly macro function that prints the title for the enrollment form. A verification ID is mandatory.|
|$pwd\_error\_message|UI for displaying error messages.|
|$pwd\_process\_flow|UI for indicating current stage.|
|$pwd\_process\_footer|JavaScript code to get the footer macro name.|
|$pwd\_reset\_stylesheet|JavaScript code to get the default CSS file ID.|
|$pwd\_verify\_personal\_data\_ui and $pwd\_verify\_personal\_data\_confirmation\_ui|UI for verifying personal data and for confirming personal data.|
|$pwd\_verify\_questions\_ui|UI for verifying questions.|
|$pwd\_verify\_simple\_ui|Input section for a simple verification method. This field is a single input field.|

## UI scripts installed with Password Reset

You can create a UI script and reference the script from a UI macro or UI page by using a &lt;g:include\_script&gt; Jelly tag. The following example shows how the $pwd\_enroll\_questions\_ui UI macro can reference the $pwd\_enroll\_questions\_ui script. In the example, \[UI Script Name\]+".jsdbx" is the name of the script:

```
<g:include_script src="$pwd_enroll_questions_ui.jsdbx" />
```

By referencing an external script, you can maintain separation between client JavaScript code and Jelly code, which simplifies maintenance. You can use the following installed scripts with Password Reset UI macros:

|Name|Description|
|----|-----------|
|$pwd\_csrf\_common\_ui\_script|Common UI script for handling a Cross-site Request Forgery \(CSRF\).|
|$pwd\_enroll\_email\_ui|JavaScript code for the $pwd\_enroll\_questions\_ui UI macro.|
|$pwd\_enroll\_google\_auth\_ui|JavaScript code for the $pwd\_enroll\_google\_auth\_ui UI macro.|
|$pwd\_enroll\_questions\_ui|JavaScript code for the $pwd\_enroll\_questions\_ui UI macro.|
|$pwd\_enroll\_sample\_ui|Included sample client JavaScript for the $pwd\_enroll\_sample\_ui UI macro.|
|$pwd\_enroll\_sms\_ui|SMS enrollment UI script.|
|$pwd\_enrollment\_submit\_event|UI script for an enrollment submission event.|
|$pwd\_util|Utilities for password reset UI pages and UI macros.|
|$pwdWfManager|Helper class to handle workflow activities and post-processing.|

## Password Reset workflows

The Password Reset plugin adds workflows that you can use as examples to create custom workflows for Password Reset processes.

|Workflow|Description|
|--------|-----------|
|Pwd Reset - AD|Connects to an AD server.|
|Pwd Reset - Local ServiceNow|Current \(local\) instance.|
|Pwd Reset - Master|Password Reset primary workflow.|
|Pwd Reset - Mock Fatal|Example workflow to use in Password Reset testing to simulate a fatal error. No retries.|
|Pwd Reset - Mock Non Fatal|Example workflow to use in Password Reset testing to simulate a non-fatal error.|
|Pwd Reset - Mock Success|Example workflow to use in Password Reset testing to simulate a successful completion.|
|Pwd Reset - Remote ServiceNow|Connects to a remote\(SOAP\) ServiceNow instance.|

|Workflow|Description|
|--------|-----------|
|Pwd Connection Test - AD|Tests connection to an AD server.|
|Pwd Connection Test - Local SN|Tests connection to local instance.|
|Pwd Connection Test - Master|Master workflow to test credential store connectivity.|
|Pwd Connection Test - Mock Failure|Example credential store connection test that simulates a failed connection.|
|Pwd Connection Test - Mock Success|Example credential store connection test that simulates a successful connection.|
|Pwd Connection Test - Remote SN|Tests connection to a remote\(SOAP\) ServiceNow instance.|

|Workflow|Description|
|--------|-----------|
|Pwd Get Lock State - AD|Gets a user account lock state for the AD server.|
|Pwd Get Lock State - Local SN|Workflow to get a user account lock state for the local instance.|
|Pwd Get Lock State - Master|Primary workflow to get a user account lock state.|
|Pwd Get Lock State - Remote SN|Gets a user account lock state for the remote\(SOAP\) ServiceNow instance.|

|Workflow|Description|
|--------|-----------|
|Pwd Unlock Account – AD|Unlocks a user account for a local instance.|
|Pwd Unlock Account - Local SN|Workflow to unlock a user account for a local instance.|
|Pwd Unlock Account - Master|Master workflow to unlock a user account.|
|Pwd Unlock Account – Remote SN|Unlocks a user account for a remote\(SOAP\) ServiceNow instance.|

|Workflow|Description|
|--------|-----------|
|Pwd Change - Master|Password change primary workflow.|
|Pwd Change – Local ServiceNow|Connects to a local instance to change a password.|
|Pwd Change – AD|Connects to an AD server to change a password.|
|Pwd Change – Remote ServiceNow|Connects to a remote\(SOAP\) ServiceNow instance to change a password.|

## Password Reset notifications

<table id="table_a25_cff_wcb"><thead><tr><th>

Name

</th><th>

Fired by event name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Password Reset – Send SMS Code

</td><td>

pwd.send\_sms\_code.trigger

</td><td>

Sends out SMS authentication code for verification.

</td></tr><tr><td>

\[K\] Password Reset – Send Email Code

</td><td>

pwd.send\_email\_code.trigger

</td><td>

Sends out authentication code via Email for verification.

</td></tr><tr><td>

Password Reset - Enrollment Reminder

</td><td>

pwd.enrollment\_reminder.trigger

</td><td>

Sends emails to remind users to enroll in the required verifications.

</td></tr><tr><td>

Password Reset - New Password Confirmation

</td><td>

pwd.email.trigger

</td><td>

For the Email/SMS Password process, sends an email or SMS \(if configured\) that includes the new password.

</td></tr><tr><td>

Password Reset - Send Verify Code

</td><td>

pwd.send\_verify\_code.trigger

</td><td>

Sends authentication code to users using email or SMS for password reset or enrollment.**Note:** If the Notify plugin is active, SMS code is sent via Twilio instead of ServiceNow Notification.

</td></tr><tr><td>

Password Reset URL

</td><td>

password.reset.url

</td><td>

For the Email/SMS Password Reset URL process: Sends email or SMS \(if configured\) that includes a link to the password reset URL.**Note:** Check the following items if the instance does not send the email notification to the user:

-   Check the System Event \[sys\_event\] table to see if the email was sent.
-   Verify that the user is subscribed to the notification.
-   Verify that the Default Self Service password reset process and password reset properties are configured correctly.

</td></tr></tbody>
</table>## SOAP messages for Password Reset

|SOAP Message|Description|
|------------|-----------|
|Change Password|When the Orchestration Add-on plugin is active, the system can use the SOAP protocol to change passwords on remote credential stores such as a remote ServiceNow instance.|
|Password Reset Request|When the Orchestration Add-on plugin is active, the system can use the SOAP protocol to reset passwords on remote credential stores such as a remote ServiceNow instance.|

## REST API

-   Name: Pwd Reset
-   API ID: pwd\_reset
-   Base API path: /api/now/pwd\_reset

|Name|Resource path|API Version|Description|
|----|-------------|-----------|-----------|
|pwd\_init|/api/now/v1/pwd\_reset/init|v1|Initial request to establish session, write logs, and fetch UI messages.|
|pwd\_identify|/api/now/v1/pwd\_reset/identify|v1|Get identification page components.|
|pwd\_verify|/api/now/v1/pwd\_reset/verify|v1|Get verification page components.|
|pwd\_new|/api/now/v1/pwd\_reset/reset|v1|Get resetting password page components.|
|pwd\_success|/api/now/v1/pwd\_reset/success|v1|Get success page components.|
|pwd\_failure|/api/now/v1/pwd\_reset/failure|v1|Get failure page components.|

|Name|Resource path|API Version|Description|
|----|-------------|-----------|-----------|
|pwd\_init|/api/now/v2/pwd\_reset/init|v2|Initial request to establish session, write logs, and fetch UI messages.|
|pwd\_identify|/api/now/v2/pwd\_reset/identify|v2|Get identification page components.|
|pwd\_verify|/api/now/v2/pwd\_reset/verify|v2|Get verification page components.|
|pwd\_new|/api/now/v2/pwd\_reset/reset|v2|Get reset password page components.|
|pwd\_success|/api/now/v2/pwd\_reset/success|v2|Get success page components.|
|pwd\_failure|/api/now/v2/pwd\_reset/failure|v2|Get failure page components.|

