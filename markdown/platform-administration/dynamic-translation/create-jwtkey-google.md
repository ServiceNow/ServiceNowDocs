---
title: Create a JWT signing key for Google Cloud Translator Service spoke
description: Assign a JSON Web Token \(JWT\) signing key to your Java KeyStore certificate.
locale: en-US
release: yokohama
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up the Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a JWT signing key for Google Cloud Translator Service spoke

Assign a JSON Web Token \(JWT\) signing key to your Java KeyStore certificate.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Identifier of the JWT signing key.|
    |Signing Keystore|Valid JKS certificate for which you want to assign the key.|
    |Key Id|Key ID to identify which key is used when multiple keys are used to sign tokens.|
    |Signing Algorithm|Algorithm to sign with the key.|
    |Signing Key Password|Password associated with the key. Use the export password or the source keystore password specified when creating the JKS certificate. For more information on this password, see [Create a Java KeyStore certificate](create-jks-google.md).|
    |Active|Option to activate the key.|

4.  Click **Submit**.


**Parent Topic:**[Set up the Google Cloud Translator Service spoke](setup-google-translator.md)

**Previous topic:**[Attach a Java KeyStore certificate to Google Cloud Translator Service spoke](attach-jks-google-translator.md)

**Next topic:**[Create a JWT provider for Google Cloud Translator Service spoke](create-jwtprovider-google.md)

