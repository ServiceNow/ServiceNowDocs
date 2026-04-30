---
title: Configure mobile re-authentication SSO login
description: Define which identity provider to use for the SSO login. If this property is not defined, the system reuses the default identity provider used for a regular login.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Re-authentication, System properties, Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile re-authentication SSO login

Define which identity provider to use for the SSO login. If this property is not defined, the system reuses the default identity provider used for a regular login.

## Before you begin

Only configure this property if **glide.authenticate.reauth.login.method** is set to `sso`.

Make sure to select `Global` as the application scope.

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the Filter Navigator.

2.  Select **New** in the System Property table.

3.  In the form, match the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.authenticate.reauth.login.sso\_id**|
    |Type|string|
    |Value|Enter the `sys_id` of the SSO provider as listed in the \[sso\_properties\] table.|


**Parent Topic:**[Configure mobile re-authentication system properties](../concept/mobile-reautentication-concept.md)

