---
title: Set preferences for security event notifications
description: Configure preferences for the types of notifications you want to receive for occurrences of specific security events. For each type, you designate whether to receive notifications by email, by push notification in Now Mobile, or in third party messaging applications such as Slack or Microsoft Teams.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Monitor security events, Instance Security Center, Platform Security]
---

# Set preferences for security event notifications

Configure preferences for the types of notifications you want to receive for occurrences of specific security events. For each type, you designate whether to receive notifications by email, by push notification in Now Mobile, or in third party messaging applications such as Slack or Microsoft Teams.

## Before you begin

To enable third party messaging applications to send security event notifications, you must activate the Messaging Notification \(com.glide.notification.messaging\) plugin. Individual users must configure their own settings. For details, see [Notifications in messaging applications](https://www.servicenow.com/docs/access?context=messaging-integration&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Role required: admin.

## Procedure

1.  In the Instance Security Center home page, click the profile menu, then click **Notification Preferences**.

<table id="table_rpk_b5z_4lb"><thead><tr><th>

Notification preference

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin Login

</td><td>

Send the selected type of notification whenever other users with assigned admin roles log into this instance from a different IP address.

</td></tr><tr><td>

Admin Unlock

</td><td>

Send the selected type of notification whenever an account for a high privilege user has been unlocked.

</td></tr><tr><td>

Failed Login

</td><td>

Send the selected type of notification whenever other users fail to log in into this instance in less than the number of attempts defined in the **glide.user.max\_unlock\_attempts** property. If you don't configure this property, the default value is 5. To learn more about this property, see [Specify lockout for failed login attempts](t_LockoutForFailedLogins.md).

</td></tr><tr><td>

HP Role Added

</td><td>

Send the selected type of notification whenever a high privilege security role \(including oauth\_admin, admin, security\_admin, and impersonator roles\) is granted to another user.To learn more about elevating user security, see [Elevate to a privileged role](t_ElevateToAPrivilegedRole.md) and [Elevated privilege roles](../concept/c_ElevatedPrivilege.md).

</td></tr><tr><td>

Impersonation

</td><td>

Send the selected type of notification whenever another user is impersonating you.To learn more about impersonating users, see [Impersonate a user](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Security Elevation

</td><td>

Send the selected type of notification whenever other users are elevated to a security admin role in this instance.

</td></tr><tr><td>

Weekly Digest

</td><td>

Send a weekly digest on the selected type of notification. It includes:-   A summary all security activities that took place in this instance throughout the week.
-   The current daily compliance score for the instance.


</td></tr></tbody>
</table>2.  For each type of security event, select the appropriate check boxes to designate the type of notifications to send you.

    You can select multiple notification methods for each.

<table id="choicetable_amb_lb4_mnb"><thead><tr><th align="left" id="d28096e215">

Check box

</th><th align="left" id="d28096e218">

Description

</th></tr></thead><tbody><tr><td id="d28096e224">

**Email**

</td><td>

Send an email for this type of security event.

</td></tr><tr><td id="d28096e233">

**Slack**

</td><td>

Send notifications for this type of security event through Slack. **Note:** This column appears only if you have set up Slack integration to the ServiceNow AI Platform.

</td></tr><tr><td id="d28096e254">

**Teams**

</td><td>

Send notifications for this security event through Microsoft Teams.**Note:** This column appears only if you have set up Microsoft Teams integration to the ServiceNow AI Platform.

</td></tr><tr><td id="d28096e275">

**Push**

</td><td>

Send push notifications on Now Mobile for this type of security event. **Note:** This column appears only if you first log into Now Mobile.

</td></tr><tr><td id="d28096e294">

**Select All**

</td><td>

Select a specific type of notification for all types security events. For example, click **Select All** located above **Email** if you want to receive email notifications for each security event type.

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Monitor security events](../concept/instance-sec-center-event-ribbon.md)

