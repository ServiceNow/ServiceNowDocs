---
title: Set up the Google Cloud Translator Service spoke
description: Integrate your Google account with your ServiceNow instance.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up the Google Cloud Translator Service spoke

Integrate your Google account with your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Google Cloud Translator Service spoke.
-   Create a service account on Google Cloud, generate a service account key of JSON type and download it. For information on creating the service account key, see the [Google](https://cloud.google.com/docs/authentication/getting-started#creating_a_service_account) documentation.
-   Enable the Cloud Translation API service. For information on enabling a service, see the [Google](https://cloud.google.com/service-usage/docs/enable-disable#enabling) documentation.
-   Role required: admin

1.  [Create a Java KeyStore certificate](create-jks-google.md)  
Encrypt the security certificates obtained from Google by creating a Java KeyStore \(JKS\) file.
2.  [Attach a Java KeyStore certificate to Google Cloud Translator Service spoke](attach-jks-google-translator.md)  
Enable the JWT client authentication by attaching a valid Java KeyStore \(JKS\) certificate to Google Cloud Translator Service spoke.
3.  [Create a JWT signing key for Google Cloud Translator Service spoke](create-jwtkey-google.md)  
Assign a JSON Web Token \(JWT\) signing key to your Java KeyStore certificate.
4.  [Create a JWT provider for Google Cloud Translator Service spoke](create-jwtprovider-google.md)  
Add a JSON Web Token \(JWT\) provider to Google Cloud Translator Service spoke.
5.  [Configure the credential for the GoogleTranslation alias](configure-credential-google.md)  
Authorize actions of Google Cloud Translator Service spoke by configuring the Google OAuth 2.0 credential.
6.  [Configure the connection attributes for the GoogleTranslation alias](configure-connection-google.md)  
Connect to the Google's translation service by configuring the Google connection. Provide information that is used by HTTP\(s\) actions or activities to connect to that service.

**Parent Topic:**[Google Cloud Translator Service Spoke](../concept/google-translator-spoke.md)

