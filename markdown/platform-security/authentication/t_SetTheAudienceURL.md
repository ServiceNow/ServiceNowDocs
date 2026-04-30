---
title: Set the audience URL for SAML
description: Enable your instance to verify that it is the intended recipient of a SAML response by using the Audience property.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service Provider \(SP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Set the audience URL for SAML

Enable your instance to verify that it is the intended recipient of a SAML response by using the Audience property.

## Before you begin

Role required: admin

## About this task

The integration verifies that each SAML response contains the same URL listed in this system property as the URL listed in the Audience element. For example:

```
<samlp:Responsexmlns:samlp="urn:oasis:names:tc:SAML:2.0:protocol"  ID="s2cdc74f37f923e26fe1aeec42b70a93d24230334f"  InResponseTo="90AA6073F01567BFB0DF194F596314E2"  Version="2.0"  IssueInstant="2010-04-29T23:21:51Z"  Destination="https://dloomac.service-now.com/navpage.do">
...
<saml:Conditions NotBefore="2012-01-30T19:57:10Z"  NotOnOrAfter="2012-01-30T20:17:10Z"><saml:AudienceRestriction><saml:Audience>https://demoi2.service-now.com</saml:Audience></saml:AudienceRestriction></saml:Conditions>
...
</samlp:Response>
```

## Procedure

1.  Navigate to **All** &gt; **SAML 2 Single Sign-on** &gt; **Properties**.

2.  In the property The audience uri that accepts SAML2 token. \(Normally, it is your instance URI. For example: https://&lt;instance name&gt;.service-now.com.\), enter the URL of your instance.

    For example, https://demoi2.service-now.com. This URL must match the value of the Audience element in the SAML Response.

3.  Click **Update**.


