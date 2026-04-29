---
title: Create a Java KeyStore certificate
description: Encrypt the security certificates obtained from Google by creating a Java KeyStore \(JKS\) file.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the Google Cloud Translator Service spoke, Google Cloud Translator Service Spoke, Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
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
      "private_key": "-----BEGIN PRIVATE KEY-----\nMIIEvQKBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQDg97zOxfOenyu2\niXC8ArQHaAgOiy27sjG3jJXohUdHkawuX+nQLWZkIbZYlZX+cMjNfpUFpzeHRkPm\n5OQ2bjHCgCTVFCbToKIH+VkMpS7LO+TFKW2TkWJHzWO2Xv30bT+2HkSb4tTZisMg\nV/sI6dGJaOko4yTIBwZc7vlr28nGJdw945+9NVkEPm/G8drYJRTlrImyfnnD0RGR\npyKctHAC3wZ/rCE5b/VIHK5ZKspRT/qXVwZsH5pW7a8NDrB1z+YQIGGOjlfINxBE\nQCE5GhiUF+XscfGdq30culFoILO9xAk/41yQb8ziDr4Ru5H1UF0ljp4t6fLw3k2o\noDsr+R+XAgMBAAECggEAA03QIY9JsSowR6mEE+YsQ7GU8LW9kbSfw0zWxMf0UIpE\np5e0BOEt0EmodmuX/NkmMdJqmN8oUx3GkIULDvuWUn90SwbVPSVuS8SvOJ7SbZyv\nEvA1UkX/1gMftEV34FecaG3QXyO5MYq2q+pu3uYkNCrsxbN0TlXAE6xU0G81auoL\nYIl7pzVfcxDW5Of5VI5AuMc8+0rgadvOPu3JThjjauMvnDPKi5sbKDsDCfTqqDys\nHMny8+uhfCOr2JtTgpc4HUgqGKpALAUQvRZYmmlKqfBNgXo+dDBKJsd7pD9NnxQn\nM7l8wqQ0kS2kfcJsHNcV4ZUORabz1q1MFlVdxxeijQKBgQD5r7J/MgN4LLekaimE\n3T27KTA12aikQl0LORQHLbHZRexVD41WoRrQySSzUvQKXSiwZwRQLO/hptDRnUyh\n6WVQLwtSiNvItLu+8Ak2mb3F+NDEFb/R1FPdTR30G7wXEeau1+cm8+8N63ehFAW4\n7IXTyDhtO5c3deXN7SDrRFjrnQKBgQDmqAdRkKPwau6q+zSGPxqcFqlXS+ghpQkT\nUPxe45aZdRuFUOUCWA9BIbMnlVHZUDnQpiIbfBJ9Tcs2/vBwLt2QjziZPbnIlmkp\nqIF4t5edar8Z6vn0lWmeupAmlFqKN7GoopUD+RIto68BfSKIPczfGLtu3PxLEmgj\nRYzY5HUTwwKBgCZ05zssCtjBmm9aYpayNMXU7DX/FjhmeEo4Olt4sEHUwTfAs3Y6\nThUGRf7QsgG+o3u4AjQPF8tblCIU5i6x8gbNmCLYLXHWVGxuMB0WxOHvFsh8yRSa\nbWhSbmCgvPGYsj0Px+x5+cHdGInYuaDn3RznY7l/SiUipYh4E2/pEQEJAoGAdu1G\nMMESNkD8ZD5324wn7TkmATPLMaXFYydLqKVSHjeqg/eszKOY4e09UXiFJjZeSP2P\n8nnrkp4M3INgd4dCiGnANgsEgq9C887FSvfmfazvca6dSIXNWqE4+Btf/4ot2RRT\nHyRKQiv2bR8XMgYjXxiCc+wPTank9eLDd4V79D8CgYEA6Eywngil5bVO5ksW9gyp\n0u5eieKMNYndPq5lyw1POyN9nx/iYQ3m2FI7d2K7aBpK0AXkLZQqv5tbqrF2fvdO\nbm4eLISLg8kdZ09OohAsRuZ6JG2aICw4vTWgQyRWLe4RxdoY9gGKh8N844tUU7uN\nPCsWu/rdB8dT8wqerTFo81U=\n-----END PRIVATE KEY-----\n",
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


**Parent Topic:**[Set up the Google Cloud Translator Service spoke](setup-google-translator.md)

**Previous topic:**[Set up the Google Cloud Translator Service spoke](setup-google-translator.md)

**Next topic:**[Attach a Java KeyStore certificate to Google Cloud Translator Service spoke](attach-jks-google-translator.md)

