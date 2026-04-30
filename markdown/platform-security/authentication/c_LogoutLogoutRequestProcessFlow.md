---
title: Logout \(LogoutRequest\) process flow
description: During logout, the instance issues the SAML 2.0 LogoutRequest service call to the IdP.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAML 2.0 concepts, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Logout \(LogoutRequest\) process flow

During logout, the instance issues the SAML 2.0 LogoutRequest service call to the IdP.

This service logs the user out and then redirects back to the specified logout URL.

![](../image/Saml2Logout.png "SAML 2 Logout")

## User Clicks the Logout Button

The user clicks the **Logout** button and the instance executes the logout script.

## LogoutRequest issued

The logout script constructs a SAML 2.0 `LogoutRequest` and posts it to the preconfigured SingleLogoutRequest SAML 2.0 service at the IdP. The IdP deflates the request and then base64 encodes it. An example `LogoutRequest` looks like this:

```
<saml2p:LogoutRequestxmlns:saml2p="urn:oasis:names:tc:SAML:2.0:protocol"  ID="21B78E9C6C8ECF16F01E4A0F15AB2D46"  IssueInstant="2010-04-28T21:36:11.230Z"  Version="2.0"><saml2:Issuer xmlns:saml2="urn:oasis:names:tc:SAML:2.0:assertion">https://dloomac.service-now.com
	</saml2:Issuer><saml2:NameID xmlns:saml2="urn:oasis:names:tc:SAML:2.0:assertion"          Format="urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress"          NameQualifier="http://idp.ssocircle.com"          SPNameQualifier="https://dloomac.service-now.com/navpage.do">david.loo@service-now.com</saml2:NameID><saml2p:SessionIndex>s211b2f811485b2a1d2cc4db2b271933c286771104
	</saml2p:SessionIndex></saml2p:LogoutRequest>
```

## User Logs Out

The user logs out of the IdP. The IdP redirects back to the instance, which in turns redirects back to the IdP since the user is not logged in.

