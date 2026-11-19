---
title: Sign and verify an ACC plugin
description: Sign an Agent Client Collector \(ACC\) plugin with a self-signed certificate and verify the signature so that endpoint devices can validate the plugin.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/digital-end-user-experience-dex/sign-verify-plugin.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 3
keywords: [sign acc plugin, verify plugin signature, self signed certificate, openssl, plugin validation, sign and verify plugin]
breadcrumb: [Creating a PowerShell remedial action, Creating DEX remedial actions, Configure, Digital End-User Experience, IT Operations Management]
---

# Sign and verify an ACC plugin

Sign an Agent Client Collector \(ACC\) plugin with a self-signed certificate and verify the signature so that endpoint devices can validate the plugin.

## Before you begin

-   The ACC plugin `tar.gz` file must be created on your local computer.
-   OpenSSL must be installed on your local computer.

Role required: admin

## Procedure

1.  Generate a 2048-bit RSA key and a corresponding self-signed certificate with one year validity by using the following command:

    ```
    openssl req -nodes -x509 -sha256 -newkey rsa:2048 -keyout "sign.key" -out "sign.crt" -days 365 -subj "/C=IN/ST=TG/L=HYD/O=servicenow/OU=acme/CN=sign"
    ```

    **Important:** Keep `sign.key` private. Anyone with this key can sign plugins that your agents trust. Don't distribute it to endpoint devices or upload it to the instance.

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
    openssl dgst -sha256 -verify pubkey.pem -signature sign.txt.sha256 *plugin name*.tar.gz
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

    The signed package \(`sign-test.tar.gz`\) is created one level up from `signed-plugin` and contains only these two files at its root, with no subfolder:

    -   `*plugin name*.tar.gz`: the original plugin archive
    -   `sign.txt.sha256_encode64.sig`: the Base64-encoded signature
10. Rename the signed package so that its file name matches the plugin name.

    ```
    mv ../sign-test.tar.gz ../*plugin name*.tar.gz
    ```

    The file name must match the plugin \(asset\) name. For example, if the plugin name is `dex-acc-custom`, name the signed package `dex-acc-custom.tar.gz`.

11. Copy and place the self-signed certificate \(`sign.crt`\) in the certificate directory \(`[agent_root]/cert`\) of the ACC agent using one of the following options:

    The certificate directory differs by operating system:

    -   macOS: `/Library/Application Support/servicenow/agent-client-collector/cert`
    -   Windows: `C:\ProgramData\ServiceNow\agent-client-collector\cert`
    -   Copy the file manually.
    -   Distribute the certificate to agent devices using a device management utility such as Jamf or Microsoft Intune.
12. Add the certificate to the agent trust store.

    For more information, see [Add a self-signed certificate to the OS truststore](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/add-certificate-trust-store.md).

13. Upload the signed ACC plugin to the ServiceNow instance.

    For more information, see [Create and edit Agent Client Collector plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/create-edit-assets.md).

    **Important:** Upload the signed package that you renamed to `*plugin name*.tar.gz`, not the original plugin archive inside it. If you upload the inner archive, the ACC logs show the error `couldn't get signature file full path`.


## What to do next

The sample certificate is valid for 365 days.

After the certificate expires, the ACC agent rejects any new plugins signed with it. To rotate the certificate, generate a new key and certificate, re-sign your plugins, and redistribute the new certificate to your agents.

