---
title: Zero Trust Access system properties
description: Use system properties to enable and customize Zero Trust Access to meet your security requirements.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Zero Trust Access, Access Management]
---

# Zero Trust Access system properties

Use system properties to enable and customize Zero Trust Access to meet your security requirements.

## Properties

![Zero Trust Access Properties](../images/session-access-system-properties.png)

<table id="table_vkg_2wf_twb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable Zero Trust Session Access

</td><td>

Option that enables administrators to use the Zero Trust Session Access feature. By default the value is `false`.

</td></tr><tr><td>

Enable debug logging for Zero Trust Session Access

</td><td>

Option to enable debug logging for Zero Trust Session Access.

</td></tr><tr><td>

Preference to remove/limit roles in case of conflict. Whenever a common role is part of both remove and limit role\(s\) set, the precedence is decided based on this property.

</td><td>

**Remove Roles** or **Limit Roles**

</td></tr><tr><td>

The number of days after which session access audit data will be deleted. The default value is 30 days and the maximum is 180 days.

</td><td>

By default, it’s 30 days.

</td></tr><tr><td>

The number of seconds after which the refresh token will be revoked if the session access policy is using IDP attributes. It should be between access token lifespan and refresh token lifespan. The default value is 1800 seconds.

</td><td>

By default, it’s 1800 seconds.

</td></tr><tr><td>

Information to be displayed when some privileges have been removed from the session for a user.

</td><td>

Description that you want to display to your users regarding limiting or removal of privileges. Sample Description:`Based on security policies defined by the administrator, some of your roles have been removed from this session. Please get in touch with your administrator for more information.`

</td></tr></tbody>
</table>