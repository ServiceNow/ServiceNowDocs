---
title: MID Server command audit log
description: The command audit log records the commands run by the MID Server for the Discovery application. Review the commands to verify there are no anomalies or errors.Enable the MID Server command audit log by setting the mid.log.command\_audit.enable property to true.The MID Server command audit log records the command name, command hash, execution status, and JEA profile for each command it runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-audit-log.html
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-10-16"
reading_time_minutes: 8
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server command audit log

The command audit log records the commands run by the MID Server for the Discovery application. Review the commands to verify there are no anomalies or errors.

<table id="table_m2t_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>The MID Server command audit log is a record of the commands the MID Server runs during discovery. Executing one pattern may run many separate commands. The MID Server command audit log supports Powershell commands for WMI and WinRM. For SSH commands, the audit log supports SSNC but not J2SSH. In Quebec, the command audit log only supports recording the commands run during discovery.

**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[Encrypt or decrypt MID Server configuration file values]()

[MID Server configuration file security]()

[MID Server authentication methods comparison]()

[MID Server authentication credentials and SOAP requests]()

[MID Server unified key store]()

[Enable MID Server mutual authentication]()

[MID Server Azure Key Vault integration]()

[Rekey a MID Server]()

[Add SSL certificates for the MID Server]()

[MID Server SSH cryptographic algorithms]()

[Attach a script file to a file synchronized MID Server]()

[MID Server FIPS Enforced Mode]()

[MID Server Governance]()

[MID Server IPKI authentication]()

## Enable the command audit log

Enable the MID Server command audit log by setting the **mid.log.command\_audit.enable** property to **true**.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  Select **New**.

3.  In the **Name** field, enter `mid.log.command_audit.enable`.

    In the **Value** field, enter `true`.

4.  Select **Submit**.

5.  Restart the MID Server to apply the property.


### What to do next

To access the MID Server command audit logs, navigate to **All** &gt; **MID Server** &gt; **Audit Logs** &gt; **Command Audit Logs** \[ecc\_agent\_command\_audit\_log\_list.do\]. To view or change this table, the user must have the role agent\_security\_admin.

## Command audit logs data

The MID Server command audit log records the command name, command hash, execution status, and JEA profile for each command it runs.

If during discovery a probe does not run a command but instead runs a script then the script name is recorded. The command hash is calculated based on the content of the script, regardless of the name. Therefore, changing the name does not affect the command hash.

The following screenshot shows the MID Server **Command Audit Logs** screen.

\[Omitted image "mid-audit-logs.png"\] Alt text: Typical data in the MID Server command audit logs.

When a probe, such as a WMIRunner, runs a command with multiple WMI fields, WMI creates one script to query those fields. WMI creates the script temporarily on the MID Server host in the `temp` folder. After WMI runs the script, it removes the script from the `temp` folder. The script is given a name based on the fields and a random number. However, the hash key is always the same given the same contents.

The command audit log reports the execution status as either a success or failure. The record entry is a success if the command ran, or a failure if it could not run. The command audit log does not consider the result of the command being run. For example, a command which runs but fails to gather data is still listed in the execution status as a success.

Discovery supports JEA profiles for WinRM. The MID Server command audit log records the JEA profile of the discovery command, if it is available. See [Microsoft Just Enough Administration \(JEA\) for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/microsoft-jea-discovery.md) for more information on JEA profiles.

By default, the table is rotated every seven days. See [Table Rotation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_TableRotation.md).

