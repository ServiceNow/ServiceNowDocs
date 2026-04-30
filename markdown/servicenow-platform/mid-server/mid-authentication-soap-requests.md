---
title: MID Server authentication credentials and SOAP requests
description: Set basic authentication credentials to update the web service invocation data. For added security, you can enforce basic authentication on each incoming SOAP request to the MID Server.Enforce basic authentication on each incoming SOAP request to the MID Server.
locale: en-US
release: xanadu
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server authentication credentials and SOAP requests

Set basic authentication credentials to update the web service invocation data. For added security, you can enforce basic authentication on each incoming SOAP request to the MID Server.

<table id="table_ahc_jv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## Basic authentication credentials and SOAP requests

You can enforce basic authentication on each request. The MID Server is not able to communicate through a proxy server if the proxy server supports only NTLM authentication. You can use basic authentication with a proxy server or create an exception for the MID server host.

Supplying basic authentication information, regardless of whether it is required, has an added advantage. The web service invocation creates or updates data using the supplied credentials. For example, when you create an incident record, the journal fields have the user id of the basic authenticated user instead of the default Guest user. This behavior allows you to identify data added by a specific MID Server.

You can set basic authentication credentials for SOAP requests. Each SOAP request contains an Authorization header as specified in the [Basic Authentication protocol](http://www.w3.org/Protocols/HTTP/1.0/draft-ietf-http-spec.html#BasicAA).

The setting for enforcing strict security controls how the instance uses the credentials you provide for the MID Server. When the setting is enabled, you must provide a user ID with access to the tables the MID Server is trying to access. When the setting is disabled, any valid user ID allows the MID Server to access to all tables.

**Parent Topic:**[Securing and encrypting MID Server data](mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server unified key store](mid-unified-keystore.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[MID Server command audit log](mid-audit-log.md)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](mid-fips-enforced.md#)

[MID Server Governance](mid-timeout.md)

## Require basic authorization for incoming SOAP requests

Enforce basic authentication on each incoming SOAP request to the MID Server.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Web Services**.

2.  Select the check box for **Require basic authorization for incoming SOAP requests**.

3.  Click **Save**.

4.  To provide basic authentication credentials for a MID Server, navigate to C:\\Program Files\\ServiceNow\\&lt;MID Server name&gt;\\agent and edit the `config.xml` file, as follows:

    1.  Find the element **&lt;parameter name="mid.instance.username" value=""/&gt;** and enter the instance administrator user name as the value.

        For example, you might enter **&lt;parameter name="mid.instance.username" value="admin"/&gt;.**

    2.  Find the element **&lt;parameter name="mid.instance.password" value=""/&gt;** and enter the configured password for this instance as the value.

        For example, you might enter **&lt;parameter name="mid.instance.password" value="abc123"/&gt;.**


