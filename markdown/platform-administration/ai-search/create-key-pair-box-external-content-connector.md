---
title: Create a public/private key pair for the Box external content connector
description: Generate an encrypted private key and a public key for use by the Box external content connector.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Box external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a public/private key pair for the Box external content connector

Generate an encrypted private key and a public key for use by the Box external content connector.

## Before you begin

You need access to the OpenSSL Library toolkit, version 3. If you don't have this toolkit available, you can install it as follows:

-   **Linux**

    Install the latest available **openssl** package using your distribution's package manager. As an example, on Ubuntu or Debian, run `sudo apt install openssl`. On Red Hat Enterprise Linux, run `sudo dnf install openssl`.

-   **macOS**

    macOS ships with a LibreSSL executable binary installed as `/usr/bin/openssl`, but one of the OpenSSL commands for this task requires options that LibreSSL doesn't support. Use Homebrew \([https://brew.sh/](https://brew.sh/)\) to install the **openssl@3** formula. For details on this formula, see [https://formulae.brew.sh/formula/openssl@3](https://formulae.brew.sh/formula/openssl@3).

-   **Windows**

    Install OpenSSL binaries from [https://github.com/openssl/openssl/wiki/Binaries](https://github.com/openssl/openssl/wiki/Binaries).


For more information about the OpenSSL Library, see [https://openssl-library.org/](https://openssl-library.org/).

Role required: none

## About this task

You need to create your own private and public RSA keys for use with the Box external content connector. The keys that the Box developer console generates are not secure enough to comply with the connector's security requirements.

To configure public/private key authentication for the connector, you need to create the following items:

1.  A 4,096-bit RSA private key in encrypted PKCS\#8 format.
    -   Your connector admin needs this encrypted private key file and its password when configuring settings for the Box external content connector.
    -   When the Box external content connector runs a crawl, it presents the public key certificate from this encrypted private key file to authenticate itself as a valid client of the OAuth 2.0 app in the Box developer console.
2.  A public key in PEM-encoded \(Base64 ASCII\) X.509 certificate format.
    -   Your Box administrator needs to upload this certificate file in the Box OAuth 2.0 app that grants API access to the Box external content connector.
    -   When the Box external content connector presents its public-key certificate for client authentication, Box uses this uploaded certificate to confirm that the connector is a valid client of the OAuth 2.0 app.

## Procedure

1.  Generate a 4,096-bit RSA private key in PEM-encoded X.509 certificate format by running this OpenSSL command:

    ```
    openssl genpkey -algorithm RSA -out private_key.pem -pkeyopt rsa_keygen_bits:4096
    ```

2.  Generate a secure password to use for the encrypted version of your new private key:

    1.  Run this OpenSSL command:

        ```
        openssl rand -base64 20
        ```

        **Note:** This command generates a 20-character password. If your organization's standards require longer passwords, replace `20` with the desired password length in characters. The password must have at least 112 bits of entropy.

    2.  Copy the generated password and record it in a secure location.

        **Important:** Your connector admin needs this password when configuring the Box external content connector.

3.  Convert your new private key to the encrypted PKCS\#8 format \(with AES-256-CBC and PBKDF2\):

    1.  Run this OpenSSL command:

        ```
        openssl pkcs8 -topk8 -in private_key.pem -out encrypted_key.pem -v2 aes-256-cbc -v2prf hmacWithSHA256 -iter 10000 -saltlen 32
        ```

    2.  When prompted, enter the secure password you generated in step [2](create-key-pair-box-external-content-connector.md#generate-secure-password-step).

    3.  Store the generated `encrypted_key.pem` file in a secure location.

        **Important:** Your connector admin needs this encrypted key file when configuring the Box external content connector.

4.  Extract the public key for your new private key in PEM-encoded X.509 certificate format:

    1.  Run this OpenSSL command:

        ```
        openssl pkey -in private_key.pem -pubout -out public_key.pem
        ```

    2.  View or edit the content of the `public_key.pem` file that you generated in step [2](create-key-pair-box-external-content-connector.md#generate-secure-password-step).

    3.  Copy the PEM-encoded X.509 public key certificate text and store it in a secure location.

        The public key consists of all the text in the file, including the `-----BEGIN PUBLIC KEY-----` and `-----END PUBLIC KEY-----` markers.

        ![PEM-encoded public key certificate text from public_key.pem file.](../image/public-key-pem-encoding.png)

        **Important:** Your Box admin needs this PEM-encoded X.509 public key certificate text when configuring the OAuth 2.0 application for Box external content connector in the Box developer console.


## What to do next

Provide the following items to your Box admin and your connector admin:

<table id="table_i22_yvt_rfc"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PEM-encoded X.509 public key certificate text

</td><td>

Provide this text to your Box administrator. They will need to upload the PEM-encoded X.509 public key certificate text to the Box developer console when configuring an OAuth 2.0 application for the Box external content connector. For more information on configuring an OAuth 2.0 application in the Box developer console for the Box external content connector, see [Configure Box for external content indexing](configure-box-external-content-indexing.md).

</td></tr><tr><td>

Encrypted private key file and password

</td><td>

Provide this encrypted private key file and its password to your connector admin. They will need the file and password when configuring the Box external content connector. For details on creating and configuring the Box external content connector, see [Create a Box external content connector](create-ext-cont-connector-box.md).

</td></tr></tbody>
</table>**Parent Topic:**[Box external content connector](../concept/box-external-content-connector.md)

