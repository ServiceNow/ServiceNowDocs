---
title: \(Optional\) Enable signed logout requests
description: Some IdPs require the Service Provider to sign logout requests with a certificate.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identity Provider \(IdP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# \(Optional\) Enable signed logout requests

Some IdPs require the Service Provider to sign logout requests with a certificate.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

If your IdP requires signed logout requests, use the IdP's metdata to set the following system properties.

## Procedure

1.  In the **Advanced** tab, from the property Sign LogoutRequest. Set this property to true if the Identity Provider's SingleLogoutRequest service requires signed LogoutRequest, select **Yes** to specify that your IdP requires a signed logout request, or select **No** to use unsigned logout requests.

2.  If you selected **Yes** to Sign LogoutRequest, then in The protocol binding for the Identity Provider's SingleLogoutRequest service. \(Value can be either "urn:oasis:names:tc:SAML:2.0:bindings:HTTP-Redirect" or "urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST".\) property, enter the one of the supported values listed in `Binding` attribute from the`SingleLogoutService` element.

    By default, the integration uses an HTTP-Redirect binding.

3.  Click **Update**.

4.  [Install a Service Provider \(SP\) key store](t_InstallASPKeystoreSigningSAMLReqs.md).


