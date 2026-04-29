---
title: Enable OpenSSL secure signing for plugins
description: Create a self-signed certificate for an Agent Client Collector plugin. The following procedure gives an example of how to create an x509 certificate using OpenSSL. For other certificate types, consult OpenSSL documentation.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC certificates, ACC deployment - shared between servers and endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Enable OpenSSL secure signing for plugins

Create a self-signed certificate for an Agent Client Collector plugin. The following procedure gives an example of how to create an x509 certificate using OpenSSL. For other certificate types, consult OpenSSL documentation.

## Before you begin

-   Ensure that the **verify-plugin-signature** property is set to **True** in the agent's `acc.yml` file to verify plugin signing.
-   Ensure **OpenSSL** is installed on your system.

Role required: agent\_client\_collector\_admin

## About this task

Enabling an OpenSSL secure signing mechanism for plugins works with an Agent Client Collector installed on a Linux system.

## Procedure

1.  Create a plugin file with a `tar.gz` extension.

    For more information, see [Create and edit Agent Client Collector plugins](create-edit-assets.md).

2.  Generate your own secure self-certificate for the plugin file.

    1.  Create an x509 certificate.

        ```
        openssl req -nodes -x509 -sha256 -newkey rsa:2048 -keyout "sign.key" -out "sign.crt" -days 365 -subj
                "/C=<CountryName>/ST=<StateOrProvinceName>/L=<Locality>/O=<Organization>/OU=<OrganizationalUnit>/CN=sign"
        ```

    2.  Sign the plugin file.

        ```
        openssl dgst -sha256 -sign "sign.key" -out sign.txt.sha256 <plugin-name>.tar.gz
        ```

        Alternatively, you can sign plugins using a certificate authority. When doing so, assign the certificate .pem format and place it in the agent's `cert` directory.

    3.  Verify that the signature is configured correctly.

        ```
        openssl dgst -sha256 -verify  <(openssl x509 -in "sign.crt" -pubkey -noout) -signature sign.txt.sha256 <plugin-name>.tar.gz
        ```

        If the file is valid, the output is `Verified OK`.

    4.  Encode the signature's certificate with base64 coding.

        ```
        base64 sign.txt.sha256 > sign.txt.sha256_encode64.sig
        ```

        A `sign.txt.sha256_encode64.sig` file is created.

3.  Run the following commands to create a new directory and insert the `tar.gz` and `sign.txt.sha256_encode64.sig` files.

    1.  `mkdir signed-plugin`

    2.  `mv <plugin-name>.tar.gz signed-plugin`

    3.  `mv sign.txt.sha256_encode64.sig signed-plugin`

    4.  `cd signed-plugin`

4.  Create another `tar.gz` file by running the same commands as you ran for the first `tar.gz` file.

    1.  `tar -C . -zcvf ../<plugin-name>.tar.gz *`

    2.  `cd..`

        **Note:** Save the new file as `../<plugin-name>.tar.gz` to avoid naming collisions with the original `<plugin-name>.tar.gz` file that exists in the current directory.

5.  Upload the new `tar.gz` plugin file to the instance.

6.  Set the plugin file as **active=true**.

7.  Place the `sign.crt` file in the agent's `cert` directory, which is located in the `config` folder.

8.  In the `acc.yml` file, set `verify-plugin-signature` to **true**.


**Parent Topic:**[Agent Client Collector certificates](../concept/acc-certificates.md)

