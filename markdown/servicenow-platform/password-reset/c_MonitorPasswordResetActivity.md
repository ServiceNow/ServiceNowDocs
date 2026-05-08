---
title: Password Reset and Password Change reports and logs
description: The Password Reset application provides several tools for monitoring and troubleshooting password reset activities.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Password Reset reference, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Password Reset and Password Change reports and logs

The Password Reset application provides several tools for monitoring and troubleshooting password reset activities.

Users with the password\_reset\_credential\_manager or password\_reset\_admin role can view the status of password reset activities, identify potential security threats, and monitor for compliance with password security policies.

The **Reset Requests**, **Activity Log**, and **Blocked Users** modules are useful for monitoring password reset activities and for troubleshooting password reset issues. They also provide access to more detailed information than is provided on the Overview module.

To make room for new data, the system periodically purges the data that is used for password reset monitoring and reporting.

## Password Reset Overview module

The **Password Reset** &gt; **Overview** module displays reports on password reset and password change activities. Users with the password\_reset\_admin role can customize the layout of the reports that appear in the Overview module.

|Title|Description|
|-----|-----------|
|Password Requests \(last 7 days\)|Number of password reset requests by type during the last 7 days.|
|Blocked Users \(last 7 days\)|Number of users blocked over the last 7 days.|
|Password Reset Request Status \(last 7 days\)|Status of all password reset requests by process.|
|Password Reset Request by Action \(last 30 days\)|Number of password reset requests by action type: **Reset Password**, **Unlock Account**, or **Reset and Unlock**.|
|Password Reset Top Users \(last 30 days\)|Number of password reset requests per user. Many password reset requests from a single user could indicate a security issue.|
|Password Reset Failed Verifications \(last 7 days\)|Number of failed verification attempts, by verification instance. A failed verification occurs when a user attempts to reset the password, but fails for one reason or another, during the identity verification step. Many failed verification attempts for a specific type of verification could indicate that the process is too complicated or unclear.|
|Password Reset Enrollment By Verification|Number of users by verification type who enrolled and did not enroll in the password reset program. A large number for users who did not enrolled could indicate a compliance or communication issue within the organization.|
|Password Change Top Users \(last 30 days\)|Number of password change requests per user. Many password change requests from a single user could indicate a security issue.|

## Password Reset activity log

The activity log \(**Password Reset** &gt; **Activity Log**\) provides detailed information that you can use to troubleshoot and to generate reports on password reset metrics. Information contained in the activity log is stored in the Password Reset activity log \[pwd\_reset\_activity\] table.

You must have the password\_reset\_credential\_manager or password\_reset\_admin role to view the log.

## Password Reset event log

The event log is a valuable resource for troubleshooting. On the **Start** menu, click **Programs \(or All Programs\)** &gt; **Administrative Tools** &gt; **Event Viewer**.

If the log does not appear, then, on the **Windows Logs** menu, click **Applications** &gt; **Service Logs**.

You must have the admin role to view the log.

## To write to the Password Reset event log

Edit the `DebugFlag` registry key entry at: `Computer > HKEY_LOCAL_MACHINE > SOFTWARE > Microsoft > Windows > CurrentVersion > Authentication > Credential Providers > {B6EFF27D-C1C4-481F-B81B-F3547C47D58A}`

By default, the key is set to 0. Set the key to 1 to write log entries to the `ServiceNowPwdReset` event log.

You must have the password\_reset\_credential\_manager or password\_reset\_admin role to write to the log.

## Password Reset blocked user notification

You can receive email notifications when the number of users that are blocked or locked exceeds the password blocked threshold. Notifications can alert you to suspicious activities. The default threshold is 10.

To subscribe: Add an email notification device or modify an existing device and then subscribe to the **Password Reset-Activity Monitor Lockout** notification.

You must have the password\_reset\_credential\_manager or password\_reset\_admin role to subscribe.

## Schedule for purging Password Reset data

To make room for new data, the system periodically purges the data that is used for password reset monitoring and reporting. Information contained in reports and monitoring tools could change dramatically immediately after a data purge.

Users with the password\_reset\_credential\_manager or password\_reset\_admin role can follow this procedure to modify the purge interval:

1.  On a non-production instance: Navigate to **Automated Test Framework** &gt; **Administration** &gt; **Table Cleanup**.
2.  Modify the designated tables.
3.  Test all changes on the non-production instance.
4.  Modify the tables on your production instance and test.

Alternatively, contact ServiceNow Technical Support to modify the purge interval.

<table id="table_wm3_fyh_kp"><thead><tr><th>

Table name

</th><th>

Purge interval

</th></tr></thead><tbody><tr><td>

\[pwd\_reset\_request\]

</td><td>

90 days \(7,776,000 seconds\). Depending on your organizational data monitoring requirements, you could configure the rule to:

-   Purge successful requests after 90 days
-   Keep failed requests for 120 days

</td></tr><tr><td>

\[pwd\_user\_lockout\]

</td><td>

90 days \(7,776,000 seconds\). Depending on your organizational data monitoring requirements, you could configure the rule to:

-   Purge successful requests after 90 days
-   Keep failed requests for 120 days

</td></tr><tr><td>

\[pwd\_reset\_activity\]

</td><td>

90 days \(7,776,000 seconds\).

</td></tr><tr><td>

\[pwd\_activity\_monitor\]

</td><td>

90 days \(7,776,000 seconds\).

</td></tr><tr><td>

\[pwd\_dvc\_enrollment\_code\]

</td><td>

1 day \(86,400 seconds\).

</td></tr><tr><td>

\[pwd\_sms\_code\]

</td><td>

1 day \(86,400 seconds\).

</td></tr></tbody>
</table>**Related topics**  


[Password Reset and Password Change reports and logs](c_MonitorPasswordResetActivity.md)

[Unblock a Password Reset user](../task/t_UnblockAUser.md)

[View user requests for password reset](../task/t_ResetARequest.md)

[Unblock a Password Reset user](../task/t_UnblockAUser.md)

