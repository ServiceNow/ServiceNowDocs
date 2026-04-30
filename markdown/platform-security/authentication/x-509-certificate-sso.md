---
title: X.509 certificates for SAML
description: Store and activate the necessary IdP certificates for your SAML configuration.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [SAML 2.0 configuration using Multi-Provider SSO, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# X.509 certificates for SAML

Store and activate the necessary IdP certificates for your SAML configuration.

The X.509 certificates are the IdP certificates that a SAML configuration uses. After you install a certificate, you can add as many certificates as necessary. When there are multiple certificates, the system uses the first active certificate that is found. If you set the URL for the **Metadata URL from which IDP properties are imported field**, the system automatically polls the IdP for a current, valid certificate when your certificate is no longer valid. It appends this certificate to your instance, and uses it for your active SAML configuration.

**Note:** Polling occurs if the IdP is accessible outside of your network.

![X.509 certificates](../image/x-509-certificate-saml.png)

