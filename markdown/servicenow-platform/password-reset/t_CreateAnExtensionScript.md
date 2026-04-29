---
title: Create a Password Reset extension script
description: Create extension scripts only from the Password Reset Extension Script form. Do not create extension scripts in the System Definition Script Includes interface.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Password Reset script includes, Password Reset reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a Password Reset extension script

Create extension scripts only from the Password Reset Extension Script form. Do not create extension scripts in the **System Definition** &gt; **Script Includes** interface.

## Before you begin

Role required: password\_reset\_admin or admin

**Note:** To use a script include as an extension script, you must set it to **Active** status.

## Procedure

1.  Navigate to **Password Reset** &gt; **Extensions** &gt; **New extension script**.

2.  Enter a name in the **Extension script name** field.

    Use CamelCase to construct a name without spaces, for example, `PwdEnrollmentCustom`.

3.  Select an **Extension script category**.

    -   Enrollment check
    -   Enrollment form processor
    -   Identification form processor
    -   Password generator
    -   User account lookup
    -   Verification form processor
4.  Click **Submit**.

    A new instance of the script include for the selected category opens.

5.  Edit the script by providing an implementation in the body of the process or processForm function, depending on the script category.

    You can add additional functions as long as the process or processForm function accepts the defined parameters and returns the expected results.

    **Note:** Do not edit or delete the Category declaration.

    ![New extension script](../image/NewExtensionScript.png)

6.  Click **Update**.


