---
title: Sign and verify an ACC plugin
description: Create a self-signed certificate for an Agent Client Collector \(ACC\) plugin and verify the signature to enable validation of the signed plugin on endpoint devices.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-09"
reading_time_minutes: 1
breadcrumb: [Creating and executing a PowerShell script-based remedial action, DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Sign and verify an ACC plugin

Create a self-signed certificate for an Agent Client Collector \(ACC\) plugin and verify the signature to enable validation of the signed plugin on endpoint devices.

## Before you begin

-   Create the ACC plugin `tar.gz` file on your local computer.
-   Make sure that OpenSSL is installed on your local computer.

Role required: admin

## Procedure

1.  Generate a 2048-bit RSA key and a corresponding self-signed certificate with one year validity by using the following command:

    ```
    openssl req -nodes -x509 -sha256 -newkey rsa:2048 -keyout "sign.key" -out "sign.crt" -days 365 -subj "/C=IN/ST=TG/L=HYD/O=servicenow/OU=acme/CN=sign"
    ```

    This command creates a private key \(`sign.key`\) and a public certificate \(`sign.crt`\).

2.  Sign the plugin file with your private key.

    ```
    openssl dgst -sha256 -sign "sign.key" -out sign.txt.sha256 *plugin name*.tar.gz
    ```

3.  Extract the public key from the certificate for signature verification.

    ```
    openssl x509 -in "sign.crt" -pubkey -noout > pubkey.pem
    ```

4.  Verify the signature using the public key to confirm the file was signed correctly.

    ```
    openssl dgst -sha256 -verify pubkey.pem -signature sign.txt.sha256 *plugin name*.tar.g
    ```

5.  Encode the signature file using Base64 to enable the ACC agent to validate the plugin.

    -   macOS

        ```
        base64 -i sign.txt.sha256 -o sign.txt.sha256_encode64.sig
        ```

    -   Windows

        ```
        openssl enc -base64 -in sign.txt.sha256 -out sign.txt.sha256_encode64.sig
        ```

6.  Create a directory to store the signed plugin.

    ```
    mkdir signed-plugin
    ```

7.  Move the plugin archive and signature file to the new directory.

    ```
    mv *plugin name*.tar.gz signed-plugin/
    
    mv sign.txt.sha256_encode64.sig signed-plugin/
    ```

8.  Navigate to the new directory.

    ```
    cd signed-plugin
    ```

9.  Create a `tar.gz` file containing both the plugin archive and the signature file.

    ```
    tar -C . -zcvf ../sign-test.tar.gz *
    ```

10. Copy and place the self-signed certificate \(`sign.crt`\) in the certificate directory \(`[agent_root]/cert`\) of the ACC agent using one of the following options:

    -   Copy the file manually.
    -   Distribute the certificate to agent devices using a device management utility such as Jamf or Microsoft Intune.
11. Add the certificate to the agent trust store.

    For more information, see [Add a self-signed certificate to your operating system's truststore](https://www.servicenow.com/docs/access?context=add-certificate-trust-store&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

12. Upload the signed ACC plugin to the ServiceNow instance.

    For more information, see [Create and edit Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=create-edit-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).


