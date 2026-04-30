---
title: Configure a secure MID Web Server extension
description: Configure a TLS listener for extra security and encryption of data transferred to and from the MID Web Server extension. Access both a private key and a certificate \(or certificate chain\) from a Java keystore to use during the TLS handshake where the MID Web Server and the client acknowledge each other.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure a secure MID Web Server extension

Configure a TLS listener for extra security and encryption of data transferred to and from the MID Web Server extension. Access both a private key and a certificate \(or certificate chain\) from a Java keystore to use during the TLS handshake where the MID Web Server and the client acknowledge each other.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **MID Server** &gt; **Extensions** &gt; **MID Web Server**.

2.  Select **New**.

3.  In the **Authentication Type** field, select an authentication type to be used.

    -   Keybased – See [Configure key-based MID Web Server authentication](configure-mid-web-server-extension-metric-data.md)
    -   Basic – Standard username/password authentication
    -   API key – See [Configure MID Web Server API key authentication](mid-web-server-api-key-authentication.md)
    -   mTLS – See [MID Web Server and agent mTLS Authentication](../concept/mid-web-server-mTLS-authentication.md)
4.  Select either the MID unified keystore or the web server keystore.

    The MID Web Server unified keystore is the most efficient option. If you want to enable backward compatibility and the ability to store keypairs in an additional keystore, use the Web server keystore \(which allows you to use the MID unified keystore as well\).

<table id="choicetable_ezm_tvg_dsb"><thead><tr><th align="left" id="d78300e151">

Option

</th><th align="left" id="d78300e154">

Description

</th></tr></thead><tbody><tr><td id="d78300e160">

**MID unified keystore**

</td><td>

1.  Select the **Use MID Unified Keystore** check box
2.  Enter an alias name in the **Keystore Certificate Alias** field or leave the field empty to use the keystore's default alias.

For more information, see the **Install custom certificates in the MID Server unified key store** section in [MID Server unified key store](https://www.servicenow.com/docs/access?context=mid-unified-keystore&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Important:** Leaving the **Keystore Certificate Alias** field empty causes connecting clients to skip certificate verification. Instead, the MID Server uses its own self-signed certificate.

</td></tr><tr><td id="d78300e203">

**Web server keystore**

</td><td>

1.  Clear the **Use MID Unified Keystore** check box.
2.  Specify an alias name in the **Keystore Certificate Alias** field or leave the field empty if you have a single alias in that keystore.
3.  If the password to the private key of the required alias is different from the keystore password, specify the alias in the **Keystore Key Password** field.
4.  Enter the keystore password in the **Keystore Password** field.


</td></tr></tbody>
</table>
**Parent Topic:**[Configure the MID Web Server extension](configure-mid-web-server-extension.md)

**Related topics**  


[Connect the agent to the MID Server using mTLS](../../agent-client-collector/task/enable-tls-agent.md)

