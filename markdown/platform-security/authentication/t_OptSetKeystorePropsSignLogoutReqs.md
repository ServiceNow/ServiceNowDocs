---
title: \(Optional\) Set keystore properties for signing logout requests for SAML
description: Set the keystore properties to enable the integration to sign logout requests by using your signed server and signed CA certificates.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Provider \(SP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# \(Optional\) Set keystore properties for signing logout requests for SAML

Set the keystore properties to enable the integration to sign logout requests by using your signed server and signed CA certificates.

## Before you begin

Role required: admin

## Procedure

1.  In the property The alias of key entry stored in SAML 2.0 SP Keystore used to sign SAML 2 requests, enter the alias name that you created for the SAML 2.0 Keystore.

    By default, the integration looks for the alias saml2sp.

2.  In the property The password of key entry stored in SAML 2.0 SP Keystore used to sign SAML 2 requests, enter the password for your SAML 2.0 Keystore.

    By default, the password is the same as the default alias name.

3.  Click **Update**.

4.  Regenerate your SP metadata.

    For more information, see [SP metadata](t_GenerateServiceNowSPMetadata.md).


