---
title: Replace an untrusted or expired third-party SSL certificate
description: When an SSL connection is required in an integration, there are circumstances when the certificate provided by the third-party vendor is either not yet trusted in ServiceNow or has expired. You can replace it or add a new certificate.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integration troubleshooting, ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Replace an untrusted or expired third-party SSL certificate

When an SSL connection is required in an integration, there are circumstances when the certificate provided by the third-party vendor is either not yet trusted in ServiceNow or has expired. You can replace it or add a new certificate.

## Before you begin

Role required: sn\_ti.write

## Procedure

1.  Acquire the SSL certificate from the third-party vendor.

    For example, you can import an X.509 Certificate \(PEM\) from an SSL endpoint in the Firefox browser, as follows.

    1.  Enter the endpoint URL into the browser address bar.

        For example: `https://<3rdparty>/`.

    2.  Click the lock icon in the address line.

    3.  Click **More Information** and click the **Security** tab.

    4.  Click **View Certificate** and click the **Detail** tab.

    5.  Click **Export** to save the PEM into your local file system.

    6.  Open the saved file in any text editor tool and copy the content into the clipboard.

        It must begin with `-----BEGIN CERTIFICATE-----` and end with `-----END CERTIFICATE-----`.

2.  Navigate to **System Definition** &gt; **Certificates**.

3.  Click **New** and [create a new record](https://www.servicenow.com/docs/access?context=t_UploadACertificateToAnInstance&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) for the integration.

4.  In **PEM Certificate**, paste in the certificate you downloaded and copied into the clipboard earlier.

5.  Click **Save**.

    The other fields in the record are generated automatically.


**Parent Topic:**[Integration troubleshooting](../concept/c_IntegrationTroubleshooting.md)

