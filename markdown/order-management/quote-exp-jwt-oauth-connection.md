---
title: Set up JWT and OAuth authentication for ServiceNow Quote Experience
description: Set up system-to-system authentication between ServiceNow and the CPQ microservice by generating a key pair, registering an OAuth application in ServiceNow, and configuring the serviceNowJwtConnection system connection in CPQ Administration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-exp-jwt-oauth-connection.html
release: brazil
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 1
breadcrumb: [Without guided setup, Set up CPQ, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Set up JWT and OAuth authentication for ServiceNow Quote Experience

Set up system-to-system authentication between ServiceNow and the CPQ microservice by generating a key pair, registering an OAuth application in ServiceNow, and configuring the `serviceNowJwtConnection` system connection in CPQ Administration.

## Before you begin

Role required: admin

## Procedure

1.  In ServiceNow, generate a public/private key pair.

    **Note:** Only PKCS8 format is supported, because it is widely compatible.

2.  Import the public key into ServiceNow.

3.  Create an OAuth Application Registry to set up the OAuth endpoint for JWT authentication.

    -   Set **AuthScope** to `useraccount`.
    -   Set the user field to the user name. If the user name is not available, use the user ID.
    For detailed instructions, see [KB1275215](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1275215).

4.  Convert the private key to PKCS8 format so that you can add it to the CPQ Administration connection.

    1.  Convert the JKS keystore to PKCS12 by using the following command:

        ```
        keytool -importkeystore \
          -srckeystore snclient.keystore -srcstorepass abcd1234 \
          -destkeystore snclient.p12 -deststoretype PKCS12 -deststorepass abcd1234
        ```

    2.  Extract the private key from the PKCS12 keystore to a PEM file by using the following command:

        ```
        openssl pkcs12 -in snclient.p12 -nodes -nocerts -passin pass:abcd1234 -out private_key.pem
        ```

    3.  Force the key to unencrypted PKCS\#8 format by using the following command:

        ```
        openssl pkcs8 -topk8 -nocrypt -in private_key.pem -out private_key_pk8.pem
        ```

    4.  Print the private key to the terminal so that you can copy it by using the following command:

        ```
        cat private_key_pk8.pem
        ```

5.  In CPQ Administration, configure the `serviceNowJwtConnection` system connection to enable JWT and OAuth authentication.

    1.  Navigate to **CPQ Administration** &gt; **Utilities** &gt; **Connections**.

    2.  Select the **serviceNowJwtConnection** system connection.

    3.  Ensure that the **Authentication Type** is set to **JWT – Client Credentials Flow**.

    4.  Enter the connection details:

        -   OAuth client ID
        -   OAuth client secret
        -   Token URL: `<instanceurl>/oauth_token.do`
        -   Private key \(the PKCS8 key from the previous step\)
        -   Key ID
        -   Host: `<ServiceNow_instance_URL>`
        -   Leave **Path** null.

