---
title: \(Optional\) Enable providing an authentication context class for SAML
description: You can enable the instance to send an authentication context class request to the IdP containing your instance's preferred authentication request format.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Provider \(SP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# \(Optional\) Enable providing an authentication context class for SAML

You can enable the instance to send an authentication context class request to the IdP containing your instance's preferred authentication request format.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

If you enable creating an AuthContextClass message, then you must also specify an authentication context class reference format.

**Note:** Some IdP's do not allow the Service Provider to set the authentication context class. Disabling this setting allows the IdP to choose the authentication context class.

## Procedure

1.  From the property Create an AuthnContextClass request in the AuthnRequest statement, select **Yes** to specify a particular context class such as Password Protected Transport, or select **No** to have the IdP select the most appropriate context class.

2.  If you selected **Yes** to Create an AuthnContextClass request in the AuthnRequest statement, then in The AuthnContextClassRef method that we will request in our SAML 2.0 AuthnRequest to the Identity Provider property, enter the URN of the context class you want to use for authentication \(see table\).

    |Authentication type|Authentication context class URN|
    |-------------------|--------------------------------|
    |Forms-based authentication|`urn:oasis:names:tc:SAML:2.0:ac:classes:PasswordProtectedTransport`|
    |Kerberos-based authentication|`urn:federation:authentication:windows`|

    By default, the integration uses a Password Protected Transport authentication method.

3.  Click **Update**.


