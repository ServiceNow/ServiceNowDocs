---
title: Create a service provider key store for SAML
description: Create a Java key store containing the following items for your instance to sign logout requests.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [\(Optional\) Set keystore properties for signing logout requests for SAML, Service Provider \(SP\) system properties, SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Create a service provider key store for SAML

Create a Java key store containing the following items for your instance to sign logout requests.

## Before you begin

Role Required: admin

## About this task

-   Signed server certificate for the instance
-   Signed CA certificate
-   Public and private key pair

You may create your own signed certificate with a private certificate authority or purchase one from a public certificate authority.

The following steps illustrate how to generate a new Java Keytool keystore file, create a certificate signing request \(CSR\), and import certificates. Any root or intermediate certificates need to be imported before importing the primary certificate for your domain. Type these commands in a command line interface.

**Note:** These instructions are not specific to the platform and require technical knowledge of security certificates to complete. Technical Support cannot assist in creating the certificates.

## Procedure

1.  Generate a Java keystore and key pair.

    ```
    keytool -genkey -alias mydomain -keyalg RSA -keystore my.keystore
    ```

2.  Generate a CSR for an existing Java keystore.

    ```
    keytool -certreq -alias mydomain -keystore my.keystore -file mydomain.csr
    ```

3.  Import a root or intermediate certificate authority CA certificate to an existing Java keystore.

    ```
    keytool -import -trustcacerts -alias root -file Thawte.crt -keystore my.keystore
    ```

4.  Import a signed primary certificate to an existing Java keystore.

    ```
    keytool -import -trustcacerts -alias mydomain -file mydomain.crt -keystore my.keystore
    ```


