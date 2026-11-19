---
title: Create a Java KeyStore certificate
description: Encrypt the security certificates obtained from Google by creating a Java KeyStore \(JKS\) file.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/dynamic-translation/create-jks-google.html
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Create a Java KeyStore certificate

Encrypt the security certificates obtained from Google by creating a Java KeyStore \(JKS\) file.

## Before you begin

-   Role required: admin
-   Download a JSON file containing the service account key from Google. For information on downloading the JSON file, see the [Google](https://cloud.google.com/docs/authentication/getting-started#creating_a_service_account) documentation. Following is a sample JSON file:

    ```
    {
      "type": "service_account",
      "project_id": "primeval-nectar-242610",
      "private_key_id": "0c6c7b1511f1c236c1300c5933d528bbf45314e5",
      "private_key": "-----BEGIN PRIVATE KEY-----\n...\n-----END PRIVATE KEY-----\n",
      "client_email": "service-now-google-trans-v3@primeval-nectar-242610.iam.gserviceaccount.com",
      "client_id": "113255944370425109391",
      "auth_uri": "https://accounts.google.com/o/oauth2/auth",
      "token_uri": "https://oauth2.googleapis.com/token",
      "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
      "client_x509_cert_url": "https://www.googleapis.com/robot/v1/metadata/x509/service-now-google-trans-v3%40primeval-nectar-242610.iam.gserviceaccount.com"
    }
    
    ```


## Procedure

1.  In the JSON file, perform the following for the `private_key` value.

    1.  Unescape the `\n` characters.

        **Tip:** To unescape characters in a JSON file, you can parse a JSON string into a JavaScript object.

    2.  Store the private key in a file with .pem extension.

2.  In the JSON file, perform the following for the `client_x509_cert_url` value.

    1.  Open the link specified for `client_x509_cert_url`.

    2.  Unescape the `\n` characters for the certificate associated with the private\_key\_id mentioned in the JSON file.

    3.  Store the certificate value in a file with .pem extension.

3.  Use the openssl command to create a PKCS 12 file using the recently created private key and certificate files.

    ```
    openssl pkcs12 -export -in [path to certificate] -inkey [path to private key] -certfile [path to certificate ] -out testkeystore.p12
    ```

    For example, if certificate.pem is the certficate and privatekey.pem is the private key:

    ```
    openssl pkcs12 -export -in certificate.pem -inkey privatekey.pem -certfile certificate.pem -out testkeystore.p12
    ```

    A PKCS 12 file, testkeystore.p12, is created.

4.  Specify an export password or source keystore password.

    **Note:** You should specify this password when creating a JWT key for Google Cloud Translator Service spoke.

5.  Use the keytool command to create a JKS file from the PKCS 12 file.

    ```
    keytool -importkeystore -srckeystore testkeystore.p12 -srcstoretype pkcs12 -destkeystore wso2carbon.jks -deststoretype JKS
    ```

    **Note:** testKeyStore.p12 is the PKCS 12 file and wso2carbon.jks is the JKS file.

6.  Specify a destination keystore password.

    **Note:** You should specify this password when attaching a JKS certificate to Google Cloud Translator Service spoke.


**Parent Topic:**[Set up the Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/setup-google-translator.md)

**Previous topic:**[Set up the Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/setup-google-translator.md)

**Next topic:**[Attach a Java KeyStore certificate to Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/attach-jks-google-translator.md)

