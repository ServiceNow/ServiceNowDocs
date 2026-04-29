---
title: CyberArk integration configuration
description: These procedures include both CyberArk and ServiceNow configuration tasks, including references to the appropriate CyberArk documentation.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# CyberArk integration configuration

These procedures include both CyberArk and ServiceNow configuration tasks, including references to the appropriate CyberArk documentation.

The credential identifier configured in the ServiceNow instance must be mapped to the credential name in the CyberArk vault. When looking up a credential, the MID Server finds the credential by matching the credential identifier to a name in vault, which must be unique. If the credential identifier is blank, then the MID Server finds the credential by IP address. To identify the credential by IP address, the system looks at the credential type to ensure that there is only one credential of that type at that address. An example of this might be when a Windows server and vCenter are both running on the same IP address. To support strict credential requirements like this in an SSH environment, a MID Server configuration parameter allows you to require that the credential type requested matches the type returned by CyberArk.

**Note:** The **Credential ID** field is the only field necessary to map your credentials to CyberArk, in all cases except for SNMPv3. The **Privacy Credential ID** field is optional and is required only when using SNMPv3 credentials and using a privacy protocol for the credentials. See [Configure the CyberArk credential identifier](../task/t_ConfigCyberArkCredIdentifr.md) for more details.

To configure your instance to obtain credentials from a CyberArk vault, complete these tasks in the order in which they appear below.

-   **[Configure the CyberArk vault and install the AIM API](../task/t_InstallCyberArkAIMAPI.md)**  
Configure the CyberArk vault to allow MID Server access and install the CyberArk AIM API on the MID Server machine.
-   **[Import the CyberArk JAR file](../task/t_ImportTheCyberArkJARFile.md)**  
Import the CyberArk JavaPasswordSDK.jar file into the instance to make it accessible to the MID Server.
-   **[Configure the MID Server for CyberArk AIM](../task/t_ConfigureTheMIDServerForCyberArk.md)**  
Configure the `config.xml` file to grant the MID Server access to the CyberArk vault with AIM API.
-   **[Configure the MID Server for CyberArk CCP](../task/t_ConfigureTheMIDServerForCyberArkCCP.md)**  
Configure the `config.xml` file to grant the MID Server access to the CyberArk CCP vault.
-   **[Configure CyberArk for SNMPv2 credentials](../task/t_ConfigCyberArkSNMPv2Cred.md)**  
If your system uses SNMPv2, you can create a special file to map the attribute in a credential to the community string.
-   **[Configure the CyberArk credential identifier](../task/t_ConfigCyberArkCredIdentifr.md)**  
Create the unique key that CyberArk can use to identify specific credentials in the external repository.
-   **[Configure AWS credentials on a CyberArk vault](../../cloud-provisioning-interface/task/create-cred-AWS.md#)**  
Configure your CyberArk vault with the AWS credentials to be retrieved for use by your instance.
-   **[Configure Azure credentials on a CyberArk vault](../../cloud-provisioning-interface/task/create-cred-azure.md)**  
Configure your CyberArk vault with the Azure credentials to be retrieved for use by your instance.

**Parent Topic:**[CyberArk credential storage integration](c_CyberArkCredStorageIntegrate.md)

