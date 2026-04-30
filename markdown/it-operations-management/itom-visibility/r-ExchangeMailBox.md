---
title: Exchange MailBox discovery
description: Discovery creates or updates a CMDB record when it detects a running instance of Exchange Mailbox.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Software discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Exchange MailBox discovery

Discovery creates or updates a CMDB record when it detects a running instance of Exchange Mailbox.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Prerequisites

The `Microsoft.Exchange.Management.PowerShell` module must be installed on the server that you want to discover.

The service `winRM` must be running on the host machine. Run the following command in the Powershell window to verify: `New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "http://$hostname/PowerShell/" -Authentication Kerberos`

## Pattern

By default, Discovery uses the **MailBox On Windows** pattern to discover Exchange MailBox.

## Credentials

Configure these credentials:

<table id="table_gmd_2kx_jz"><thead><tr><th>

Credential type

</th><th>

Additional notes

</th></tr></thead><tbody><tr><td>

[Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The user must be able to run Powershell commands against the Exchange hosts. Use **Exchange Mailbox** as the CI type for the applicative credential.

**Important:** Do not use the **Exchange Mailbox server** CI type.

</td></tr><tr><td>

[Windows credentials](https://www.servicenow.com/docs/access?context=r_WindowsCredentialsForm&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)

</td><td>

The OS user must be a domain user, not a local user for the server.

</td></tr></tbody>
</table>## Data collected

The following data is collected on the Exchange Mailboxes \[cmdb\_ci\_exchange\_mailbox\] table:

|Label|Field Name|
|-----|----------|
|Name|name|
|Version|version|
|Class|sys\_class\_name|
|Fully qualified domain name|fqdn|
|IP Address|ip\_address|
|Installation directory|install\_directory|
|Type|type|

**Parent Topic:**[Software discovery](../concept/c_Software.md)

