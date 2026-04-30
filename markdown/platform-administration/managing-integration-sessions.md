---
title: Managing integration sessions
description: Manage access to an instance by configuring how long integration sessions last before expiring.Secure your instance by enforcing a maximum time for sessions regardless of integration activity.Specify when to time out integration sessions after a period of inactivity.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration with third-party applications and data sources, Integrations, Configure core features, Administer]
---

# Managing integration sessions

Manage access to an instance by configuring how long integration sessions last before expiring.

Similar to user sessions, you can secure your instance by configuring when to time out an integration session after a period of inactivity and a maximum active session time. By default, integration session time out after five minutes of inactivity.

**Parent Topic:**[Integration with third-party applications and data sources](c_IntegrateWThirdPartyAppsDataSrces.md)

## Configure a maximum active time for integration sessions

Secure your instance by enforcing a maximum time for sessions regardless of integration activity.

### Before you begin

Role required: admin

### About this task

By default, sessions expire only after a period of inactivity. Enforcing a maximum active session time ends sessions regardless of if an integration has been active recently. The active session timeout should be greater than the value configured for the inactive session timeout. For example, if sessions are configured to time out after 30 minutes of inactivity, the active session timeout should be greater than 30 minutes.

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|`glide.active.session.timeout.invalidate.session`|
    |Description|`Specifies whether integration sessions can be invalidated by configuring a maximum active session time.`|
    |Type|**true \| false**|
    |Value|`true`|

4.  Select **Submit**.

5.  From the System Property \[sys\_properties\] list, open the **glide.integrations.active.session.life\_span** property.

6.  In the **Value** field, enter the number of minutes before integration sessions time out regardless of user activity.

    The value should be greater than the value of **glide.integration.session\_timeout** for inactive integration session timeout. By default, the inactive session timeout for integration sessions is five minutes.

7.  Select **Update**.


### Result

Integrations are logged out of the instance after the time specified and their credentials must be entered again to access the instance. This setting helps secure an instance using integrations, such as the REST API.

**Related topics**  


[Configure a maximum active time for user sessions](../../administer/user-sessions/concept/c_ManageUserSessions.md#)

## Modify integration session timeout after inactivity

Specify when to time out integration sessions after a period of inactivity.

### Before you begin

Role required: admin

### About this task

By default, after one minute of inactivity, the platform ends an integration session and logs the user out automatically.

### Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|`glide.integration.session_timeout`|
    |Description|`Sets the inactive session timeout for integration sessions, in minutes.`|
    |Type|**string**|
    |Value|Specify the number of minutes.|

4.  Select **Submit**.


**Related topics**  


[Modify user session timeout after inactivity](../../administer/user-sessions/concept/c_ManageUserSessions.md#)

