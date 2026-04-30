---
title: Install a service provider keystore for signing SAML requests
description: Use the following steps to remove the existing example key store and install your own Service Provider key store containing your public and private key pair.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [\(Optional\) Set keystore properties for signing logout requests for SAML, Service Provider \(SP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Install a service provider keystore for signing SAML requests

Use the following steps to remove the existing example key store and install your own Service Provider key store containing your public and private key pair.

## Before you begin

Role required: admin

## Procedure

1.  [Create a Service Provider key store](t_CreatingAServiceProviderKeyStore.md).

2.  Navigate to **SAML 2 Single Sign-on** &gt; **Certificate** or **Multi-provider** &gt; **Administrator** &gt; **x509 Certificate**.

3.  Click **SAML 2.0 Keystore\_Key2048\_SHA256**.

4.  Click the **Manage Attachments** link.

5.  Select the Delete checkbox next to saml2sp\_key2048withsha256.jks.

6.  Click **Remove**.

7.  Click **Choose Files** and select the Keystore containing your signed certificates.

8.  Click **Attach**.

9.  Close the Attachments popup.

    **Note:** It is recommended to provide different name for the certificate that is attached newly.

10. In Key store password, enter the password to access the SAML 2 alias.

11. Click **Update**.


