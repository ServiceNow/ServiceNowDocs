---
title: Install the LDAP X.509 SSL certificate
description: You can install an X.509 certificate for your LDAP integration.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Install the LDAP X.509 SSL certificate

You can install an X.509 certificate for your LDAP integration.

## Before you begin

Role required: admin

## Procedure

1.  Purchase or generate an SSL certificate on your LDAP server.

2.  Navigate to **LDAP** &gt; **Certificate** and click **New**.

3.  Fill in the form fields:

    |Field|Description|
    |-----|-----------|
    |Name|The certificate name.|
    |Expiration notification|Select this option to send a notification to the users selected in the **Notify on expiration** field. By default, this is enabled.|
    |Notify on expiration|Select the users to revive the notification regarding certificate expiration. If no users are selected, the logged in user is added by default, along with the last two logged in users with the administrator role.|
    |Warn in days to expire|The number of days before expiration that the instance send the notification. Enter a value of at least 20. Instances upgraded to Istanbul and later releases have this value set to 20 unless a greater value is specified.|
    |Active|A check box to indicate that this certificate is active.|
    |Format|The format of the certificate.|
    |Type|The certificate container. The instance recognizes certificates from trust stores, Java keystore, and PKCS\#12 keystores.|
    |Valid from|The instance automatically adds the certificate valid from date to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |Expires|The instance automatically adds the certificate expiration date to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |Expires in days|The calculated number of days to expiration.|
    |Short description|A description for the certificate.|
    |Issuer|The instance automatically adds the certificate issuer to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |Subject|The instance automatically adds the certificate subject to this field. Attach the certificate to the X.509 certificate record to populate this field.|
    |PEM Certificate|Enter the value of the X509 certificate.|

    **Note:** The integration does not currently sign the certificate in communications between the instance and the IdP.

4.  Click **Save**.


## What to do next

Click **Validate Stores/Certificates** to test the trust store and certificate.

