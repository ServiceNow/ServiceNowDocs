---
title: Specify lockout for failed login attempts
description: The system provides inactive script actions that enable you to specify the number of failed login attempts before a user account is locked and to reset the count after a successful login.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Defining login scenarios, Local Authentication, Authentication, Access Management]
---

# Specify lockout for failed login attempts

The system provides inactive script actions that enable you to specify the number of failed login attempts before a user account is locked and to reset the count after a successful login.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Script Actions** to view or activate the scripts.

    **Note:** Starting with the Kingston release, following a zBoot, the script actions **SNC User Lockout Check with Auto Unlock** and **SNC User Clear** are activated.

    To learn more about properties that affect failed login attempts, see [Managing failed login attempts \(instance security hardening\)](../../security-center/reference/sc-managing-failed-login-attempts.md) in the Instance Security Hardening Settings.

<table id="table_yzs_qcf_g1b"><thead><tr><th>

Script action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SNC User Lockout Check with Auto Unlock

</td><td>

-   Uses the value of the glide.user.max\_unlock\_attempts property to set the limit for failed login attempts.
-   Unlocks the user account after the time period that is specified for the glide.user.unlock\_timeout\_in\_mins property. If no value is specified, then the system unlocks the user account after the default period of 15 minutes.


</td></tr><tr><td>

SNC User Lockout Check

</td><td>

Tracks the number of failed login attempts and locks the user account after a specified number of failed login attempts \(default: 5\).

</td></tr><tr><td>

SNC User Clear

</td><td>

Updates the user record after a successful login: Resets the number of failed login attempts and updates the date of the last login.

</td></tr></tbody>
</table>
## What to do next

Each time a user attempts to log in, the action is recorded in an event log. You can view a log of failed login attempts.

1.  Navigate to **System Policy** &gt; **Event Logs**.
2.  Filter for **login.failed** in the **Name** field. You can view the attempted login name, date, and IP address logged for the attempt.

