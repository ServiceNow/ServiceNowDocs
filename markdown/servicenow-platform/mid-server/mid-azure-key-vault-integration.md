---
title: MID Server Azure Key Vault integration
description: The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.The MID Server supports specified credentials for integration with the Azure Key vault.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Azure Key Vault integration

The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.

## Before you begin

To install the required application on the instance, navigate to **Plugin Manager** &gt; **External Credential Storage and Management**.

<table id="table_m2t_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>Role required: External Credential Storage and Management application Scope ID is required: com.sn\_mid\_extcredstrg

## About this task

When setting up access to the Azure Key Vault, the MID Server is either within the Azure environment or it is on an external virtual machine. This procedure covers setting up the Azure Key Vault for a MID Server within the Azure environment.

For more information about specific Azure and Azure Key Vault procedures, see the [Azure Key Vault documentation](https://learn.microsoft.com/en-us/azure/key-vault/).

## Procedure

1.  Within the Azure cloud environment, create a virtual machine.

2.  Navigate to the Identity section of that virtual machine.

3.  Enable system assigned identity.

    Once it is enabled, you have the option to assign a role for that identity.

4.  Navigate to the **Add role assignment** menu.

5.  Set the scope to your Subscription.

6.  Add the Key Vault administrator role.

7.  Set the resource to the key vault that you want to integrate with the MID Server.


**Parent Topic:**[Securing and encrypting MID Server data](../concept/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](../concept/mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](../concept/mid-authentication-soap-requests.md#)

[MID Server unified key store](../concept/mid-unified-keystore.md#)

[Enable MID Server mutual authentication](install-mid-mutual-auth.md)

[MID Server command audit log](../concept/mid-audit-log.md)

[Rekey a MID Server](t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](../concept/mid-fips-enforced.md#)

[MID Server Governance](../concept/mid-timeout.md)

## Azure Key Vault Integration for External Virtual Machine MID Servers

The MID Server integration with the Azure Key vault enables Orchestration, Discovery, and Service Mapping to run without storing any credentials on the instance.

### Before you begin

Role required: External Credential Storage and Management application \(Scope ID:**com.sn\_mid\_extcredstrg**\) is required.

### About this task

When setting up access to the Azure Key Vault, the MID Server is either within the Azure environment or it is on an external virtual machine. This procedure covers setting up the Azure Key Vault for a MID Server that is on an external virtual machine.

For more information about specific Azure and Azure Key Vault procedures, see the [Azure Key Vault documentation](https://learn.microsoft.com/en-us/azure/key-vault/).

### Procedure

1.  In the Azure portal, navigate to App registrations.

2.  Create a new application for the MID Server.

3.  Take a note of the **tenant id** and **client id** because these are used later.

4.  Provide API Permission for Azure Key Vault to the application.

5.  Navigate to **Certificates and Secrets** for the new application.

6.  Generate a new client secret and take a note of that client secret.

    At this point, you should have the **client\_id**, **tenant\_id**, and **secret\_key** for the application registration.

7.  Add the following parameters to the MID Server **config.xml** using the recorded values.

    ```
    <parameter name="ext.cred.azure.vault_name" secure="false" value="<azure_key_vault_name>"/> (optional) 
    <parameter name="ext.cred.azure.tenant_id" secure="true" value="<tenant_id_value>"/> 
    <parameter name="ext.cred.azure.client_id" secure="true" value="<client_id_value>"/> 
    <parameter name="ext.cred.azure.secret_key" secure="true" value="<secret_key_value>"/> 
    ```


## Supported Credentials for Azure Key Vault Integration

The MID Server supports specified credentials for integration with the Azure Key vault.

### List of Credentials

-   **SNMPV3 Credentials**

    ```
      {
        "type": "snmpv3",
        "user": "<user_value>",
        "authentication_key": "<authentication_key_value>",
        "privacy_protocol": "<privacy_protocol_value>",
        "privacy_key": "<privacy_key_value>",
        "authentication_protocol": "<authentication_protocol_value>",
        "snmp_context": "<snmp_context_value>"
      }
    ```

-   **VMWare Credentials**

    ```
      {
        "type": "vmware",
        "password": "<password_value>",
        "user": "<user_value>"
      }
    ```

-   **SSH Credentials**

    ```
      {
        "type": "ssh",
        "password": "<password_value>",
        "user": "<user_value>"
      }
    ```

-   **Windows Credentials**

    ```
      {
        "type": "windows",
        "password": "<password_value>",
        "user": "<user_value>",
        "domain": "<domain_value>" // If it is null or empty, user name will become `.\user`
      }
    ```

-   **Azure Service Principal Credentials**

    ```
      {
        "type": "azure",
        "client_id": "<client_id_value>",
        "tenant_id": "<tenant_id_value>",
        "secret_key": "<secret_key_value>"
      }
    ```

-   **SSH Private Key Credentials**

    ```
      {
        "type": "ssh_private_key",
        "password": "<password_value>", // optional
        "user": "<user_value>",
        "ssh_certificate": "<ssh_certificate_value>",
        "ssh_private_key": "<ssh_private_key_value>",
        "ssh_passphrase": "<ssh_passphrase_value>" // optional
      }
    ```

-   **AWS Credentials**

    ```
      {
        "type": "aws",
        "access_key": "<access_key_value>",
        "secret_key": "<secret_key_value>"
      }
    ```

-   **API Key Credentials**

    ```
      {
        "type": "api_key",
        "api_key": "<api_key_value>"
      }
    ```

-   **Applicative Credentials**

    ```
      {
        "type": "<applcation_type>", // generated by JSON builder: TODO
        "password": "<password_value>",
        "user": "<user_value>"
      }
    
    ```

-   **Azure Enterprise Agreement Credentials**

    ```
      {
        "type": "ea_azure",
        "access_key": "<access_key_value>",
        "enrollment_number": "<enrollment_number>"
      }
    ```

-   **Azure SAS Credentials**

    ```
      {
        "type": "azure_sas",
        "sas_key": "<sas_key_value>",
        "sas_key_name": "<sas_key_name_value>"
      }
    ```

-   **Basic Auth Credentials**

    ```
      {
        "type": "basic_auth",
        "password": "<password_value>",
        "user": "<user_value>"
      }
    ```

-   **CIM Credentials**

    ```
      {
        "type": "cim",
        "password": "<password_value>",
        "user": "<user_value>"
      }
    ```

-   **Cloud Foundry Credentials**

    ```
      {
        "type": "sn_itom_pattern_pcf",
        "password": "<password_value>",
        "user": "<user_value>",
        "ssh_private_key": "<ssh_private_key_value>",
        "ssh_passphrase": "<ssh_passphrase_value>"
      }
    ```

-   **Google API Credentials**

    ```
      {
        "type": "gcp",
        "email": "<email_value>",
        "secret_key": "<secret_key_value>"
      }
    ```

-   **SSL Keystore Credentials**

    ```
      {
        "type": "keystore",
        "keystore_password": "<keystore_password_value>",
        "keystore_path": "<keystore_path_value>",
        "key_password": "<key_password_value>"
      }
    ```

-   **JMS Credentials**

    ```
      {
        "type": "jms",
        "password": "<password_value>",
        "user": "<user_value>"
      }
    ```

-   **SNMP Community Credentials**

    ```
      {
        "type": "snmp",
        "password": "<password_value>"
      }
    ```

-   **SSL Credentials**

    ```
      {
        "type": "keystore",
        "user": "<user_value>",
        "password": "<password_value>",
        "additional_properties": "<additional_properties_value>",
        "key_password": "<key_password_value>",
        "keystore": "<keystore_value>",
        "keystore_password": "<keystore_password_value>",
        "keystore_type": "<keystore_type_value>",
        "ssl_provider_name": "<ssl_provider_name_value>",
        "security_protocol": "<security_protocol_value>",
        "truststore": "<truststore_value>",
        "truststore_password": "<truststore_password_value>",
        "truststore_type": "<truststore_type_value>"
      }
    ```

-   **IBM Credentials**

    ```
      {
        "type": "ibm",
        "user": "<user_value>",
        "password": "<password_value>",
        "softlayer_user": "<softlayer_user_value>",
        "softlayer_key": "<softlayer_key_value>",
        "bluemix_key": "<bluemix_key_value>"
      }
    ```


### Gov Cloud Support for Azure Key Vault Integration

You may need to override authentication and the vault URL when operating in government cloud environments. The following examples are for US government clouds.

-   **Auth endpoint:**

    For US government clouds: https://login.microsoftonline.us/%s/oauth2/v2.0/token

    For US government cloud support: `<paramter name="ext.cred.azure.vault_auth_endpoint" value="https://login.microsoftonline.us/%s/oauth2/v2.0/token"/>`

-   **__Scope:__**

    For US government clouds: https://vault.usgovcloudapi.net/.default

    `<paramter name="ext.cred.azure.endpoint_scope" value="https://vault.usgovcloudapi.net/.default"/>`

    For Germany government clouds: https://vault.microsoftazure.de/.default

    For Chinese government clouds: https://vault.azure.cn/.default


