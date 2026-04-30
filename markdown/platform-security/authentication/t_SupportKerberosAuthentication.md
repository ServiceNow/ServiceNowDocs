---
title: \(Workaround\) Support Kerberos authentication
description: A workaround is available for the SAML 2.0 integration that changes the authentication context from forms-based authentication to Windows-based authentication.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# \(Workaround\) Support Kerberos authentication

A workaround is available for the SAML 2.0 integration that changes the authentication context from forms-based authentication to Windows-based authentication.

## Before you begin

Role required: admin

## About this task

Currently, the SAML 2 integration uses a PasswordProtectedTransport or "forms-based authentication" authentication context. This authentication context requires the IdP to present users with a form for authentication credentials. With Kerberos, a SAML session is already active through an established Windows login, so the user does not need to authenticate with the IdP.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Open the **SAML2 Update1** IdP record.

3.  Set the **The AuthnContextClassRef method that we will be included in our SAML 2.0 AuthnRequest to the Identity Provider** to one of the following:

<table id="table_kqd_rzg_cs"><tbody><tr><td>

`urn:oasis:names:tc:SAML:2.0:ac:classes:PasswordProtectedTransport` \(Default\)

</td></tr><tr><td>

`urn:federation:authentication:windows`

</td></tr></tbody>
</table>4.  Click **Update**.


