---
title: Attach a script file to a file synchronized MID Server
description: You can attach a script file to synchronize to a connected MID Server. Windows Internet Explorer enhanced security blocks downloaded files that it determines are potentially dangerous. However synchronizing the files avoids this security problem.Windows Internet Explorer enhanced security blocks downloaded files that it determines are potentially dangerous.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Attach a script file to a file synchronized MID Server

You can attach a script file to synchronize to a connected MID Server. Windows Internet Explorer enhanced security blocks downloaded files that it determines are potentially dangerous. However synchronizing the files avoids this security problem.

## Before you begin

Role required: **admin**

<table id="table_yfh_kv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## About this task

Enhanced security in Windows browsers, such as Internet Explorer, blocks downloaded files that it determines are potentially dangerous. This would block files downloaded for use by the MID Server. You would need to unblock each file manually through the browser.

To get around this issue, use file synchronization. File synchronization requires you to proactively take script files from your instance and save them on the MID Server. The files on the instance and the MID server stay synchronized, but there is no longer any need for the MID Server to download the whole file. File synchronization also protects any updates you make in those script files from being overwritten during the upgrade of an instance.

You can attach multiple files, but the last attached file gets synchronized to the MID Server. If you delete the attachment, the script file becomes inactive, and the synchronized file is deleted from the MID Server.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Script Files**.

2.  Open the file to which you would like to attach the script file, or click **New** to create a new file.

3.  Select **Use attachment**, and then click the paperclip icon to add the attachment.

    When **Use attachment** is checked, an attached script file overrides the script contained in the **Script** field. If this check box is cleared, the script in the **Script** field is used instead of the attachment.

    The script file attachment name must match the MID Server script file name, since the record can contain other attachments.

4.  Click **Update** to initiate the synchronization process.

    Ensure that the file name matches the script name. If you receive the error message: `File type not permitted or mime type does not match the file content`, request that your administrator turn off mime type validation on attachments. The system property **glide.security.file.mime\_type.validation** controls this setting.


**Parent Topic:**[Securing and encrypting MID Server data](../concept/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](../concept/mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](../concept/mid-authentication-soap-requests.md#)

[MID Server unified key store](../concept/mid-unified-keystore.md#)

[Enable MID Server mutual authentication](install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](mid-azure-key-vault-integration.md#)

[MID Server command audit log](../concept/mid-audit-log.md)

[Rekey a MID Server](t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[MID Server FIPS Enforced Mode](../concept/mid-fips-enforced.md#)

[MID Server Governance](../concept/mid-timeout.md)

## Enable script file synchronization for Windows enhanced security

Windows Internet Explorer enhanced security blocks downloaded files that it determines are potentially dangerous.

Script files synchronized with the MID Server are stored on the instance in the MID Server Script File `[ecc_agent_script_file]` table, which you can access in the **MID Server** &gt; **Script Files** module.

When the MID Server first connects to the instance, the instance creates a directory called `\scripts` in the MID Server root. The instance then creates a parent directory in the path `\scripts\<parent name>` using definitions from the ecc\_agent\_script\_file table. Finally, the instance creates the script files themselves inside the parent directory using the records from the ecc\_agent\_script\_file table.

The record for the parent directory looks like this:

![MID Server script file](../image/MIDServerScriptFileSync.png)

The instance creates each script file in the parent directory on the MID Server using the record Name from the ecc\_agent\_script\_file table as the file name and the Script field payload as the file contents. A script file record looks like this:

![script file example](../image/MIDServerScriptFileSync2.png)

The synchronization of the script file continues to work as if the script was manually added to the form.

See [Attach a script file to a file synchronized MID Server](mid-server-script-attach.md#) for instructions on how to attach a script file.

**Note:** The MID Server Script File \[ecc\_agent\_script\_file\] table is domain separated. You can create versions of these policies that only a MID Server from the same domain can use. For instructions, see [Set up domain separation for MID servers](../concept/c_MIDServerDomainSeparation.md#).

