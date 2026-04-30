---
title: Password Reset extension script categories
description: You can use a custom extension script to extend Password Reset functionality for credential store, verification, or identification types.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Password Reset script includes, Reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset extension script categories

You can use a custom extension script to extend Password Reset functionality for credential store, verification, or identification types.

**Note:** To use a script include as an extension script, you must set it to **Active** status.

## Password Reset extension script categories

Extension scripts must specify a category that indicates which script include is being extended, for example, `category: 'password_reset.extension.enrollment_check'`. The ServiceNow platform installs several scripts in each category. A script in the **Enrollment check** category can perform the enrollment check for a verification. Detailed information on each extension script appears in [Password Reset extension scripts](pw-reset-ext-script-includes.md).

|Extension script category|Description|
|-------------------------|-----------|
|Enrollment check|Defines how to check that a user is enrolled in the Password Reset process. Scripts of this category are available in the **Enrollment check** field when you define a verification type \(Password Reset Verification Type form\).|
|Enrollment form processor|Defines how an enrollment form is processed \(if automatic enrollment is not configured\). Scripts of this category are available in the **Enrollment form processor** field when you define a verification type \(Password Reset Verification Type form\).|
|Identification form processor|Defines how a user identification is processed. Scripts of this category are available in the **Identification processor** field when you define a verification type \(Password Reset Identification Type form\).|
|Password generator|Defines how to generate a password. Scripts of this category are available in the **Auto generate password** field when you configure a credential store \(Password Reset Credential Store Type form\).|
|Post reset script|Executes at the end of a Password Reset process. Scripts of this category are available in the **Post reset script** field when you configure a process \(Password Reset Process form\).|
|User account lookup|Defines how to look up a user account. Scripts of this category are available in the **User account lookup** field when you configure a credential store \(Password Reset Credential Store form\).|
|Verification form processor|Defines how a verification form is processed. Scripts of this category are available in the **Verification processor** field when you define a verification type \(Password Reset Verification Type form\).|

**Related topics**  


[Password Reset extension scripts](pw-reset-ext-script-includes.md)

