---
title: View user requests for password reset
description: The Reset Requests module displays the status of each password reset request from the Password Reset Request table \[pwd\_reset\_request\].
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reset a password or unlock a user account with service desk assistance, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# View user requests for password reset

The **Reset Requests** module displays the status of each password reset request from the Password Reset Request table \[pwd\_reset\_request\].

## Before you begin

Role required: password\_reset\_admin or password\_reset\_service\_desk

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Reset Requests**.

<table id="table_nvn_j22_sr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User

</td><td>

User whose password is being reset or changed.

</td></tr><tr><td>

Process

</td><td>

Process that implements this password reset request.

</td></tr><tr><td>

Type

</td><td>

Type of Password Reset request:

-   **Change Password**: Request to change a password.
-   **Help Desk**: Request opened on behalf of the requesting user by a service desk agent.
-   **Self Service**: Requesting user opened the reset request.


</td></tr><tr><td>

Action Type

</td><td>

Corrective action performed during the Password Reset request.

-   **Change Password**: Update the credential store with the new password.
-   **Reset and Unlock Account**: Generate a new password for the user and unlock the user account.
-   **Reset Password**: Generate a new password for the user.
-   **Unlock Account**: Unlock the user account.


</td></tr><tr><td>

Status

</td><td>

Result of the Password Reset request:

-   **Completed With Failure**: User completed all steps in the Password Reset process, but the password was not reset in the credential store.
-   **Completed With Success**: User completed all steps in the Password Reset process and the password was reset in the credential store.
-   **Expired**: User did not complete all steps in the Password Reset process in the time allowed.
-   **In Progress**: User is working through the steps to reset the password.
-   **Max Number of Attempts**: User failed to answer the security questions correctly during the identity verification step and has exceeded the maximum number of attempts allowed.
-   **Verified**: User has completed the identity verification step and is verified. The user can move to the Password Reset step.


</td></tr><tr><td>

Active

</td><td>

Whether the request is open or closed.

</td></tr><tr><td>

Retry

</td><td>

Total number of times the user has attempted to complete a password reset request.

</td></tr></tbody>
</table>
**Parent Topic:**[Reset a password or unlock a user account with service desk assistance](reset-password-for-user.md)

