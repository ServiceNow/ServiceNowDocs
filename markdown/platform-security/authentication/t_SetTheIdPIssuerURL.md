---
title: Set the IdP issuer URL
description: Provide the URL to the IdPs who will issue the security token.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Identity Provider \(IdP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Set the IdP issuer URL

Provide the URL to the IdPs who will issue the security token.

## Before you begin

Role required: admin

## About this task

The integration verifies that each SAML response contains the same URL listed in this system property as the URL listed in the Issuer element. For example:

```
<samlp:Responsexmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"  Destination="https://demoi2.service-now.com/navpage.do"  ID="s28da6774c88ae1eab292bf25fe625db81919d8e1e"  InResponseTo="SNC841720c227c81948cfd68cadcad235c6"  IssueInstant="2012-01-30T20:07:10Z"  Version="2.0"><saml:Issuer xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">http://idp.ssocircle.com</saml:Issuer>
   ...
   <saml:Assertion xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion"     ID="s2f347f973c063836cf70ea38302d94976f9c5b851"     IssueInstant="2012-01-30T20:07:10Z"     Version="2.0"><saml:Issuer>http://idp.ssocircle.com</saml:Issuer>
      ...
   </saml:Assertion></samlp:Response>
```

## Procedure

1.  Navigate to **All** &gt; **SAML 2 Single Sign-on** &gt; **Properties**.

2.  In the property The Identity Provider URL which will issue the SAML2 security token with user info., enter the URL to your IdP.

    Each IdP URL must be unique. By default, the integration contains the URL to SSOCircle. For more information, see [http://idp.ssocircle.com](http://idp.ssocircle.com/).


