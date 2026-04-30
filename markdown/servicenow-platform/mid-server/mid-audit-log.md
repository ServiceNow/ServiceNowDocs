---
title: MID Server command audit log
description: The command audit log records the commands run by the MID Server for the Discovery application. Review the commands to check for anomalies or errors.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server command audit log

The command audit log records the commands run by the MID Server for the Discovery application. Review the commands to check for anomalies or errors.

<table id="table_m2t_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>The MID Server command audit log is a record of the commands the MID Server runs during discovery. For example, executing one pattern may run many separate commands. The MID Server command audit log supports Powershell commands for WMI and WinRM. For SSH commands, the audit log supports SSNC but not J2SSH. In Quebec, the command audit log only supports recording the commands run during discovery.

## Enable the command audit log

The MID Server audit log is enabled with the MID Server property **mid.log.command\_audit.enable**, which is set to false by default. Add the property in the **MID Server Properties** table \[ecc\_agent\_property\_list.do\]. Once enabled, the MID Server command audit logs are accessed in the instance by navigating to **MID Server** &gt; **Command Audit Logs** \[ecc\_agent\_command\_audit\_log\_list.do\]. To see or change this table, the user must have the role **agent\_security\_admin**.

![Typical data in the MID Server command audit logs.](../image/mid-audit-logs.png)

## Data recorded in the command audit logs

The MID Server command audit log records the name of the command and the command hash. If, for example, during discovery a probe does not run a command but instead runs a script then the script name is recorded. The command hash is calculated based on the content of the script, regardless of the name. Therefore, changing the name does not affect the command hash.

When a probe, such as a WMIRunner, runs a command with multiple WMI fields then WMI creates one script to query those fields. The script is created temporarily on the MID Server host in the temp folder. After the script is run, it is removed from the temp folder. The script is given a name based on the fields and a random number. However, the hash key is always the same given the same contents.

The command audit log reports the execution status as either a success or failure. The record entry is a success if the command was run, or a failure if it was unable to run. The command audit log does not consider the result of the command being run. For example, a command which runs but fails gather data is still listed in the execution status as a success.

Discovery supports JEA profiles for WinRM. The MID Server command audit log records the JEA profile of the discovery command, if it is available. See [Microsoft Just Enough Administration \(JEA\) for Discovery](https://www.servicenow.com/docs/access?context=microsoft-jea-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more information on JEA profiles.

By default, the table is rotated every seven days. For more information, see [Table Rotation](https://www.servicenow.com/docs/access?context=c_TableRotation&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Securing and encrypting MID Server data](mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](mid-authentication-soap-requests.md#)

[MID Server unified key store](mid-unified-keystore.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](mid-fips-enforced.md#)

[MID Server Governance](mid-timeout.md)

