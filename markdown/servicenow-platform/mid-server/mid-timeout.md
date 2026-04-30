---
title: MID Server Governance
description: Improve MID Server security by setting an automatic timeout to invalidate and shut down inactive MID Servers. You can enable this feature and set the inactivity timeout period globally and for each MID Server.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server Governance

Improve MID Server security by setting an automatic timeout to invalidate and shut down inactive MID Servers. You can enable this feature and set the inactivity timeout period globally and for each MID Server.

<table id="table_yfh_kv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## Overview of MID Server Governance

MID Server Governance prevents forgotten MID Servers connected to ServiceNow instances from being utilized if the instance is compromised. ​MID Server Governance keeps a record of the last status change of the MID Server validation/invalidation process.

This feature is not enabled by default, and is available out-of-the-box as part of the MID Server plugin. Once enabled, MID Server authentication is expired after a predetermined period of inactivity unless explicitly configured to never expire.

## Enable and Configure MID Server Governance

MID Server Governance is enabled for all MID Servers by setting the following true/false system property:​ **mid.inactivity.timeout.enabled**. This property is not defined by default. The global inactivity timeout is ​specified by setting the following integer system property: **mid.inactivity.timeout.days**. The property takes an integer which specifies the timeout in days. The default timeout is 30 days if unspecified.

You can override the timeout for a particular MID Server by specifying **mid.inactivity.timeout.days** as a configuration parameter on that MID Server. A timeout value of 0 disables MID Server Governance on that MID Server. Therefore, you can set a global timeout and also change or disable timeouts for certain MID Servers.

You do not need to restart the MID Server after changing the Governance configuration. Governance works with either basic or mutual authentication.

## Activity Tracking

The MID Server analyzes activity by tracking incoming and outgoing ECC queue messages​. Once per hour, the MID Server reports the last activity to instance, which is stored in the ecc\_agent record​​, and checks if the inactivity timeout has been reached. If the inactivity timeout has been reached and the MID Server is up, the MID Server is invalidated and shuts down. If the timeout is reached when the MID Server is down, a job on the instance determines if the MID Server is idle and invalidates it on the instance.

When MID server is approaching auto-invalidation timeout due to inactivity, the MID Server page will display a message indicating:​

-   An info message when 3-7 days remain before inactivity timeout.

-   An error message when less than 3 days remain before inactivity timeout.

-   After a MID has been auto-invalidated, an error message is displayed indicating the date the MID was auto-invalidated​.


## Clearing the auto-invalidated state

After a MID Server has been auto-invalidated, the auto-invalidated status must be manually cleared in order to bring the MID back up successfully​. The MID Server shuts down immediately if it is restarted without clearing this state. In addition, a MID issue will be logged indicating this occurrence.

The auto-invalidated state of a MID Server can be cleared by selecting the **Clear auto invalidated** UI action from the MID Server instance page​. After invoking this UI action, the user should start their MID Server and continue with the usual validation process.

## Purpose field

The purpose is a text field that the customer can update at any point to indicate the intended usage for the MID Server. This field is purely descriptive and has no further interactions.

**Parent Topic:**[Securing and encrypting MID Server data](mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies](mid-security-checks.md)

[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](mid-authentication-soap-requests.md#)

[MID Server unified key store](mid-unified-keystore.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[MID Server command audit log](mid-audit-log.md)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](mid-fips-enforced.md#)

