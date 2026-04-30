---
title: Reset a password or unlock a user account with service desk assistance
description: Reset a password or unlock a user account by requesting the assistance of a service desk agent.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Reset a password or unlock a user account with service desk assistance

Reset a password or unlock a user account by requesting the assistance of a service desk agent.

## Before you begin

Watch this video example of service desk agents resetting passwords: [Resetting User Passwords \(Video\)](https://www.youtube.com/watch?v=CokNL8aw6hA).

**Note:**

-   You must clear the **Public access** property to enable the service desk-assisted process. See [Configure your Password Reset process](t_CreateAPasswordResetProcess.md).
-   You can perform this activity on a mobile device.
-   You can change the theme of the service desk page to the dark theme. For more information about the dark theme, see [Exploring themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Role required: password\_reset\_admin or password\_reset\_service\_desk

## About this task

In a service desk-assisted Password Reset process, only the service desk agents with the password\_reset\_service\_desk role can reset user passwords. Users can’t reset passwords.

## Procedure

1.  Navigate to **All** &gt; **Password Reset** &gt; **Service Desk**.

2.  Select a user and the Password Reset process to use.

3.  Click **Verify Identity**.

4.  On the Verify Identity form, enter the answers provided by the user, and then click **Continue**.

    If the user's identity is verified, the Reset Password form displays the identity verification and status of the account lock.

5.  Perform one of the following actions.

    -   If the user isn’t locked, the form displays the **Reset password** button. Enter the new password and click **Reset password**.
    -   If the user's account is locked, the form displays the **Reset password** and **Unlock account** buttons. You can enter a new password and click **Reset password** to reset the password and unlock the account. If the **Enable account unlock** option is selected for the password process, you can unlock the account without resetting the password by clicking **Unlock account**.
6.  To reset the password for a different user, you must first navigate away from the **Service Desk** and then navigate to **Password Reset** &gt; **Service Desk**.


-   **[View user requests for password reset](t_ResetARequest.md)**  
The **Reset Requests** module displays the status of each password reset request from the Password Reset Request table \[pwd\_reset\_request\].
-   **[Unblock a Password Reset user](t_UnblockAUser.md)**  
If a user is manually banned or is flagged as exceeding max attempts, the user can be blocked \(not allowed to use the Password Reset application\). You can unblock a blocked user.

**Parent Topic:**[Configuring Password Reset](../concept/password-reset-admin-guide.md)

