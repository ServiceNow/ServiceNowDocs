---
title: Generating a server certificate
description: You can use keytool to generate a new Java keystore file, create a certificate signing request \(CSR\), and import the private key, public certificate pair, and signed certificates into the keystore.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generating an LDAP client certificate, Certificates, Encryption]
---

# Generating a server certificate

You can use keytool to generate a new Java keystore file, create a certificate signing request \(CSR\), and import the private key, public certificate pair, and signed certificates into the keystore.

## Before you begin

Role required: admin

## About this task

See the [Java keytool documentation](http://docs.oracle.com/javase/7/docs/technotes/tools/windows/keytool.html) for more information on generating keys and CSRs.

Enter these commands in a command line interface:

## Procedure

1.  Generate a Java keystore and key pair.

    For example, this command creates a keystore called my.keystore and generates a private key called mydomain within the keystore.

    ```
    keytool -genkey -alias mydomain -keyalg RSA -keystore my.keystore
    ```

2.  Generate a CSR for an existing Java keystore.

    For example, this command generates a CSR called mydomain.csr or the mydomain key.

    ```
    keytool -certreq -alias mydomain -keystore my.keystore -file mydomain.csr
    ```

3.  Import a root or intermediate certificate authority, or CA, certificate to the Java keystore.

    For example, this command imports the CA certificate for Thawte. This command assumes that Thwate was the CA that signed the CSR.

    ```
    keytool -import -trustcacerts -alias root -file Thawte.crt -keystore my.keystore
    ```

4.  Import a signed primary certificate to the Java keystore.

    For example, this command imports the signed certificate mydomain.crt into the keystore.

    ```
    keytool -import -trustcacerts -alias mydomain -file mydomain.crt -keystore my.keystore
    ```

5.  Upload the certificate in the keystore file \(my.keystore\) to the instance.


## What to do next

[Uploading a certificate to an instance](t_UploadACertificateToAnInstance.md)

**Parent Topic:**[Generating an LDAP client certificate](t_GenerateAnLDAPClientCertificate.md)

