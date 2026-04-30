---
title: Configuring mutual authentication
description: Mutual authentication establishes trust by exchanging secure sockets layer \(SSL\) certificates.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Web service security, Authentication, Access Management]
---

# Configuring mutual authentication

Mutual authentication establishes trust by exchanging secure sockets layer \(SSL\) certificates.

During the SSL handshake, the server presents its certificate to the client. Subsequently, depending on the server's configuration, it may request a certificate from the client. Both server and client perform certificate validation procedures to ensure the authenticity and integrity of the presented certificates.

Following a successful validation, acknowledgments are exchanged before the initiating the HTTPS connection.

**Note:** For information about using a custom HTTPS protocol profile to enable mutual authentication, see [Create a protocol profile](https://www.servicenow.com/docs/access?context=t_CreateAProtocolProfile&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

Administrators do the preliminary work of setting up the client Key Store and generating certificates before certification requests are fulfilled.

**Warning:** This feature only enables mutual authentication on outbound https connections.

## Creating the Key Store

The instance currently supports uploading a Java Key Store file, which contain a private key and a public certificate pair, the public certificate includes complete chain including the root certificate.

To set up your client Key Store:

-   You require a certificate signed by a trusted certificate authority \(CA\).
-   Your API endpoint provider may assist you in generating the Key Store.

If you need to generate the Key Store, the process involves several steps using command-line interface commands to generate a new Key Store file, create a certificate signing request \(CSR\), and import signed certificates. Before importing your domain's primary certificate, any root or intermediate certificates should be imported first. Here's a step-by-step instruction:

1.  Generate a Java keystore and key pair.

    ```
    keytool -genkey -alias mydomain -keyalg RSA -keystore my.keystore
    ```

2.  Generate a CSR for an existing Java keystore.

    ```
    keytool -certreq -alias mydomain -keystore my.keystore -file mydomain.csr
    ```

3.  Send the CSR to your CA signing authority to sign and return the certificate files, which includes intermediate and root certificates along with signed certificate.
4.  Import a root or intermediate certificate authority CA certificate to an existing Java keystore.

    ```
    keytool -import -trustcacerts -alias root -file Thawte.crt -keystore my.keystore
    ```

    **Note:** You can bundle all the certificates in one file and import. This is preferable option. If you do this way you can skip 5

    ```
    keytool -import -alias mydomain -file merged.crt -keystore my.keystore
    ```

5.  Import a signed primary certificate to an existing Java keystore.

    ```
    keytool -import -trustcacerts -alias mydomain -file mydomain.crt -keystore my.keystore
    ```


## Setting up the Key Store

Now that the key store has been created, it can be uploaded to the Certificates table. On the **System Definition** &gt; **Certificates** page, click **New** and set the following fields:

-   Enter a certificate **Name**.
-   Store the key store as **Active**.
-   Set **Type = Java Key Store**.
-   Provide a **Key store password**. This is the password that was used to create the keystore.

Click **Submit** to create the Java Key Store entry.

![](../image/Keystore.png "Key Store")

## Specifying a Trusted Server Certificate

During an outbound SSL connection, which is an HTTPS Web Service call, it is possible to specify a certificate provided by the service provider that ensures the validity of the service provider during the SSL connection. For example, a browser attempting to connect to a secure service which identifies itself by a certificate.

By uploading the trusted server certificate, ServiceNow ensures that the service it is connecting to is valid and secure.

Create a new Certificate entry with the type of "Trust Store Cert" and attach a DER formatted certificate, or copy and paste its PEM format into the **PEM Certificate** field.

## Protocol Profile

![](../image/CertExchange.png "Certificate Exchange")

-   When a client requests the server certificate for authentication, a certificate signing request \(CSR\) is generated.
-   To respond to a CSR, the server generates two unique cryptographic keys: A public key, which is used to encrypt messages to the server and a private key, which is used to decrypt messages. Both keys are kept in the Key Store.
-   Keys are used to decrypt the client secure messages so they can be read by the server. Any outgoing connection that is going to be HTTPS verifies the certification by checking the Key Store, offering its public certification, and uses the trust store certificates to verify mutual trust back.
-   To complete the secure link between the client and the server, the server matches the certificate to the corresponding private key. Because only the server has access to the private key, the server can decrypt the data from the client.

**Note:** For information about using a custom HTTPS protocol profile to enable mutual authentication, see [Create a protocol profile](https://www.servicenow.com/docs/access?context=t_CreateAProtocolProfile&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

The server responds by sending a certificate. Is this a certificate that the client accepts? If yes, a message is sent to the server accepting the certificate and a secure channel is initiated. If the certificate is not accepted, it may mean that the root authority is needed for certification.

