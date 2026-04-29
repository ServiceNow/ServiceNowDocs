---
title: Values in the User table field for SAML
description: Ensure that the integration's User table field contains appropriate matching values.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a NameID policy for SAML, Service Provider \(SP\) system properties, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Values in the User table field for SAML

Ensure that the integration's User table field contains appropriate matching values.

For example, if the integration uses the email field as the `NameID` token, ensure that the instance lists the same email address as the IdP. The integration fails to authenticate any user who does not have a matching value for the `NameID` token.

