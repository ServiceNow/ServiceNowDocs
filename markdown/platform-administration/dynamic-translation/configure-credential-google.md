---
title: Configure the credential for the GoogleTranslation alias
description: Authorize actions of Google Cloud Translator Service spoke by configuring the Google OAuth 2.0 credential.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the credential for the GoogleTranslation alias

Authorize actions of Google Cloud Translator Service spoke by configuring the Google OAuth 2.0 credential.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select the Google OAuth 2.0 credential.

3.  Open the record specified in the **OAuth Entity Profile** field.

4.  In the **JWT Provider** field, specify the JWT provider that you want to use.

5.  Click **Update**.

6.  To verify if an OAuth Access token is generated to connect to Google's translation services, click the **Get OAuth Token** related link of the Google OAuth 2.0 credential.


**Parent Topic:**[Set up Google Cloud Translator Service spoke](setup-google-translator.md)

**Previous topic:**[Create a JWT provider for Google Cloud Translator Service spoke](create-jwtprovider-google.md)

**Next topic:**[Configure the connection attributes for the GoogleTranslation alias](configure-connection-google.md)

