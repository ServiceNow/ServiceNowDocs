---
title: Configure mobile re-authentication login method
description: Define the re-authentication method to be either single sign-on \(SSO\) or local login, depending on your security requirements.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Re-authentication, System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile re-authentication login method

Define the re-authentication method to be either single sign-on \(SSO\) or local login, depending on your security requirements.

## Before you begin

Make sure to select `Global` as the application scope.

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the filter navigator.

2.  Select **New** in the System Property table.

3.  In the form, match the following values:

<table id="table_tgg_45x_xfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.authenticate.reauth.login.method**

</td></tr><tr><td>

Type

</td><td>

string

</td></tr><tr><td>

Value

</td><td>

`sso` - To use single sign-on

 `db` - To use local login

</td></tr></tbody>
</table>
**Parent Topic:**[Configure mobile re-authentication system properties](mobile-reautentication-concept.md)

