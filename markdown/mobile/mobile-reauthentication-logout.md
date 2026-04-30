---
title: Configure mobile re-authentication logout option
description: Configure this parameter to force your users to log out each time before they re-authenticate.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure mobile re-authentication system properties, Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile re-authentication logout option

Configure this parameter to force your users to log out each time before they re-authenticate.

## Before you begin

Only configure this property if **glide.authenticate.reauth.login.method** is set to `sso`.

Make sure to select `Global` as the application scope.

**Note:** Note: Some SSO identity providers may require users to be logged out before successfully enabling a re-authentication flow. Use the property **glide.authenticate.reauth.logout.first**, to force users to log out, before re-authentication.

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the Filter Navigator.

2.  Select **New** in the System Property table.

3.  In the form, match the following values:

<table id="table_tgg_45x_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.authenticate.reauth.logout.first**

</td></tr><tr><td>

Type

</td><td>

`true | false`

</td></tr><tr><td>

Value

</td><td>

`true` - Users are forced to log out each time before re-authenticating.`false` - Users are not forced to log out before re-authenticating.

</td></tr></tbody>
</table>
**Parent Topic:**[Configure mobile re-authentication system properties](../concept/mobile-reautentication-concept.md)

