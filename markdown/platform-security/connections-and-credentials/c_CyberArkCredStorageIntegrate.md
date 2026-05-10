---
title: CyberArk credential storage integration
description: The MID Server integration with the CyberArk vault enables ServiceNow Orchestration, ServiceNow Discovery, and ServiceNow Service Mapping to run without storing any credentials on the instance.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# CyberArk credential storage integration

The MID Server integration with the CyberArk vault enables ServiceNow® Orchestration, ServiceNow® Discovery, and ServiceNow® Service Mapping to run without storing any credentials on the instance.

## Introduction to CyberArk

CyberArk Application Identity Management \(AIM\) product uses the Privileged Account Security solution to eliminate the need to store application passwords embedded in applications, scripts or configuration files, and allows these highly sensitive passwords to be centrally stored, logged, and managed within the CyberArk vault. This approach enables organizations to comply with internal and regulatory requirements of periodic password replacement and to monitor activities associated with all types of privileged identities, whether on-premise or in the cloud.

The instance maintains a unique identifier for each credential, the credential type \(such as SSH, SNMP, or Windows\), and any credential affinities. The MID Server obtains the credential identifier, credential type, and IP address from the instance, and then uses the CyberArk vault to resolve these elements into a usable credential. The credential resolver can also look up the hostname, fqdn, and use reverse DNS lookup to get fqdn.

The CyberArk integration requires the ServiceNow® [External Credential Storage plugin](../task/t_ActivateExtrnlCredStoragePlugIn.md), which is available in **System Definitions** &gt; **Plugins**. The MID Server and CyberArk AIM/API client must be installed on the same machine. CyberArk Application Access Manager \(AAM\) Credential Providers version 12.0.1 and later is supported.

## Installed with CyberArk

-   **Business rule**: The External Credential Storage business rule performs the following tasks when an administrator makes any change to the external credential storage property:
    -   Changes the view for the Credentials record list and form to the External Storage view. This view enables users to see the Credential ID column in the list.
    -   Instructs the MID Server to refresh its non-external credentials cache in preparation for a change in the way that credentials are obtained.
-   **System property**: A property called Enable External Credential Storage \[com.snc.use\_external\_credentials\] enables or disables the External Credential Storage plugin after it is activated. This property is located in **Discovery Definition** &gt; **Properties** and **Orchestration** &gt; **MID Server Properties**, and is enabled when you activate the plugin.

    **Note:** If you disable external credential storage with the system property, the system automatically sets all the external credentials to inactive in the instance. If you re-enable the feature with this property, the system does not reset the external credential records to active. You must reactivate each credential record manually.


## Supported credential types

The CyberArk integration supports these ServiceNow credential types:

-   GCP
-   Azure
-   CIM
-   JMS
-   SNMP forum
-   SNMPv3
-   Basic Auth
-   SSH Key Pair
-   SSH Private Key \(with key, pass phrase, and password\)
-   VMware
-   Windows
-   Applicative Credentials

**Note:** To use CyberArk integration with the GCP credential type, you must modify the external credential storage jar. For details see [ServiceNow GCP Credential Resolver using CyberArk](https://www.servicenow.com/community/itom-blog/servicenow-gcp-credential-resolver-using-cyberark/ba-p/2272452).

ServiceNow AI Platform features that use these network protocols also support the use of credentials stored on a CyberArk vault.

|Network protocol|ServiceNow® Workflow Studio support|Orchestration support|
|----------------|-----------------------------------|---------------------|
|SOAP|SOAP Step|[Create a SOAP web service activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateASOAPWebServiceActivity.md) with basic authentication overrides|
|REST|REST Step|[Create a REST web service activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateARESTWebServiceActivity.md) with basic authentication overrides|
|JDBC|JDBC Step|JDBC activity|
|SSH|SSH Step|SSH activity|
|PowerShell|PowerShell Step|PowerShell activity|
|SFTP|SFTP Step|SFTP activity|
|JMS| |JMS activity|

**Important:** You cannot manage credentials stored on a CyberArk vault and a custom [external credential storage](c_ExternalCredentialStorage.md) system using the same MID Server. The MID Server and CyberArk AIM/API client must be installed on the same machine.

## CyberArk architecture

![CyberArk storage architecture.](../image/CyberArkArchitectureDiagram.png "CyberArk storage architecture")

**Note:** CyberArk uses the base system mid.jar file for resolving credentials.

## How the MID Server handles Windows accounts

Credential lookup initially attempts to match the specified credential ID to an existing value in the CyberArk vault **Name** field. If a match is found, that credential is returned. If no match is found, the credential lookup attempts to find a match using the IP address. If the IP address lookup matches more than one credential, such as Windows and Tomcat on the same server, the lookup fails. To avoid this issue, set the **ext.cred.type\_specifier** parameter in the MID Server config.xml file to **true** to force CyberArk to return credentials that match both the credential type and the IP address. For example, if an IP address is shared by both Windows and Tomcat, a credential type of Windows returns the Windows credential only.

## Upgrade the CyberArk library

You can upgrade the CyberArk library if a secured configuration parameter is needed.

Check the following configuration parameter in the **config.xml**: `<parameter name="mid.secure_config.provider" value="com.service_now.mid.services.config.CyberArkSecuredConfigProvider"/>`

Perform the following steps to perform the upgrade if a secured config parameter provider is configured.

1.  Rename the CyberArk client version to `JavaPasswordSDK_MajorVersion_minorVersion_patchNum.jar`.
2.  Create a new jar entry in the `ecc_agent` table where the rename jar can be attached. This new entry downloads to the MID Server. This step results in two jar \(Passworsdk.jar and JavaPasswordSDK \_12\_X\_X.jar\).
3.  Delete old ecc\_agent entry from instance. This step deletes Passworsdk.jar from the MID Server, and the JavaPasswordSDK \_12\_X\_X.jar remains in the system.

-   **[CyberArk integration configuration](c_CyberArkIntegrationConfiguration.md)**  
These procedures include both CyberArk and ServiceNow configuration tasks, including references to the appropriate CyberArk documentation.

**Parent Topic:**[External credential storage](c_ExternalCredentialStorage.md)

