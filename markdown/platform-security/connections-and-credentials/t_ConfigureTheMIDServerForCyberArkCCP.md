---
title: Configure the MID Server for CyberArk CCP
description: Configure the config.xml file to grant the MID Server access to the CyberArk CCP vault.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [CyberArk integration configuration, CyberArk credential storage integration, External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# Configure the MID Server for CyberArk CCP

Configure the `config.xml` file to grant the MID Server access to the CyberArk CCP vault.

## Before you begin

Role required: admin

## About this task

**Note:**

In the Zurich family release, the instance needs an additional Update Set that can be downloaded from [Enable CyberArk Central Credential Provider \(CCP\) Integration in Zurich Release \[KB2682524\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2682524). Follow the provided installation steps. The Australia family release includes this script by default.

## Procedure

1.  Manually configure the MID Server [Add a MID Server parameter](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=zurich&pubname=zurich-servicenow-platform&section=t_SetMIDServerParameters&ft:locale=en-US) file with these parameters.

    This configuration cannot be done from the instance.

<table id="table_dwd_rh4_vs"><thead><tr><th>

Parameter

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ext.cred.safe\_folder

</td><td>

NameOfFolder

</td><td>

Folder to use for all credential lookups. For example, **root**.

</td></tr><tr><td>

ext.cred.use\_cyberark

</td><td>

true

</td><td>

Boolean parameter indicating that this MID Server is integrated with CyberArk.

</td></tr><tr><td>

ext.cred.ccp\_endpoint

</td><td>

CCPendpointURL

</td><td>

The CCP endpoint URL, which must use HTTPS. For example: `https:// /AIMWebService/api/Accounts`

</td></tr><tr><td>

ext.cred.cyberark.cert\_path

</td><td>

/path/on/mid/agent/security/EXAMPLE-cyberark-client.pfx

</td><td>

Path to the certificate file.

</td></tr><tr><td>

ext.cred.cyberark.cert\_password

</td><td>

example-password

</td><td>

Password for the certificate file.

</td></tr></tbody>
</table><table id="table_kqv_3nz_st"><thead><tr><th>

Parameter

</th><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ext.cred.timeout

</td><td>

30

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

</td></tr><tr><td>

ext.cred.verify\_ssl

</td><td>

true

</td><td>

The MID Server validates the CCP server certificate, verifying the server’s identity. This setting is recommended for production environments. If set to false, the MID Server does not validate the CCP server certificate.

</td></tr><tr><td>

ext.cred.check\_revocation

</td><td>

true

</td><td>

This parameter controls certificate revocation checking for the CCP server certificate chain. While true, enables CRL/OCSP checks.

</td></tr><tr><td>

ext.cred.snmpv2\_community\_property

</td><td>

AttributeName

</td><td>

SNMPv2 is not natively supported in CyberArk. If your organization has created custom SNMPv2 credentials in which the community string does not appear in the password field of the credential, use this property to map the attribute in the credential to the community string.

</td></tr></tbody>
</table>
**Parent Topic:**[CyberArk integration configuration](../concept/c_CyberArkIntegrationConfiguration.md)

