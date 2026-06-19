---
title: Attach a Java KeyStore certificate to Google Cloud Translator Service spoke
description: Enable the JWT client authentication by attaching a valid Java KeyStore \(JKS\) certificate to Google Cloud Translator Service spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/dynamic-translation/attach-jks-google-translator.html
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Attach a Java KeyStore certificate to Google Cloud Translator Service spoke

Enable the JWT client authentication by attaching a valid Java KeyStore \(JKS\) certificate to Google Cloud Translator Service spoke.

## Before you begin

-   Role required: admin
-   Valid Java KeyStore certificate

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Identifier of the certificate.|
    |Notify on expiration|Users to be notified when the certificate expires.|
    |Warn in days to expire|Number of days to send a notification before the certificate expires.|
    |Active|Option to activate the certificate.|
    |Type|Type of the certificate. Select **Java Key Store**.|
    |Expires in days|Number of days until the certificate expires.|
    |Key store password|Password to access the certificate. Use the destination keystore password specified when creating the JKS certificate. For more information on this password, see [Create a Java KeyStore certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/create-jks-google.md).|
    |Short description|Summary about the certificate.|

4.  Click the manage attachments icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachments icon\) and attach a JKS certificate.

5.  To validate the JKS certificate, click **Validate Stores/Certificates**.

6.  Click **Submit**.


**Parent Topic:**[Set up the Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/setup-google-translator.md)

**Previous topic:**[Create a Java KeyStore certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/create-jks-google.md)

**Next topic:**[Create a JWT signing key for Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/create-jwtkey-google.md)

