---
title: Managing user sessions
description: The ServiceNow AI Platform provides the ability to view and terminate individual user sessions, lock out users from the system, and make users inactive.Secure your instance by enforcing a maximum time for sessions regardless of user activity.Specify when to time out user sessions after a period of inactivity.Configure how much time users have to extend a session before it times out due to inactivity.Lock out a user when you don’t want the user to access the instance.You can mark a user inactive so the user doesn't show up in any fields that reference active users on the User table.You can terminate a user session, for example, if you’re going to perform system maintenance and users are still logged in.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Monitoring user activity, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Managing user sessions

The ServiceNow AI Platform provides the ability to view and terminate individual user sessions, lock out users from the system, and make users inactive.

Regardless of the number of windows you have open in a browser, it’s considered to be one session. However, if you have two separate browsers open \(such as Google Chrome and Safari\), it’s considered to be two separate sessions.

-   Terminating a user session effectively logs that user out of the next transaction, which is usually the next browser select. Use the terminate sessions feature when you want to perform system maintenance.
-   Locking a user out of the system means they can no longer log in or generate any actions from any email messages that they send to the instance. Locking users out also terminates their sessions.
-   Making a user inactive means they don't show up in any fields that reference active users on the **User** table.

**Parent Topic:**[Monitoring user activity](../../roles/concept/user-admin-tools-landing.md)

## Configure a maximum active time for user sessions

Secure your instance by enforcing a maximum time for sessions regardless of user activity.

### Before you begin

Role required: admin

### About this task

By default, sessions expire only after a period of inactivity. Enforcing a maximum active session time ends sessions regardless of whether a user has been active recently, including whether they recently selected to extend a session. The active session timeout should be greater than the value configured for the inactive session timeout. For example, if sessions are configured to time out after 30 minutes of inactivity, the active session timeout should be greater than 30 minutes.

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Filter the System Properties \[sys\_properties\] list for the following properties and then select a property to open its record.

    -   **glide.ui.active.session.life\_span**: Sets the maximum session time for authenticated user sessions regardless of user activity. Authenticated users are logged out of the instance after the time specified and must enter their credentials again to access the instance.
    -   **glide.guest.active.session.life\_span**: Sets the maximum session time for guest user sessions regardless of user activity. This setting helps secure an instance using applications that involve guest user sessions, such as Agent Chat.
3.  In the **Value** field, enter the number of minutes before the session times out regardless of user activity.

    The value should be greater than the value of the corresponding properties for an inactive session timeout: **glide.ui.session\_timeout** for authenticated users or **glide.guest.session\_timeout** for guest users. By default, the inactive session timeout for both authenticated and guest users is 30 minutes.

4.  Select **Update**.


**Related topics**  


[Configure a maximum active time for integration sessions](../../../integrate/concept/managing-integration-sessions.md#)

## Modify user session timeout after inactivity

Specify when to time out user sessions after a period of inactivity.

### Before you begin

Role required: admin

### About this task

By default, after 30 minutes of inactivity in the application, the platform logs the user out automatically, unless the **Remember Me** check box in the login screen is selected. Making the interval longer can lead to the unnecessary maintenance of inactive sessions in memory. Adjust this timeout setting to no more than a few hours, although up to 24 hours is workable.

**Note:**

-   Ajax calls to the server keep the session alive \(such as Labels and Refreshing dashboards\).
-   Polling keeps the session alive when the chat desktop is open \(requires the Chat plugin\).

### Procedure

1.  Clear the **Remember Me** check box in the login screen.

2.  In the navigation filter, enter `sys_properties.list`.

3.  From the System Property \[sys\_properties\] list, search for **glide.ui.session\_timeout**.

4.  If **glide.ui.session\_timeout** doesn’t exist, select **New** to add a new property using the following values:

    -   **Name**: **glide.ui.session\_timeout**
    -   **Description**: Type a brief description. In this case, enter something like `Override the default session timeout (30). This value is in minutes`.
    -   **Type**: Select the appropriate data type. In this case, select **Integer**.
    -   **Value**: Change the default value from 30 minutes to a value of your choice.
    **Note:** The session timeout can also be set through installation exit customizations.


### What to do next

Administrators may also want to add the following properties to the System Properties table.

-   **glide.security.csrf.handle.ajax.timeout**: Handles errors for timed out Ajax requests when set to **true**.
-   **glide.security.auto.resubmit.ajax**: Automatically resubmits timed-out Ajax requests when set to **true** and the [Log in to an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/t_LoggingIn.md) check box is selected or [Change the default value of the Remember me check box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/c_ChSetRemMeChkbxCookie.md). A pop-up appears to users asking them to continue.
-   **glide.ui.auto\_req.extend.session**: When set to **true**, the system automatically extends a user's session by the value they select for the homepage refresh time. If there’s no homepage refresh time, the standard timeout value applies. Tablet and mobile devices don’t support this property. When set to **false**, user sessions time out when the **Remember me** check box is clear. The timeout is based on whether there’s a homepage refresh time. When there’s no homepage refresh time, the standard timeout value applies. When there’s a homepage refresh time, the user session times out after the timeout value plus one interval of the homepage refresh time. For example, if a user selects a refresh interval of five minutes, then that session expires after the timeout value plus five minutes.

    **Note:** Users who select the **Remember me** check box are unaffected by session timeout properties.


Administrators can also add the following properties to configure additional timeout settings for user sessions. These additional settings help to conserve system resources:

-   **glide.session.unauthorized.timeout.enabled**: Enables an alternate session timeout for unauthenticated, guest sessions. Guest sessions are created for HTTP requests to the instance that don’t contain authentication information. By default this property is set to **true**.
-   **glide.unauthorized.session\_timeout**: Specifies the time, in minutes, after an authenticated user logs out of an instance before the session ends. Set the property to a value greater than **0** and less than the value in the **glide.ui.session\_timeout** property.

**Related topics**  


[Modify integration session timeout after inactivity](../../../integrate/concept/managing-integration-sessions.md#)

## Prompting users to extend a session

Configure how much time users have to extend a session before it times out due to inactivity.

### Before you begin

Role required: admin

### About this task

By default, users are prompted to extend their session two minutes before it expires with an "Extend your session" dialog box. This procedure explains how to adjust the timing of when users are presented with this prompt.

### Procedure

1.  Navigate to **All**, and then enter `sys_properties.list` in the navigation filter.

2.  Open the **glide.ui.session\_timeleft** property.

3.  In the **Value** field, enter the number of minutes before the session timeout to prompt users to extend their session.

    Setting the value to zero turns off prompting users to extend their sessions.

4.  Select **Update**.


## Lock out a user

Lock out a user when you don’t want the user to access the instance.

### Before you begin

Role required: user\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and select the user from the list.

2.  Select the **Locked Out** check box, and update the record.


## Mark a user inactive

You can mark a user inactive so the user doesn't show up in any fields that reference active users on the **User** table.

### Before you begin

Role required: admin

### About this task

**Note:** By default, when you mark a user inactive, you lock out that user. The **Lock Out Inactive Users** business rule governs this behavior.

If you clear the **Active** checkbox, the user is locked out and cannot access the instance. This functionality is controlled through a Glide property **glide.authenticate.only.allow.active.user.login** which will only allow the active users to access the instance.

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and select the user from the list.

2.  Clear the **Active** check box, and update the record.


## Terminate a user session

You can terminate a user session, for example, if you’re going to perform system maintenance and users are still logged in.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Logged in users**.

    You can only see users who are logged in to the same application node as you. If the Active field on a user record value is false, the user is logged in but not currently running a transaction. Most users appear as inactive at any given time.

2.  Select the session that you want to end.

3.  Select **Lock Out Session**.

    The session is terminated, and the user is redirected to the login page at the next attempted transaction. The user isn’t locked out. Multiple user sessions may be associated with one user. Terminating a user session only affects the specific session.

    **Note:** Mobile user sessions can’t be terminated using this process.


