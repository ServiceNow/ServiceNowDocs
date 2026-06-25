---
title: MID Server configuration file security
description: Sensitive MID Server configuration data can be protected using several different schemes, including internal and external data encryption and external data storage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-encrypter-api.html
release: australia
product: MID Server
classification: mid-server
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 8
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server configuration file security

Sensitive MID Server configuration data can be protected using several different schemes, including internal and external data encryption and external data storage.

<table id="table_vbn_2v4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>The MID Server uses one secured configuration provider at a time. You can use either the default security provider or CyberArk as the secured configuration provider. Mixed provider configurations are not supported. For example, you cannot use the default security provider together with CyberArk. The following built-in security options are available:

-   **Default security provider**: Secures the data in the **config.xml** file by encryption. When the MID Server is restarted, any unencrypted data is encrypted and written to the **config.xml** file. The default security provider offers these encryption options:
    -   **Default encryptor**: Default process for encrypting data in the MID Server **config.xml** file. See [Encrypt or decrypt MID Server configuration file values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-manual-encryption.md) for details.
    -   **Windows Data Protection API \(DPAPI\)**: The operating system performs the data encryption, rather than the MID Server. DPAPI encryption is based on the logged in user's account. When this scheme is used, the data can only be decrypted by the same user account. If the account changes, the data must be re-encrypted.
    -   **Custom encryption**: Implement the [IMidServerEncrypter interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-encrypter-interface.md) to create your own custom encryption scheme to manage sensitive **config.xml** data.
-   **CyberArk**: Data security is provided by [CyberArk integration configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_CyberArkIntegrationConfiguration.md), which moves sensitive data from the **config.xml** file to a secure CyberArk vault. This solution does not encrypt the data and does not use the IMidServerEncrypter interface.
-   **Custom external storage**: Implement the [ISecuredConfigProvider interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-secured-config-interface.md) to create your own custom external storage system to manage sensitive **config.xml** data.

\[Omitted image "SecuredMIDConfigFileDiagram.png"\] Alt text: Secured content and encryption schemes

-   **[Encrypt MID Server configuration data with DPAPI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-data-encrypt-with-dpapi.md)**  
Windows Data Protection API \(DPAPI\) encrypts sensitive data from the **config.xml** file, based on the MID Server user account.
-   **[Use CyberArk as a secure configuration provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/use-cyberark-secure-config-provider.md)**  
You can use a CyberArk vault to secure any sensitive data from the MID Server **config.xml** file.
-   **[Change MID Server configuration file security schemes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/change-mid-server-security-schemes.md)**  
The MID Server provides several schemes for securing sensitive data in the **config.xml** file and allows you to switch between these options to suit your security requirements.
-   **[MID Server ISecuredConfigProvider interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-secured-config-interface.md)**  
Use the methods in this interface to create custom providers that manage secured parameter values in the MID Server **config.xml** file.
-   **[MID Server IMidServerEncrypter interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-encrypter-interface.md)**  
Use the methods in this interface to create a custom external encrypter for the MID Server **config.xml** file.

**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[Encrypt or decrypt MID Server configuration file values]()

[MID Server authentication credentials and SOAP requests]()

[MID Server unified key store]()

[Enable MID Server mutual authentication]()

[MID Server Azure Key Vault integration]()

[MID Server command audit log]()

[Rekey a MID Server]()

[Add SSL certificates for the MID Server]()

[Specify an external TrustStore for the MID Server]()

[MID Server SSH cryptographic algorithms]()

[Attach a script file to a file synchronized MID Server]()

[MID Server FIPS Enforced Mode]()

[MID Server Governance]()

