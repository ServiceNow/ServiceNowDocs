---
title: URL information for an SSO provider
description: During a login challenge resulting from a URL link into the instance that requires an SSO session, the referring URL might need to be supplied to the SSO provider so that after authentication, the URL can be passed back to the instance and linked to the correct resource.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SAML 2.0 concepts, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# URL information for an SSO provider

During a login challenge resulting from a URL link into the instance that requires an SSO session, the referring URL might need to be supplied to the SSO provider so that after authentication, the URL can be passed back to the instance and linked to the correct resource.

![SSO flow with redirect](../image/SSOTargetRedirect.png "SSO Target Redirect")

Installation exit return values have been enhanced to pass a URL instead of, or in addition to the URL defined by the properties. Usually, you would return a username or a predefined string value to control authorize or challenge the SSO session. The following examples show the extended behavior of passing a URL.

```
return "failed_missing_requirement:%26amp;TARGET=https://instance.service-now.com/nav_to.do?uri=incident.do?sys_id=12345";
```

The example above passes the URL `https://instance.service-now.com/nav_to.do?uri=incident.do?sys_id=12345` to the SSO provider in the form of a URL parameter named TARGET.

**Note:** It is assumed that the SSO provider will use that information in the TARGET parameter to redirect back to the instance when the user credentials have been collected and authentication passed.

A colon : demarcates the two return values and an encoded &amp; \(%26amp;\) concatenates the URL defined in the property **glide.authenticate.failed\_missing\_requirement** and the TARGET parameter.

