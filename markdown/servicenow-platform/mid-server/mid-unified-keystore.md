---
title: MID Server unified key store
description: The MID Server unified key store allows all products on the MID Server to use common certificates and key pairs. This feature allows applications to use the same secure communication channel to the MID Server that the MID Server uses to connect to the instance.Install custom certificates to unify the security channels for various applications.If the key store becomes corrupted or is accidentally deleted you can restore a backup of the MID Server key store. This is especially useful for key stores with custom key-pairs, because otherwise recreating custom key-pair data can be difficult and time consuming.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 12
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server unified key store

The MID Server unified key store allows all products on the MID Server to use common certificates and key pairs. This feature allows applications to use the same secure communication channel to the MID Server that the MID Server uses to connect to the instance.

<table id="table_m2t_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>When the MID Server starts, the common name \(CN\) of the certificate is inspected to identify if a custom certificate has been installed. If a custom certificate is detected, the creation of the certificate/keypair will be skipped and an attribute is set on the ecc\_agent record to indicate the usage of a custom certificate.

When a custom certificate is used, the **Re-key** UI-action is disabled on the instance for the MID Server. A new UI action called **Remove custom keypair** is available to switch back to using a self-signed certificate. Using this action will cause the MID Server to remove the custom certificate and generate a new self-signed certificate, similar to the re-key option.

When a MID is upgraded, any custom certificates that were installed will be retained.

## PEM bundle support

MID Server unified key store supports PEM bundle certificate and key pairs.

## Sample PEM bundle

```
-----BEGIN PRIVATE KEY----- 

MIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQC0pj5O8QKFpHy9 

... 

oPdU+h0grs9SJp6rFx0PzDY= 

-----END PRIVATE KEY----- 

Bag Attributes 

    friendlyName: <myCustomCert>

    localKeyID: 54 69 6D 65 20 31 35 39 35 33 35 34 32 30 38 30 35 31  

subject=/C=US/ST=CA/L=Santa Clara/CN=epic1016883 

issuer=/C=US/ST=CA/L=Santa Clara/CN=epic1016883 

-----BEGIN CERTIFICATE----- 

MIIDKzCCAhOgAwIBAgIEPqMQqDANBgkqhkiG9w0BAQsFADBGMQswCQYDVQQGEwJV 

... 

4g53RN+LqtJVeeQkZvIbZOfuSqypdVfudkS8dqxQALb8IuHUV7JOcBvOT79mSTs= 

-----END CERTIFICATE----- 
```

**Parent Topic:**[Securing and encrypting MID Server data](mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](mid-authentication-soap-requests.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[MID Server command audit log](mid-audit-log.md)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](mid-fips-enforced.md#)

[MID Server Governance](mid-timeout.md)

## Install custom certificates in the MID Server unified key store

Install custom certificates to unify the security channels for various applications.

### Before you begin

Role required: admin

When installing the certificate on a MID Server hosted in Linux, `install-certificate.sh` can be unresponsive if the Linux entropy pool count is less than a few hundred. Check the entropy count of the Linux pseudo random number generator \(PRNG\) with the following command:

```
cat /proc/sys/kernel/random/entropy_avail
```

If the entropy count is too low, you can install an entropy generator such as RNGD or Haveged. For more information about installing Haveged for CentOS and Ubuntu, see [How to Setup Additional Entropy for Cloud Servers Using Haveged](https://www.digitalocean.com/community/tutorials/how-to-setup-additional-entropy-for-cloud-servers-using-haveged).

### Procedure

1.  If the MID Server is running, stop the MID Server.

    **Note:**

    If the entry for alias **DefaultSecurityKeyPairHandle** is being modified, you must invalidate the MID Server before stopping it.

2.  Create a PEM bundle certificate and keypair by running one of the following commands in the MID Server install folder.

    -   Generate self-signed certificates for non-MTLS use cases with the command:

        ```
        openssl req -newkey rsa:2048 -nodes -keyout key.pem -x509 -days 365 -out certificate.pem
        ```

    -   Export the key store to a PEM bundle using the command:

        ```
        openssl pkcs12 -in <myCustomCert>.p12 -nodes -out <myCustomCert>.pem
        ```

    -   Get only certificates in the PEM format with the command:

        ```
        openssl pkcs12 -in <myCustomCert>.p12 -out <myCustomCert>.pem -clcerts -nokeys
        ```

    -   Get only keys in the PKCS\#8 format with the command:

        ```
        openssl pkcs12 -in <myCustomKey>.p12 -out <myPrivateKey>.key -nocerts -nodes
        ```

    -   Install the certificate, or certificate chain, and private key for Windows hosts using the command:

        ```
        bin/scripts/manage-certificates.bat -a <alias> <file path to PEM bundle>
        ```

    -   Install the certificate, or certificate chain, and private key for Linux hosts using the command:

        ```
        bin/scripts/manage-certificates.sh -a <alias> <file path to PEM bundle>
        ```

    **Note:**

    The header and footer of the PEM syntax must be the following:

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

3.  Start the MID Server.

4.  Validate the MID Server with the instance.

5.  To revert the MID Server to use a self-generated certificate, select the MID Server in the instance and use the UI action **Remove custom certificate**.

    **Note:** The MID Server can also be reverted using the **Invalidate** UI action. Invalidating a MID Server removes any custom certificates that are installed and creates a new self-signed certificate for the MID Server.


### What to do next

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


**Related topics**  


[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

## Restore the MID Server key store with a backup

If the key store becomes corrupted or is accidentally deleted you can restore a backup of the MID Server key store. This is especially useful for key stores with custom key-pairs, because otherwise recreating custom key-pair data can be difficult and time consuming.

### Before you begin

Role required: Agent admin

### About this task

Starting with the Tokyo release, the MID Server automatically makes a backup of the **agent\_keystore** file when it is changed. Backups are stored in **security\_backup** under the agent folder. They are stored outside the security folder to protect against accidental deletions or corruptions of the security folder.

In the backup folder, there is a dedicated backup log file: **keystore\_backup\_audit\_trail.log**. This log keeps track of backup files and backup activities. Each backup log entry has backup file name with a time stamp, a matching **keypairs.mid\_id**, and a list of aliases of key-pairs in the backup.

**Note:** For security purposes, the backup key store should have the same attributes as the original key store, such as owner, group, and permissions. Those attributes ensure the MID Server has the same protection at file system level.

The key store backups can be modified with the MID Server properties **mid.keystore.max\_backups**, **mid.keystore.max\_live\_backups**, and **mid.keystore.backup\_overwrite\_timespan**. See [MID Server properties](../reference/r_MIDServerProperties.md#) for more information.

### Procedure

1.  Stop MID Server.

2.  Navigate to the **security\_backup** and view the **keystore\_backup\_audit\_trail.log** to choose which backup to restore.

3.  Copy that backup to the **agent\_keystore** file in the security folder.

    Check the file permissions to make sure that it has the same owner and permissions as the original one. If **agent\_keystore** already exists in that location, overwrite it with the backup.

4.  Check **config.xml** to make sure that the **keypairs.mid\_id** matches the one in the audit log file.

5.  If the **keypairs.mid\_id** do not match, update **config.xml** to match them.

6.  Navigate to the instance and invalidate the MID server.

    This will create a **delete\_mid\_keypair** system command in the **ecc\_queue**.

7.  Find all **delete\_mid\_keypair** output messages for the MID Server and mark them as processed.

    The goal is to mark the MID Server as invalidated without triggering the key-pair deletion. Unless the system commands are marked as processed, MID Server deletes the **defaultsecuritykeypairhandle** key-pair regardless of whether it is custom or auto-generated.

8.  Restart MID Server.

9.  Navigate to the instance and validate the MID Server.


