---
title: Configure the MID Server for CyberArk
description: Configure the config.xml file to grant the MID Server access to the CyberArk vault.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Getting started with credentials, Connections and Credentials, Access Management]
---

# Configure the MID Server for CyberArk

Configure the `config.xml` file to grant the MID Server access to the CyberArk vault.

## Before you begin

Role required: admin

Before starting this procedure, import the `JavaPasswordSDK.jar` file into the instance.

## Procedure

1.  Manually configure the MID Server [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&section=t_SetMIDServerParameters&ft:locale=en-US) file with these parameters.

    This configuration cannot be done from the instance.

    |Parameter|Value|Description|
    |---------|-----|-----------|
    |ext.cred.safe\_folder|NameOfFolder|Folder to use for all credential lookups. For example, **root**.|
    |ext.cred.use\_cyberark|true|Boolean parameter indicating that this MID Server is integrated with CyberArk.|

<table id="table_kqv_3nz_st"><thead><tr><th>

Parameter

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ext.cred.safe\_timeout

</td><td>

5 \(sec\)

</td><td>

Timeout of each credential lookup in the vault, specified in seconds.

</td></tr><tr><td>

ext.cred.safe\_name

</td><td>

NameOfSafe

</td><td>

Default safe name used for all credential lookups. If parameters are in multiple safes, the credential ID may be specified in the format **&lt;safeName&gt;:&lt;CredentialID&gt;**. When configured like this, the **NameOfSafe** field is ignored. If all external credentials have their credential IDs specified in this format, then leave out the **NameOfSafe** field.**Note:** By default the separator character in this format is a colon. To assign any character you want as a separator, add this line to the `CredMap.properties` file: `safe.cred.split.string=<string>`.

</td></tr><tr><td>

ext.cred.app\_id

</td><td>

ServiceNow\_MID\_Server

</td><td>

Specifies the App-ID used to grant permission to the MID Server to access the CyberArk vault. The default value, **ServiceNow\_MID\_Server**, must be defined in the CyberArk vault. You can use this parameter to override the default and specify your own App-ID. If you edit the App-ID in this parameter, make sure to configure CyberArk to match.

</td></tr><tr><td>

ext.cred.type\_specifier

</td><td>

true

</td><td>

Forces an IP address lookup to return credentials that match both the CyberArk platform ID and the IP address. For example, if an IP address is shared by both Windows and Tomcat, a credential with a platform ID starting with **Win** returns the Windows credential only. When this parameter is set to true, CyberArk looks for platform IDs that begin with:-   Win: Windows
-   Unix: SSH
-   VMWare: VMware


</td></tr><tr><td>

ext.cred.check\_ssh\_type

</td><td>

false

</td><td>

When set to true, requires that the type of SSH credential returned from CyberArk matches the type of credential requested. For example, if a normal SSH username/password credential is requested and only SSH keys are available, the credential lookup fails.

</td></tr></tbody>
</table>
**Parent Topic:**[CyberArk integration configuration](../concept/c_CyberArkIntegrationConfiguration.md)

