---
title: Generating an LDAP client certificate
description: Generate an LDAP client certificate for mutual authentication using OpenSSL. The final output is a PKCS\#12 certificate stored within a Java keystore.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Certificates, Encryption]
---

# Generating an LDAP client certificate

Generate an LDAP client certificate for mutual authentication using OpenSSL. The final output is a PKCS\#12 certificate stored within a Java keystore.

## Before you begin

Role required: admin

## About this task

See the [OpenSSL documentation](http://www.openssl.org/docs/) for more information about generating certificates. These steps assume you have access to OpenSSL.

Enter these commands in a command line interface.

## Procedure

1.  Generate a self-signed client certificate.

    For example, this command creates a client certificate test1-cert.crt based on the test1-key.key private key.

    ```
    openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout test1-key.key -out test1-cert.crt
    ```

2.  Convert both the certificate file and private key to PKCS\#12 \(a file with a .pfx or .p12 extension\).

    For example, this command converts the client certificate and private key to a PKCS\#12 certificate called test1-certificate.pfx.

    ```
    openssl pkcs12 -export -out test1-certificate.pfx -inkey test1-key.key -in test1-cert.crt
    ```

3.  Generate the Java Key Store and import the pkcs12 file into it.

    For example, this command imports the certificate to the test1.jks Java keystore.

    ```
    keytool -importkeystore -srckeystore test1-certificate.pfx -srcstoretype PKCS12 -destkeystore test1.jks
    ```

4.  [Upload the certificate](t_UploadACertificateToAnInstance.md) in the keystore file \(`test1.jks`\) to the instance.

    **Note:**

    If you are uploading to an on-premise instance using a certificate with the .jks extension and you receive an error saying "No valid certificate found to process the application upload", use a certificate with the .pfx extension instead.


## What to do next

[Uploading a certificate to an instance](t_UploadACertificateToAnInstance.md)

-   **[Generating a server certificate](t_GenerateAServerCertificate.md)**  
You can use keytool to generate a new Java keystore file, create a certificate signing request \(CSR\), and import the private key, public certificate pair, and signed certificates into the keystore.

**Parent Topic:**[Certificates](../concept/c_Certificates.md)

**Related topics**  


[Exploring Certificates](../concept/exploring-certificates.md)

[Uploading a certificate to an instance](t_UploadACertificateToAnInstance.md)

