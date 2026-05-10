---
title: Update your X.509 certificate
description: If you require an SSL connection for the integration, there are circumstances when the certificate provided by the third-party vendor is either not yet trusted in ServiceNow or has expired. This task is optional.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [WhoisXML API integration setup, WhoisXML API integration, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Update your X.509 certificate

If you require an SSL connection for the integration, there are circumstances when the certificate provided by the third-party vendor is either not yet trusted in ServiceNow or has expired. This task is optional.

## Before you begin

Role required: admin

## Procedure

1.  Acquire the SSL certificate from the third-party vendor.

    For example, you can import an X.509 Certificate \(PEM\) from an SSL endpoint in the Firefox browser, as follows.

    1.  Enter the endpoint URL into the browser address bar.

        For example: `https://<3rdparty>/`.

    2.  Click the lock icon in the address line.

    3.  Click **More Information** and click the **Security** tab.

    4.  Click **View Certificate** and click the **Detail** tab.

    5.  Click **Export** to save the PEM into your local file system.

    6.  Open the saved file in any text editor tool and copy the content to the clipboard.

        It must begin with `-----BEGIN CERTIFICATE-----` and end with `-----END CERTIFICATE-----`.

2.  Navigate to **System Definition** &gt; **Certificates**.

3.  Click **New** and [create a new record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_UploadACertificateToAnInstance.md) for the integration.

4.  In **PEM Certificate**, paste in the certificate you downloaded and copied into the clipboard earlier.

5.  Add the certificate to the Identity Provider record.

    1.  Navigate to **Multi-Provider SSO** &gt; **Identity Providers**.

    2.  Select the active default identity provider for which you created the new certificate.

    3.  Scroll down to **X.509 certificates** related list, and click **Edit**.

    4.  Move the newly created certificate to the **Selected** column.

6.  Click **Save**.

    The other fields in the record are generated automatically.

    **Note:** If you have a certificate that has expired, you need to remove it. For information on how to remove the expired certificate, refer to [KB0691439 Replacing an expiring SAML certificate](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0691439).


