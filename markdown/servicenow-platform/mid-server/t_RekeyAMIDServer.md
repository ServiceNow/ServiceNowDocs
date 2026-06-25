---
title: Rekey a MID Server
description: Rekey a MID Server to generate a new private key. Private keys are used to decrypt automation credentials, so that MID Servers can transmit information securely. Key pairs are initially generated when a MID Server is validated, and MID Servers should be rekeyed periodically to meet security requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t\_RekeyAMIDServer.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Rekey a MID Server

Rekey a MID Server to generate a new private key. Private keys are used to decrypt automation credentials, so that MID Servers can transmit information securely. Key pairs are initially generated when a MID Server is validated, and MID Servers should be rekeyed periodically to meet security requirements.

## Before you begin

Role required: admin

<table id="table_imd_hv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## About this task

When the MID Server comes back online, the system automatically validates the new key, and the MID Server resumes processing automation tasks.

Automation credentials are secured by encrypting them in the instance with the MID Server’s trusted public key prior to transmission. When the MID Server is created, it generates a keypair, consisting of a public and private key. After the MID Server is validated, it can use the private key to decrypt automation credentials. You should occasionally rekey the MID Server to meet your organizations security requirements.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Servers**.

2.  Open the MID Server whose keypairs you want to rotate.

3.  Under **Related Links**, click **Rekey**.


**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[Encrypt or decrypt MID Server configuration file values]()

[MID Server configuration file security]()

[MID Server authentication credentials and SOAP requests]()

[MID Server unified key store]()

[Enable MID Server mutual authentication]()

[MID Server Azure Key Vault integration]()

[MID Server command audit log]()

[Add SSL certificates for the MID Server]()

[Specify an external TrustStore for the MID Server]()

[MID Server SSH cryptographic algorithms]()

[Attach a script file to a file synchronized MID Server]()

[MID Server FIPS Enforced Mode]()

[MID Server Governance]()

[Validate the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateAMIDServer.md)

