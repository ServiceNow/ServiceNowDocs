---
title: Enable MID Server mutual authentication
description: Configure the MID Server to use a client certificate for authenticating to the instance. This avoids the need to create a basic authentication credentials in the Key Store for the MID Server's configuration.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Enable MID Server mutual authentication

Configure the MID Server to use a client certificate for authenticating to the instance. This avoids the need to create a basic authentication credentials in the Key Store for the MID Server's configuration.

## Before you begin

Role required: admin

<table id="table_jjd_jmj_bpb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## About this task

MID Server mutual authentication removes the MID Server user name and password and provides a client certificate for authentication. Whenever a server requests authentication, this certificate is sent instead. To use mutual authentication, certificate based authentication must be enabled. See [Set up Certificate-based authentication](https://www.servicenow.com/docs/access?context=set-up-mutual-auth&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) for the procedure.

If a new MID Server is created with mutual authentication, it does not add capabilities automatically. An administrator must add capabilities to its record on the instance. However, existing MID Servers using basic authentication with capabilities are preserved when switching to mutual authentication.

A MID Server using mutual authentication cannot be re-keyed or validated as a UI action on the instance.

Self-signed certificates are not supported with mutual authentication. Internally signed certificates are only supported when signed by a private certificate authority. Commercially signed certificates are supported when signed by a commonly trusted certificate authority, such as those trusted by browsers and operating systems.

In the Quebec release, a MID Server using the Health Log Analytic application cannot be configured with mutual authentication.

## Procedure

1.  Contact ServiceNow support to request mutual authentication on the MID Server.

2.  Obtain a certificate and private key from a respected certificate authority.

    MID Server mutual authentication only supports the PEM bundle format and private key in PCKS\#8 format. The bundle must have both the private key and certificate. Open the certificate using a text editor and see if it is in text format. The header and footer of the PEM syntax is the following:

    ```
     -----BEGIN CERTIFICATE----- 
    ```

    ```
     -----END CERTIFICATE----- 
    ```

    ![The bundle contains the correct formatting and both the private key and certificate.](../image/install-mid-mutual-auth-bundle.png)

    You can read the contents of a PEM certificate using the `openssl` command on Linux or Windows as follows: `openssl x509 -in cert.crt -text`. The private key must be in the PKCS\#8 format. The header and footer of the PKCS\#8 syntax is the following:

    ```
     -----BEGIN PRIVATE KEY----- 
    ```

    ```
     -----END PRIVATE KEY----- 
    ```

      You can check the contents of a private key using the `openssl` command on Linux or Windows as follows: `openssl rsa -in private.key -check`

    **Note:** If your certificate is not in PKCS\#8 format, you get an error: `- main SEVERE *** ERROR *** Could not find valid private key`

3.  Split up the PEM certificate into 3 different PEM files.

    1.  Private key and leaf certificate
    2.  Leaf certificate
    3.  Intermediate certificates and root certificate
4.  On the instance, upload file containing the intermediate and root certificates to the CA Certificate Chain table: **sys\_ca\_certificate.list**.

    **Note:** If uploading individually instead of a bundle, start with the root certificate, and then the intermediate certificate\(s\). It is preferrable to uploade this file as a PEM bundle, whose type is set to CA Cert, instead of splitting it into multiple files.

5.  Check the uploaded CA Cert record on the instance and wait for the **Publish Status** to change to **Exists**.

    **Note:** Do not proceed until the publish status is updated to **Exists**.

6.  On the instance, navigate to **sys\_user\_certificate.list**.

7.  Attach only the leaf certificate to **sys\_user\_certificate.list** without including the private key.

8.  If the MID Server is validated, invalidate the MID Server before continuing.

9.  Create a new record.

    **Note:** The record must have the MID Server's name and the **User Role** must be **MID Server**.

10. Attach the original, unsplit PEM certificate to the record.

    ![The attachment is in the top corner of the record.](../image/mid-mtls-user-cert-record.png)

    **Note:** Ensure that the attached file contains only the certificate.

11. If the MID Server is running, stop the MID Server.

12. On the MID Server host machine, run the following commands to install and manage the certificate and private key.

    Run the script from the root of the agent directory because it requires the jar files in the class path. The security directory is then created in the agent root folder and is used by MID Server. For example: `bin/scripts/manage-certificates.bat -m.`

    The **manage-certificates** has the following functions and the scripts must be run from the agent folder.

    -   **Enable mutual authentication​**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -m`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -m`

    -   **Remove mutual authentication and restore back basic authentication**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -b <myUserName myPassword>`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -b <myUserName myPassword>`

    -   **Add new certificates and certificate chains with a specified alias​**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -a <alias> <fileName>`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -a <alias> <fileName>`

        The `alias` is a unique name given to the certificate being imported. The MID Server requires a custom certificate for mutual authentication, with the default alias name `defaultsecuritykeypairhandle`. To configure MTLS communication between the MID Server and instance, the certificate entry must be added to the key store using the alias name `defaultsecuritykeypairhandle`.

        The `fileName` is a file path that can contain a PEM certificate, or certificate chain, and a PCKS\#8 private key. The file path to the PEM bundle can contain multiple certificates and a single private key. The header and footer of each PEM certificate must be the following:

        ```
         -----BEGIN CERTIFICATE----- 
        ```

        ```
         -----END CERTIFICATE----- 
        ```

        The header and footer of the PKCS\#8 syntax must be the following:

        ```
         -----BEGIN PRIVATE KEY----- 
        ```

        ```
         -----END PRIVATE KEY----- 
        ```

        An exception is thrown if the certificate chain fails validation. If the file contains multiple certificates, they must be ordered: leaf certificate, intermediate certificates, then root certificates.

    -   **Display certificate details for the specified alias**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -g <alias> ​`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -g <alias> ​`

        This command displays information such as subject distinguished name, issuer name, and expiry date from the certificate.

    -   **List all existing aliases**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -l`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -l`

        This command lists all the alias names available in the **agent\_keystore**.

    -   **Delete certificates using an alias​**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -d <alias>`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -d <alias>`

        This command deletes the alias and record from the keystore. The entry for alias **DefaultSecurityKeyPairHandle** can be deleted using this command.

    -   **Remove all entries from the keystore**

        For Windows, use the command: `bin/scripts/manage-certificates.bat -r ​`

        For Linux, use the command: `./bin/scripts/manage-certificates.sh -r ​`

        This command deletes the existing entries from the keystore, except alias **DefaultSecurityKeyPairHandle**. ​

13. Start the MID Server.


**Parent Topic:**[Securing and encrypting MID Server data](../concept/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](../concept/mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](../concept/mid-authentication-soap-requests.md#)

[MID Server unified key store](../concept/mid-unified-keystore.md#)

[MID Server Azure Key Vault integration](mid-azure-key-vault-integration.md#)

[MID Server command audit log](../concept/mid-audit-log.md)

[Rekey a MID Server](t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](../concept/mid-fips-enforced.md#)

[MID Server Governance](../concept/mid-timeout.md)

[Install custom certificates in the MID Server unified key store](../concept/mid-unified-keystore.md#)

[MID Server unified key store](../concept/mid-unified-keystore.md#)

