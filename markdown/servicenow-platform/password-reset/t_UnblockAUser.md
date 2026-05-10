---
title: Unblock a Password Reset user
description: If a user is manually banned or is flagged as exceeding max attempts, the user can be blocked \(not allowed to use the Password Reset application\). You can unblock a blocked user.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reset a password or unlock a user account with service desk assistance, Configuring Password Reset, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Unblock a Password Reset user

If a user is manually banned or is flagged as exceeding max attempts, the user can be blocked \(not allowed to use the Password Reset application\). You can unblock a blocked user.

## Before you begin

Role required: password\_reset\_admin or password\_reset\_service\_desk

## About this task

Blocking events include:

-   The user exceeded the limit for the number of failed password attempts.
-   The most recent password reset occurred before the wait time required until the next reset.
-   The user failed to provide the correct information while attempting to reset the password.

If the number of blocked or locked users exceeds the limit within a defined time interval, it triggers a system log event. You can configure the number of blocked or locked users and the time interval required to generate the log event by setting the password\_reset.activity\_monitor.incident\_threshold and password\_reset.activity\_monitor.incident\_window properties.

## Procedure

1.  To view the list of blocked users, navigate to **Password Reset** &gt; **Blocked Users**.

2.  To unblock a self-service user:

    1.  Navigate to **Password Reset** &gt; **Blocked Users**.

    2.  Select a user from the list.

    3.  Select **Delete** on the **Actions on selected rows** list.

3.  To unblock a user whose password was reset by a service desk agent:

    If a user is manually banned or flagged as exceeding max attempts, the user can be blocked \(not allowed to use the Password Reset application\). When the password reset request is made through self-service, the user is unblocked when the password is successfully reset.

    In contrast, service desk agents are allowed any number of retries. The max\_attempt\_reached limit does not apply and the **Blocked** status for the user is not reset after the password is reset. As a result, after you successfully reset a user password, you must unblock the user manually.

    If the user is not unblocked manually, then the system resets the blocked state only when the max\_attempt\_window time period elapses and the user tries to reset the password using self-service.

    1.  After you successfully reset a user password, navigate to **Password Reset** &gt; **Blocked Users**.

    2.  Change the **Blocked** setting for the user from true to false.


**Parent Topic:**[Reset a password or unlock a user account with service desk assistance](reset-password-for-user.md)

**Related topics**  


[Password Reset and Password Change reports and logs](../concept/c_MonitorPasswordResetActivity.md)

[Configure Password Reset properties](t_SetPwdResetProps.md)

[Password Reset and Password Change reports and logs](../concept/c_MonitorPasswordResetActivity.md)

