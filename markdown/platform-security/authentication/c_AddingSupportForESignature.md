---
title: Add E-Signature support for SAML
description: Configure the following properties for E-Signature with Security Assertion Markup Language \(SAML\) 2.0 update 1.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Add E-Signature support for SAML

Configure the following properties for E-Signature with Security Assertion Markup Language \(SAML\) 2.0 update 1.

When E-signature is active with Multi-SSO, SAML properties aren’t used. The system adds E-signature properties to the SAML2 Update1 Properties \[saml2\_update1\_properties\] table:

|Property|Description|Default|
|--------|-----------|-------|
|Assertion Consumer Index for eSignature authentication|An index number that identifies the endpoint.|1|
|Assertion Consumer URL for eSignature authentication|The URL that identifies the consumer.|`https://yourinstance.service-now.com/consumer.do`|
|AuthnRequest URL for eSignature Authentication|The URL for authentication|none|

If you’re using E-Signature with SAML 1.0 or SAML 2.0 \(not including update 1\), see the special configuration instructions: [E-signature for Multi-Provider SSO](../../authentication/concept/e-signature-for-multi-provider-sso.md).

**Note:** If you’re a Life Science Customer using E-Signature, deactivate the User self-lockout prevention business rule.

