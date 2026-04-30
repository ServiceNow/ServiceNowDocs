---
title: Securing and encrypting MID Server data
description: After configuring your MID Server, you can add security by encrypting MID Server parameter values in the config.xml file. Encryption protects data that the MID Server returns to the ECC Queue. Other available security options include the authorization of SOAP requests, restricting access to the MID Server configuration file, and establishing secure socket layer \(SSL\) connections.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Securing and encrypting MID Server data

After configuring your MID Server, you can add security by encrypting MID Server parameter values in the `config.xml` file. Encryption protects data that the MID Server returns to the ECC Queue. Other available security options include the authorization of SOAP requests, restricting access to the MID Server configuration file, and establishing secure socket layer \(SSL\) connections.

<table id="table_u22_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## How MID Server password encryption works

The **username** and **password** are initially set in the `config.xml` file on the MID Server. When the MID Server retrieves the credentials, it replaces the clear-text password with an encrypted password automatically, using an AES256 encryption algorithm. In continued efforts to improve MID Server security, the encryption algorithm has been enhanced. The MID Server also maintains an encryption key that is generated each time it starts and remains in memory and not on the hard disk. When credentials need to be sent from the instance to the MID Server, the following process takes place:

1.  The instance retrieves the encrypted **password** and the unencrypted **username** from the instance database table.
2.  The instance decrypts the encrypted **password**, and then re-encrypts it using the MID Server encryption key.
3.  The **username** and re-encrypted **password** are sent to the MID Server through the encrypted TLS session was already established between the MID server and the instance.
4.  The MID Server receives the credentials and decrypts the **password** in memory before using the credentials for remote operations. At no point is the credential password stored on the disk in an unencrypted format.

-   **[MID Server certificate check policies](mid-security-checks.md)**  
MID Server uses three kinds of security checks to secure external traffic. The security checks use TLS/SSL certificate validation, hostname validation, and OCSP validation to improve security. Control these security checks with the MID Server certificate check policies table.
-   **[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)**  
The value of any MID Server parameter in the `config.xml` file can be encrypted. The attributes for all encrypted values are managed from within the configuration file, including the security attribute of the login password.
-   **[MID Server configuration file security](../reference/mid-server-encrypter-api.md)**  
Sensitive MID Server configuration data can be protected using several different schemes, including internal and external data encryption and external data storage.
-   **[MID Server authentication credentials and SOAP requests](mid-authentication-soap-requests.md#)**  
Set basic authentication credentials to update the web service invocation data. For added security, you can enforce basic authentication on each incoming SOAP request to the MID Server.
-   **[MID Server unified key store](mid-unified-keystore.md#)**  
The MID Server unified key store allows all products on the MID Server to use common certificates and key pairs. This feature allows applications to use the same secure communication channel to the MID Server that the MID Server uses to connect to the instance.
-   **[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)**  
Configure the MID Server to use a client certificate for authenticating to the instance. This avoids the need to create a basic authentication credentials in the Key Store for the MID Server's configuration.
-   **[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)**  
The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.
-   **[MID Server command audit log](mid-audit-log.md)**  
The command audit log records the commands run by the MID Server for the Discovery application. Review the commands to check for anomalies or errors.
-   **[Rekey a MID Server](../task/t_RekeyAMIDServer.md)**  
Rekey a MID Server to generate a new private key. Private keys are used to decrypt automation credentials, so that MID Servers can transmit information securely. Key pairs are initially generated when a MID Server is validated, and MID Servers should be rekeyed periodically to meet security requirements.
-   **[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)**  
Configure the MID Server to connect to a source over SSL.
-   **[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)**  
The MID Server utilizes SSH clients to perform many discovery actions. During the SSH handshake, both the client and server first determine which algorithms both parties support, then client picks the highest priority algorithm. For the Host Key Algorithm, the client picks highest priority algorithm which both parties support that matches the key type.
-   **[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)**  
You can attach a script file to synchronize to a connected MID Server. Windows Internet Explorer enhanced security blocks downloaded files that it determines are potentially dangerous. However synchronizing the files avoids this security problem.
-   **[MID Server FIPS Enforced Mode](mid-fips-enforced.md#)**  
The MID Server supports the National Security Cloud \(NSC\) IL-5 environment, which requires all utilized cryptography to be FIPS validated. The MID server can be run in FIPS Enforced Mode, where only cryptographic algorithms which are FIPS validated are utilized.
-   **[MID Server Governance](mid-timeout.md)**  
Improve MID Server security by setting an automatic timeout to invalidate and shut down inactive MID Servers. You can enable this feature and set the inactivity timeout period globally and for each MID Server.

**Parent Topic:**[Manage instance data sources](../../../administer/general/concept/manage-data-sources.md)

