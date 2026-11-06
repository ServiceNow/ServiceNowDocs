---
title: MID Server configuration file security
description: Sensitive MID Server configuration data can be protected using several different schemes, including internal and external data encryption and external data storage.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
---

# MID Server configuration file security

Sensitive MID Server configuration data can be protected using several different schemes, including internal and external data encryption and external data storage.

<table id="table_vbn_2v4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>The MID Server uses one secured configuration provider at a time. You can use either the default security provider or CyberArk as the secured configuration provider. Mixed provider configurations are not supported. For example, you cannot use the default security provider together with CyberArk. The following built-in security options are available:

-   **Default security provider**: Secures the data in the **config.xml** file by encryption. When the MID Server is restarted, any unencrypted data is encrypted and written to the **config.xml** file. The default security provider offers these encryption options:
    -   **Default encryptor**: Default process for encrypting data in the MID Server **config.xml** file. See [Encrypt or decrypt MID Server configuration file values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-manual-encryption.md) for details.
    -   **Windows Data Protection API \(DPAPI\)**: The operating system performs the data encryption, rather than the MID Server. DPAPI encryption is based on the logged in user's account. When this scheme is used, the data can only be decrypted by the same user account. If the account changes, the data must be re-encrypted.
    -   **Custom encryption**: Implement the [IMidServerEncrypter interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-encrypter-interface.md) to create your own custom encryption scheme to manage sensitive **config.xml** data.
-   **CyberArk**: Data security is provided by [CyberArk integration configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_CyberArkIntegrationConfiguration.md), which moves sensitive data from the **config.xml** file to a secure CyberArk vault. This solution does not encrypt the data and does not use the IMidServerEncrypter interface.
-   **Custom external storage**: Implement the [ISecuredConfigProvider interface](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-secured-config-interface.md) to create your own custom external storage system to manage sensitive **config.xml** data.

\[Omitted image "SecuredMIDConfigFileDiagram.png"\] Alt text: Secured content and encryption schemes

