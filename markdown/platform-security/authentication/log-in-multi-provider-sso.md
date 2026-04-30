---
title: Log in using Multi-Provider SSO
description: The recommended and most efficient method for users to log in using Multi-Provider SSO is to use a specifically configured URL.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Log in using Multi-Provider SSO

The recommended and most efficient method for users to log in using Multi-Provider SSO is to use a specifically configured URL.

## Before you begin

Role required: admin

## About this task

After multi-provider SSO is configured, you can send a URL to your users with the correct IdP in the parameter string. For example:

**/login\_with\_sso.do?glide\_sso\_id=&lt;sys\_id of the sso configuration&gt;**

After a user successfully logs in to the IdP page, a cookie containing the IdP sys\_id is added to the browser. The next time the user attempts to log in, the system redirects the user to log in to the IdP server, which automatically logs in to the instance.

If a URL parameter is not set or the browser cache has been cleared, users can also do the following:

## Procedure

1.  Click the **Use external login** link on the login page.

    The external login page appears. Users can click **Use local login** to return to the standard login page.

2.  Enter the value for the specified field on the user table that you configured in Multi-Provider SSO properties.

    The user is redirected to the IdP server, where they log in.


## Result

After users successfully log in to an IdP, they are automatically redirected to that IdP whenever they attempt to access the instance. To have a user access a different IdP, send the user a URL with the new IdP information in the parameter. The new IdP overwrites the old IdP in the cookie if the user successfully logs in. If the user does not log in successfully, the old IdP information is retained in the cookie.

