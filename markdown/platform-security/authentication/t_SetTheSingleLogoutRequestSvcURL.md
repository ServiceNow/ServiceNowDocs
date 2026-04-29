---
title: Set the SingleLogoutRequest service URL
description: Set the request service URLs for the integration's IdP by using the IdP's metadata.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identity Provider \(IdP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Set the SingleLogoutRequest service URL

Set the request service URLs for the integration's IdP by using the IdP's metadata.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## Procedure

1.  In the The base URL to the Identity Provider's SingleLogoutRequest service. The LogoutRequest will be posted to this URL as the SAMLRequest parameter property, enter the URL obtained from the `SingleLogoutService` element.

    The LogoutRequest is posted to this URL as the SAMLRequest parameter. By default, the integration contains the URL to the SSOCircle service.

2.  In the URL to redirect users after logout, typically back to the portal that enabled the SSO \(e.g. http://portal.companya.com/logout\) property, enter the URL where you want to redirect users after they successfully logout.

    If your IdP uses form-based authentication, enter the URL to your IdP's login form. If your IdP uses a non-form-based authentication method such as Kerberos, you should set the URL to a static logout page. This way, users who log out do not get immediately get redirected to the IdP and login again. By default, the integration contains the URL to the static UI page `external_logout_complete.do`.


