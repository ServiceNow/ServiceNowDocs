---
title: Replacing a missing certificate for SAML
description: If the Certificate module displays a blank page, the SAML 2.0 certificate record has been deleted. You can replace the missing certificate by manually creating a certificate record.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Install the identity provider certificate, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Replacing a missing certificate for SAML

If the **Certificate** module displays a blank page, the SAML 2.0 certificate record has been deleted. You can replace the missing certificate by manually creating a certificate record.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Create a new record called `SAML 2.0`.

    **Important:** You MUST use this name. This requirement is only true if you are not using [Multi-Provider Single sign-on \(SSO\)](../../single-sign-on/concept/c_MultipleProviderSingleSignOn.md).

3.  Click **SAML 2 Single Sign-on** &gt; **Certificate**.

4.  In the PEM Certificate field, enter the value of the `ds:X509Certificate` element from your IdP's metadata.

5.  Click **Save**.


