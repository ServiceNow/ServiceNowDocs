---
title: Get started with credentials
description: The MID Server uses the credentials you create in the Credentials \[discovery\_credentials\] table to access resources for Discovery, Orchestration, Service Mapping, and Cloud Management.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Connections and Credentials, Access Management]
---

# Get started with credentials

The MID Server uses the credentials you create in the Credentials \[discovery\_credentials\] table to access resources for Discovery, Orchestration, Service Mapping, and Cloud Management.

## How MID Servers use credentials

By default, Windows MID Servers use the login credentials of the MID Server service on the host machine to discover Windows devices in the network. You should [Configure Windows MID Server service credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md) so that they have at least local administrator privileges. For Linux and UNIX machines and network devices, the MID Server uses the SSH and SNMP credentials configured in the instance in **Discovery** &gt; **Credentials**.

MID Servers that Orchestration uses must have access to the necessary credentials to execute commands on computers in the network, as specified by the [Workflow activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-activities/c_WorkflowActivities.md). Orchestration can use the same SSH and SNMP credentials as Discovery, but has two additional credentials designed for specific Workflow activities: Windows \(for [PowerShell activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchestrPowerShellActivities.md)\) and VMware.

## Encryption and decryption

The platform stores credentials in an encrypted field on the Credentials \[discovery\_credentials\] table. Once they are entered, they cannot be viewed.

When the MID Server requests credentials, the ServiceNow AI Platform decrypts the credentials using the following process:

1.  The credentials are decrypted on the instance with the password2 fixed key.
2.  The credentials are re-encrypted on the instance with the MID Server's public key.
3.  The credentials are encrypted on the load balancer with SSL.
4.  The credentials are decrypted on the MID Server with SSL.
5.  The credentials are decrypted on the MID Server with the MID Server's private key.

**Note:** The platform does not have separate encryption keys for multi-tenant instances.

## Credential order

Credentials can be assigned an order value in the [Credentials Form](r_WindowsCredentialsForm.md#), which forces the application to try all the credentials at their disposal in a certain sequence. If you do not specify an order value, the application tries the credentials in the Credentials \[discovery\_credential\] table randomly, until it finds one that works. For example, when:

-   Orchestration attempts to run a command on an SSH server, such as a Linux or a UNIX machine.
-   Discovery attempts to query an SNMP device, such as a printer, router, or UPS.

After identifying the credentials for a device, Discovery and Orchestration create an affinity between the credentials and the device using the Credential Affinity `[dscy_credentials_affinity]` table. All subsequent discoveries or Orchestration activities attempt to match the credentials in this table with a device for which an affinity exists. If credentials for a device change, Discovery and Orchestration try all available credentials again until they create a new affinity.

**Note:** If Orchestration and Discovery are installed, and credential alias is enabled, multiple affinities can exist. In this case, the platform looks up credentials for each affinity and inserts the credential for the affinity with the lowest order into the probe.

Ordering credentials is useful in the following situations:

-   The credentials table contains many credentials, with some used more frequently than others. For example, the table contains 150 SSH credentials, and five of those credentials are used to log in to 90% of the devices. It is good practice to configure those five credentials with low-order numbers, which place them at the top of the execution list. Discovery and Orchestration work faster when they try these common credentials first. After the first successful connection, the ServiceNow AI Platform knows which credentials to use the next time for each device.
-   The ServiceNow AI Platform has aggressive login security. For example, configure database credentials with a low-order value if Solaris database servers in the network only provide three failed login attempts before locking out the MID Server.

## Credential aliases

Credential aliases are available for [Discovery](../concept/discovery-credential-alias.md#) and [Orchestration](../concept/c_AssignCredsOrchActivities.md).

Aliases for Discovery enable an administrator to:

-   Employ a credential filtering behavior with configurable levels of compliance.
-   Assign multiple credential aliases to a Discovery schedule.
-   Prevent the creation of credential affinities that use inappropriate or sensitive credentials. To learn more, see [credential affinities](../concept/c_CredentialAffinity.md).

Aliases for Orchestration enable workflow creators to:

-   Assign individual credentials to any activity in an Orchestration workflow
-   Assign individual credentials to any action in Flow Designer
-   Assign different credentials to each occurrence of the same activity type in an Orchestration workflow.
-   Assign different credentials to each occurrence of the same action in designer flow.

## External credential stores

If you do not want credentials stored in your instance, you can use external credential repositories. External credential stores save the credentials in an external site that your instance can access. [CyberArk](../concept/c_CyberArkCredStorageIntegrate.md) is the only supported external credential store. However, other external stores can be configured using the ServiceNow API.

