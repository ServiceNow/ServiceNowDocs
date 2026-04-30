---
title: Sample SAML 2 responses after the update
description: The following sections illustrate the new required elements and attributes that the IdP should provide in the SAML Response.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Update your existing SAML 2.0 integration, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Sample SAML 2 responses after the update

The following sections illustrate the new required elements and attributes that the IdP should provide in the SAML Response.

## Sample SAML 2 Response with Issuer Element

The following SAML 2 response uses the Issuer element.

```
<samlp:Responsexmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"  Destination="https://demoi2.service-now.com/navpage.do"  ID="s28da6774c88ae1eab292bf25fe625db81919d8e1e"  InResponseTo="SNC841720c227c81948cfd68cadcad235c6"  IssueInstant="2012-01-30T20:07:10Z"  Version="2.0"><saml:Issuer xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion">http://idp.ssocircle.com</saml:Issuer>
   ...
   <saml:Assertion xmlns:saml="urn:oasis:names:tc:SAML:2.0:assertion"     ID="s2f347f973c063836cf70ea38302d94976f9c5b851"     IssueInstant="2012-01-30T20:07:10Z"     Version="2.0"><saml:Issuer>http://idp.ssocircle.com</saml:Issuer>
      ...
   </saml:Assertion></samlp:Response>
```

## Sample SAML 2 Response with the SubjectConfirmation and SubjectConfirmationData Elements

The following SAML 2 response uses the SubjectConfirmation and SubjectConfirmationData elements with the NotOnOrAfter and Recipient attributes.

```
<saml:SubjectConfirmationMethod="urn:oasis:names:tc:SAML:2.0:cm:bearer"><saml:SubjectConfirmationData InResponseTo="SNC841720c227c81948cfd68cadcad235c6"     NotOnOrAfter="2012-01-30T20:17:10Z"     Recipient="https://demoi2.service-now.com/navpage.do"/></saml:SubjectConfirmation>
```

## Sample SAML 2 Response with the AudienceRestrictions and Audience Elements

The following SAML 2 response uses the AudienceRestrictions and Audience elements with the NotBefore and NotOnOrAfter attributes.

```
<saml:ConditionsNotBefore="2012-01-30T19:57:10Z"  NotOnOrAfter="2012-01-30T20:17:10Z"><saml:AudienceRestriction><saml:Audience>https://demoi2.service-now.com</saml:Audience></saml:AudienceRestriction></saml:Conditions>
```

