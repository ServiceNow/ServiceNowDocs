---
title: Encrypt or decrypt MID Server configuration file values
description: The value of any MID Server parameter in the config.xml file can be encrypted. The attributes for all encrypted values are managed from within the configuration file, including the security attribute of the login password.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/mid-server-manual-encryption.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Encrypt or decrypt MID Server configuration file values

The value of any MID Server parameter in the `config.xml` file can be encrypted. The attributes for all encrypted values are managed from within the configuration file, including the security attribute of the login password.

## Before you begin

Role required: admin

<table id="table_m2t_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## Procedure

1.  Navigate to the `agent` directory that was created when the MID Server was installed and open the `config.xml` file using a text editor such as WordPad.

2.  Locate or add the parameter you want to encrypt.

    For example, you might want to protect your proxy server passwords by configuring this parameter:

    ```
    <parameter name="mid.proxy.password" value="securepassw0rd"/>
    ```

3.  Add the encryption attribute **secure="true"**.

    ```
    <parameter name="mid.proxy.password" secure="true" value="securepassw0rd"/>
    ```

4.  Restart the MID Server.

5.  Open the `config.xml` file.

    The encrypted password appears as follows:

    ```
    <parameter name="mid.proxy.password" secure="true" value="encrypted:rhrfUNYRzZAI8/BkTtZmNA=="/>
    ```

    .

6.  To decrypt this or any other value in the `config.xml` file and display the value in clear text:

    1.  Stop the MID Server.

    2.  Set the **secure="true"** attribute to **false**.

    3.  Replace the encrypted value with the clear text value.

    4.  Restart the MID Server.


**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[MID Server configuration file security]()

[MID Server authentication credentials and SOAP requests]()

[MID Server unified key store]()

[Enable MID Server mutual authentication]()

[MID Server Azure Key Vault integration]()

[MID Server command audit log]()

[Rekey a MID Server]()

[Add SSL certificates for the MID Server]()

[Specify an external TrustStore for the MID Server]()

[MID Server SSH cryptographic algorithms]()

[Attach a script file to a file synchronized MID Server]()

[MID Server FIPS Enforced Mode]()

[MID Server Governance]()

