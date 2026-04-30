---
title: Create a JWT provider for Google Cloud Translator Service spoke
description: Add a JSON Web Token \(JWT\) provider to Google Cloud Translator Service spoke.
locale: en-US
release: yokohama
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up the Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a JWT provider for Google Cloud Translator Service spoke

Add a JSON Web Token \(JWT\) provider to Google Cloud Translator Service spoke.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Identifier of the JWT provider.|
    |Expiry Interval \(sec\)|Number of seconds that indicate the lifespan of the JWT provider token. Specify `3600`.|
    |Signing Configuration|JWT signing key.|

4.  Right-click the form header, and click **Save**.

5.  In the Standard Claims related list, enter the values for these claims.

    |Claim name|Claim value|
    |----------|-----------|
    |aud|https://www.googleapis.com/oauth2/v4/token|
    |iss|**client\_email** value from the JSON file.|

6.  In the Custom Claims related list, create the **scope** claim and enter its value as `https://www.googleapis.com/auth/cloud-translation`.

7.  Click **Update**.


**Parent Topic:**[Set up the Google Cloud Translator Service spoke](setup-google-translator.md)

**Previous topic:**[Create a JWT signing key for Google Cloud Translator Service spoke](create-jwtkey-google.md)

**Next topic:**[Configure the credential for the GoogleTranslation alias](configure-credential-google.md)

