---
title: Introduction to credentials, connections, and aliases for Orchestration
description: All application integrations in Orchestration require connection information, credentials, and connection and credential aliases to their respective applications to access resources.Define an alias to label a credential or connection record.Orchestration requires credentials to access resources.Use the connections table to setup a JMS, JDBC, or HTTP\(s\) connection to a target host.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 9
breadcrumb: [Orchestration activity designer, Classic Orchestration, Data and Automation]
---

# Introduction to credentials, connections, and aliases for Orchestration

All application integrations in Orchestration require connection information, credentials, and connection and credential aliases to their respective applications to access resources.

Before you can execute an application integration in Orchestration, you must create and configure the corresponding connection information and credentials. The Connections pertains to an integration with a system, such as an IP address or endpoint with protocols. It contains specific details, such as database particulars, when integrating with a database. The associated Credentials are the authentication data required to make the connection.

Connection information and credentials can vary between QA/Development/Production environments for the same integration. The tight coupling between this data and application metadata, such as workflow or job scheduling, make application metadata obsolete when you change environments. To alleviate this problem, the concept of an alias is introduced, for connections and credentials, to decouple this data from application metadata. These aliases allow customers to design their application metadata to couple to an alias, which during runtime resolves to connection and credential data.

There are two types of aliases, a connection and credential alias and a credential alias. There are business rules that enforce certain constraints on these aliases. Names should contain alphabets, numbers, and underscores but cannot have special characters. The alias must be unique in a scope. If you choose to have multiple active connections, you can have more than one active connection in the same domain. If you do not choose this option, you can have only one active connection in per domain.

**Note:** If you enable multiple active connections, when the connection records resolve, your application picks one connection based on an established order. The order of the connections depends on the API you use to retrieve connection data.

You can add additional connection attributes to an alias, which are available in connection data during run time. Variables overridden by connection administration during run time should not affect the alias.

The credential alias resolves only credential data. Along with alias data model, you can use a scriptable API which can get connection and credential data during runtime.

**Parent Topic:**[Orchestration activity designer](c_WorkflowActivityDesigner.md)

## Using Connection and Credential Alias with Orchestration

Define an alias to label a credential or connection record.

The Credential and Connection Alias defines an alias that labels a credential or connection record. It is extended from the sys\_metadata table. It requires the admin role. The credential\_admin and connection\_admin have read access to sys\_alias. A connection alias contains:

-   **Name**

    Name of the alias.

-   **ID**

    This field is based on the format "scope name.alias name" Unique index on ID to ensure unique record based on scope name + name. If the scope is global, the ID is the alias name.

-   **Type**

    You can select either 'Credential' or 'Connection and Credential'. The default is Connection and Credential.

-   **Connection type**

    This field is applicable when the alias type is set to Connection and Credential. There are three connection types: HTTP, JDBC, JMS. The default is HTTP.


If you create a workday alias in global scope, the ID is set to workday

If you create a workday alias in hr app scope, the ID is set to x\_hr\_app.workday

-   Name can only contain alphabets, numbers and underscore.
-   During the upgrade, the tag in credential record will be migrated to connection alias. If the tag in previous release’s credential record contains special characters other than alphabets, numbers and underscore, the tag data will be preserved during the upgrade. The user still can use these connection alias, but the user cannot update these alias, unless he removes these special characters when do the update.

## Using credentials with Orchestration

Orchestration requires credentials to access resources.

### Credential table

The credential table \(discovery\_credential\) defines credentials that can be used for integration. In the previous release, the Credential table contains a string-type tag field, which labels a credential and the tag is used in Orchestration activities. In the Madrid release, the credential alias is renamed from tag, and the type is changed from string to GlideList, which is a reference to the connection alias table.

### Credential types

The following credential types are provided:

<table id="table_whp_qp5_5y"><thead><tr><th>

Credential type

</th><th>

Description

</th><th>

Supports Test Credential option

</th></tr></thead><tbody><tr><td>

[Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The credentials to explore the applications on a device or computer. [Discovery patterns used by ITOM Visibility](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) often need applicative credentials.

</td><td>

No

</td></tr><tr><td>

[Amazon Web Service credentials](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The Amazon Web Services \(AWS\) main account, access key ID, and secret access key.**Note:** You cannot test AWS credentials through the Test

</td><td>

No

</td></tr><tr><td>

[Azure Service Principal and Enterprise Agreement credentials](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The Azure service principals required for an Azure subscription.

</td><td>

No

</td></tr><tr><td>

[Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

A user name and password.

</td><td>

No

</td></tr><tr><td>

[CIM credentials](https://www.servicenow.com/docs/access?context=r_CIMCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The user name and password required to access a CIMOM - Common Information Model Object Manager \(CIM\) server, which obtains information about VMware ESX servers.

</td><td>

No

</td></tr><tr><td>

[Cloud credentials](https://www.servicenow.com/docs/access?context=r_CloudManagementCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

Credentials that Orchestration uses to access cloud resources.

</td><td>

No

</td></tr><tr><td>

[JDBC credentials](https://www.servicenow.com/docs/access?context=r_JDBCCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

A user name and password to access a Java Database Connectivity \(JDBC\) connection.

</td><td>

Yes

</td></tr><tr><td>

[JMS credentials](https://www.servicenow.com/docs/access?context=r_JMSCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

A user name and password to access to a Java Message Service \(JMS\).

</td><td>

Yes

</td></tr><tr><td>

[OAuth 2.0 credentials](https://www.servicenow.com/docs/access?context=oauth-2-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

OAuth 2.0 credentials enable ServiceNow® to obtain access to user accounts on an HTTP service.

</td><td>

 

</td></tr><tr><td>

[SNMP community credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=yokohama&pubname=yokohama-platform-security&section=r_SNMPCommunityCredentialsForm&ft:locale=en-US)

</td><td>

The community string to access devices via SNMP.

</td><td>

Yes

</td></tr><tr id="row_yc2_zp5_5y"><td>

[SNMPv3 credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=yokohama&pubname=yokohama-platform-security&section=r_SNMPCredentialsForm&ft:locale=en-US)

</td><td>

The user name and keys required to access devices on your SNMP v3 network.

</td><td>

Yes

</td></tr><tr><td>

[SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The user name and password to access Linux and UNIX devices.

</td><td>

Yes

</td></tr><tr><td>

[SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The private key credentials to access Linux and UNIX devices. **Note:** For better security, SSH private key credentials are suggested over SSH password credentials.

</td><td>

Yes

</td></tr><tr><td>

[VMware credentials](https://www.servicenow.com/docs/access?context=r_VMwareCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

Credentials to access vCenter resources. These credentials are required for any work that is performed on vCenter, such as cloning a virtual machine.

</td><td>

Yes

</td></tr><tr><td>

[Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The user name and password required to access Windows computers. Several [Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) must be met to use Windows credentials.

</td><td>

Yes

</td></tr></tbody>
</table>### How MID Servers use credentials

By default, Windows MID Servers use the login credentials of the MID Server service on the host machine to discover Windows devices in the network. You should [Configure Windows MID Server service credentials](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=yokohama&pubname=yokohama-servicenow-platform&section=t_ConfigMIDSvrSvcCredentials&ft:locale=en-US) so that they have domain or local administrator privileges. For Linux and UNIX machines and network devices, the MID Server uses the SSH and SNMP credentials configured in the instance in **Discovery** &gt; **Credentials**.

MID Servers that Orchestration uses must have access to the necessary credentials to execute commands on computers in the network as specified by the [Workflow activities](https://www.servicenow.com/docs/access?context=c_WorkflowActivities&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US). Orchestration can use the same SSH and SNMP credentials as Discovery, but has two additional credentials designed for specific workflow activities: Windows \(for [PowerShell](https://www.servicenow.com/docs/access?context=c_OrchestrPowerShellActivities&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)\) and VMware.

### Encryption and decryption

The platform stores credentials in an encrypted field on the Credentials \[discovery\_credentials\] table. Once they are entered, they cannot be viewed.

When credentials are requested by the MID Server, the platform decrypts the credentials using the following process:

1.  The credentials are decrypted on the instance with the password2 fixed key.
2.  The credentials are re-encrypted on the instance with the MID Server's public key.
3.  The credentials are encrypted on the load balancer with SSL.
4.  The credentials are decrypted on the MID Server with SSL.
5.  The credentials are decrypted on the MID Server with the MID Server's private key.

**Note:** The platform does not have separate encryption keys for multi-tenant instances.

### Credential order

Credentials can be assigned an order value in the [Credentials form](https://www.servicenow.com/docs/access?context=t_CreateCredential&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US), which forces the application to try all the credentials at their disposal in a certain sequence. If you do not specify an order value, the application tries the credentials in the Credentials \[discovery\_credential\] table randomly, until it finds one that works, such as when Orchestration attempts to run a command on an SSH server \(such as a Linux or UNIX machine\), or when Discovery attempts to query an SNMP device \(such as a printer, router, or UPS\).

After identifying the credentials for a device, Discovery and Orchestration create an affinity between the credentials and the device using the Credential Affinity `[dscy_credentials_affinity]` table. All subsequent discoveries or Orchestration activities attempt to match the credentials in this table with a device for which an affinity exists. If credentials for a device change, Discovery and Orchestration try all available credentials again until they create a new affinity.

**Note:** If Orchestration and Discovery are installed, and credential alias is enabled, multiple affinities can exist. In this case, the platform looks up credentials for each affinity and inserts the credential for the affinity with the lowest order into the probe.

Ordering credentials is useful in the following situations:

-   The credentials table contains many credentials, with some used more frequently than others. For example, if the table contains 150 SSH credentials, and 5 of those are used to log in to 90% of the devices, it is good practice to configure those five with low-order numbers, which places them at the top of the execution list. Discovery and Orchestration will work faster if they try these common credentials first. After the first successful connection, the system knows which credentials to use the next time for each device.
-   The system has aggressive login security. For example, if the Solaris database servers in the network only allow three failed login attempts before they lock out the MID Server, configure the database credentials with a low-order value.

### Credential alias

Credential alias enables flow and workflow creators to:

-   Assign individual credentials to any activity in an Orchestration workflow.
-   Assign individual credentials to any action in Workflow Studio.
-   Assign different credentials to each occurrence of the same activity type in an Orchestration workflow.
-   Assign different credentials to each occurrence of the same action in designer flow.

Credential alias also works with credential affinities.

### External credential stores

If you do not want credentials stored in your instance, you can use external credential repositories. External credential stores save the credentials in an external site that your instance can access. Only [CyberArk](https://www.cyberark.com/) is supported.

## Connections with Orchestration

Use the connections table to setup a JMS, JDBC, or HTTP\(s\) connection to a target host.

### Connection Table

The Connection table \(sys\_connection\) is the base table for all connection tables. You can setup connections for the following protocols:

-   JDBC
-   JMS
-   HTTP\(s\)

The connection table references the connection alias table, which couples the connection alias to connection information. Every connection records the following information:

|Field|Description|
|-----|-----------|
|Name|Name of the connection. This field must be unique on the table.|
|Credential|Specify the credential to use with this connection. This is optional.|
|Connection alias|The connection alias resolves your connection and credentials at run time. Only one connection is active per Connection alias at any one time.|
|Active|Check to make the current connection active.|
|Domain|Domain to which the connection belongs.|

Credential is unique across active connections, if not empty.

### Upgrading connection information

The JDBC connection \(jdbc\_connection\) and JMS connection \(orch\_jms\_ds\) tables are existing Orchestration connection tables. In madrid, we re-parent them to extend from Connection \(sys\_connection\) table. They move from Orchestration run time plugins to Credentials &amp; Connections plugins. They are originally extended from sys\_metadata. The sys\_metadata related data will be removed. JDBC field name changes:

-   JDBC server is renamed to host
-   Database port is renamed to port

