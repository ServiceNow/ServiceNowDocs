---
title: SNMP credentials
description: Discovery explores many kinds of devices \(switches, routers, printers, and so on\) using the SNMP protocol. Credentials for SNMP don’t include a user name, just a password, called the community string.The SNMP Community credential type manages access to discover many kinds of devices \(switches, routers, printers, etc.\) using the SNMP protocol. This credential type is available for Discovery, Service Mapping, and Orchestration.SNMPv3 credentials accept a privacy protocol and an additional privacy key and are available for Discovery and Orchestration. For external storage in CyberArk, you can select a privacy account key.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Create and test your credentials, Get started with credentials, Connections and Credentials, Access Management]
---

# SNMP credentials

Discovery explores many kinds of devices \(switches, routers, printers, and so on\) using the SNMP protocol. Credentials for SNMP don’t include a user name, just a password, called the *community string*.

The default read-only community string for many SNMP devices is public, and Discovery will try that automatically. Enter the appropriate SNMP credentials if they differ from the *public* community string.

Discovering SNMP uses all community strings that are configured. This behavior does not apply to discovering SNMPv3.

The default Orchestration activity SNMP Query returns the object identifier \(OID\) of a device and requires SNMP credentials.

## SNMP community credentials

The SNMP Community credential type manages access to discover many kinds of devices \(switches, routers, printers, etc.\) using the SNMP protocol. This credential type is available for Discovery, Service Mapping, and Orchestration.

Credentials for SNMP do not include a user name, just a password \(the community string\). The default read-only community string for many SNMP devices is public, and the system will try that automatically. Enter the appropriate SNMP credentials if they differ from the public community string.

These fields are available in the Credentials form for SNMP community.

<table id="table_avj_ljv_2y"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique and descriptive name for this credential.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

User name

</td><td>

Enter the user name to create in the Credentials table. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name. For CIM discovery, the user must have the admin role.

</td></tr><tr><td>

Password

</td><td>

Enter the password.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential system. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.To use the credential for discovering CIs not belonging to this CI type using Service Mapping and Discovery patterns, enter the table name for the CI type to which the CI belongs, for example cmdb\_ci\_apache\_web\_server.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When you select this option the **User name** and **Password** fields are replaced with the **Credential ID** field. [External credential storage](c_ExternalCredentialStorage.md) is only available when the External Credential Storage plugin in activated. **Note:** Currently, the only supported external storage system is [CyberArk](c_CyberArkCredStorageIntegrate.md).

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.**Note:** Selecting Specific **Specific MID servers** doesn’t affect mid server selection. It’s used only to decide which mid servers should have visibility to the credential. **Specific MID servers** isn’t supported in Orchestration activities.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

Windows MID Server Service Account

</td><td>

When active, the defined credential represents the MID Server service account.

</td></tr></tbody>
</table>## SNMPv3 credentials

SNMPv3 credentials accept a privacy protocol and an additional privacy key and are available for Discovery and Orchestration. For external storage in CyberArk, you can select a privacy account key.

These fields are available in the Credentials form for SNMPv3.

<table id="table_a35_tc1_djb"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique and descriptive name for this credential. For example, you might call it **SNMP Community Atlanta**.

</td></tr><tr><td>

Active

</td><td>

Enable or disable these credentials for use.

</td></tr><tr><td>

Applies to

</td><td>

Select whether to apply these credentials to **All MID servers** in your network, or to one or more **Specific MID servers**. Specify the MID Servers that should use these credentials in the **MID servers** field.

</td></tr><tr><td>

MID servers

</td><td>

Select one or more MID Servers from the list of available MID Servers. The credentials configured in this record are available to the MID Servers in this list. This field is available only when you select **Specific MID servers** from the **Applies to** field.

</td></tr><tr><td>

Order

</td><td>

Order \(sequence\) in which Discovery tries this credential as it attempts to log on to devices. The smaller the number, the higher in the list this credential appears. Establish credential order when using large numbers of credentials or when security locks out users after three failed login attempts. If all the credentials have the same order number \(or none\), the instance tries the credentials in a random order.

</td></tr><tr><td>

User name

</td><td>

Enter the SNMP user name. Avoid leading or trailing spaces in user names. A warning appears if the platform detects leading or trailing spaces in the user name.

</td></tr><tr><td>

Authentication protocol

</td><td>

Select the authentication type to use for this credential. The choices are: -   MD5
-   SHA-1
-   SHA-224
-   SHA-256
-   SHA-384
-   SHA-512

</td></tr><tr><td>

Authentication Key

</td><td>

Enter the authentication key to use for this credential.

</td></tr><tr><td>

Privacy protocol

</td><td>

Select the encryption protocol for this credential. The choices are:-   3DES
-   AES128
-   AES192
-   AES256
-   DES

</td></tr><tr><td>

Privacy key

</td><td>

Enter the key associated with the selected privacy protocol.

</td></tr><tr><td>

Credential ID

</td><td>

Enter the unique key configured for external credentials in the JAR file uploaded to the MID Server for an external credential provider. The **Credential ID** field has a limit of 40 characters.This field is only visible when the **External credential store** check box is selected.

</td></tr><tr><td>

Privacy Credential ID

</td><td>

Enter the privacy account key configured for SNMPv3 credentials in CyberArk. If you are using a privacy protocol in CyberArk, this field must have the same value as the **Name** field for the CyberArk SNMPv3 Privacy Account. This field is only visible for SNMPv3 when you select **CyberArk** from the **Credential Store Type** field. If you are not using a privacy key for CyberArk, leave this field empty.

</td></tr><tr><td>

Credential alias

</td><td>

Allow workflow creators to assign individual credentials to any activity in an Orchestration workflow or assign different credentials to each occurrence of the same activity type in an Orchestration workflow.

</td></tr><tr><td>

External credential store

</td><td>

Select this check box to use an external credential storage system. When external storage is enabled, the **Credential ID** field appears. External credential storage is only available when the [External Credential Storage plugin](../task/t_ActivateExtrnlCredStoragePlugIn.md) is activated and the **External Storage** view is selected.

</td></tr><tr><td>

Credential Store Type

</td><td>

Select the external storage provider. Select **CyberArk** only if you are using a CyberArk SNMPv3 privacy key. The **Privacy Credential ID** field appears to allow entry of the key.

</td></tr><tr><td>

Use Context

</td><td>

Select this check box to add a context value for this credential. This field is visible in the **Discovery** view. Contexts are not currently supported for external credential storage.**Note:** A context is a collection of management information accessed by an SNMPv3 credential that references a specific OID. Contexts are sometimes referenced to collect information about the device that cannot be accessed by the normal credential. A context can be provided by the manufacturer or configured separately. If you have multiple SNMPv3 credentials with the same user name and keys, but some of your devices need a context and some do not, then you will need to create separate records for each device.

</td></tr><tr><td>

Context Name

</td><td>

Enter the context name value for this credential. This should only be used if you have devices that require this value for full access. This field is visible when the **Use Context** check box is selected.

</td></tr></tbody>
</table>