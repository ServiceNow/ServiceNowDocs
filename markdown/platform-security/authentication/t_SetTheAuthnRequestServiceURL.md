---
title: Set the AuthnRequest service URL
description: Using the IdP's metadata, set the request service URLs for the integration's IdP.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Identity Provider \(IdP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Set the AuthnRequest service URL

Using the IdP's metadata, set the request service URLs for the integration's IdP.

## Before you begin

Role required: admin

## Procedure

1.  In the property The base URL to the Identity Provider's AuthnRequest service. The AuthnRequest will be posted to this URL as the SAMLRequest parameter, enter the URL to the HTTP-Redirect binding obtained from the `SingleSignOnService` element.

2.  Select the check box next to Sign AuthnRequest to enable the Identity Provider's single-sign on service to receive a signed AuthnRequest.

3.  In the property When SAML 2.0 single sign-on fails because the session is not authenticated, or this is the first login, redirect to this URL. This is the base URL where the initial SAML 2.0 AuthnRequest is sent using the SAMLRequest parameter, enter the URL to the HTTP-Redirect binding obtained from the `SingleSignOnService` element.

    By default, the integration contains the URL to the SSOCircle service.


