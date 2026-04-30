---
title: Install the identity provider certificate
description: You can paste a PEM certificate into a X.509 Certificate form so the identify provider can verify communications with the service provider.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Install the identity provider certificate

You can paste a PEM certificate into a X.509 Certificate form so the identify provider can verify communications with the service provider.

## Before you begin

Role required: admin

## About this task

The IdP's certificate is located within the IdP's metadata. The IdP developer determines where the certificate metadata resides when creating the local IdP.

**Note:** Certificates for single-sign on should always be in PEM format to work with SAML certificates.

## Procedure

1.  Navigate to **All** &gt; **SAML Single Sign-on** &gt; **Certificate**.

2.  Fill in the form fields \(see table\).

3.  Click **Save**.

    ![Pasting in the PEM certificate](../image/X509.png)

    **Note:** The integration does not currently sign the certificate in communications between the instance and the IdP.

    |Field|Description|
    |-----|-----------|
    |Name|The certificate name. Do not change the Name entry. The name of the X.509 certificate must be SAML 2.0 in order for the integration to use it. This requirement is only true if you are not using [Multi-Provider Single sign-on \(SSO\)](../../single-sign-on/concept/c_MultipleProviderSingleSignOn.md).|
    |Expiration notification|Select this option to send a notification to the users selected in the **Notify on expiration** field. By default, this is enabled.|
    |Notify on expiration|Select the users to revive the notification regarding certificate expiration. If no users are selected, the logged in user is added by default, along with the last two logged in users with the administrator role.|
    |Warn in days to expire|The number of days before expiration that the instance send the notification. Enter a value of at least 20. Instances upgraded to Istanbul and later releases have this value set to 20 unless a greater value is specified.|
    |Active|A check box to indicate that this certificate is active.|
    |Format|The format of the certificate. SAML uses the PEM format.|
    |Type|The certificate container. The instance recognizes certificates from trust stores, Java keystore, and PKCS\#12 keystores.|
    |Valid from|The instance automatically adds the certificate valid from date to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |Expires|The instance automatically adds the certificate expiration date to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |Expires in days|The calculated number of days to expiration.|
    |Short description|A description for the certificate.|
    |Issue|The instance automatically adds the certificate issuer to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |Subject|The instance automatically adds the certificate subject to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |PEM Certificate|Enter the value of the X509 certificate.|


## What to do next

Click **Validate Stores/Certificates** to test the trust store and certificate.

