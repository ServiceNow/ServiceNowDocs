---
title: Event Management MID Web Server extension form
description: Fields in the form for creating or modifying a MID Web Server extension.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Event Management reference, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management MID Web Server extension form

Fields in the form for creating or modifying a MID Web Server extension.

<table id="table_od5_flc_bx"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the extension for easy identification.

</td></tr><tr><td>

Short description

</td><td>

Brief, meaningful description of the extension.

</td></tr><tr><td>

Status

</td><td>

This field is auto-populated with the status of the extension. The field is blank until the extension is started. After issuing a command to the extension, one of the following values is displayed: -   Started: The extension is running.
-   Stopped: The extension is not running.
-   Offline: The MID Server is down.
-   Error: The extension failed with an error. The error message is displayed in the **Error Message** field.
-   Warning: A run-time exception has occurred. The extension continues to work.

</td></tr><tr><td>

HTTP/HTTPS Port

</td><td>

Port number the extension listens on for incoming requests.

</td></tr><tr><td>

Authentication Type

</td><td>

The available authentication types are: -   **API Key** \(default\): Any client connecting to the extension must enter an API key into the request's authorization header. For details on viewing existing API keys, see [Configure MID Web Server API key authentication](../task/mid-web-server-api-key-authentication.md).
-   **Keybased** \(deprecated and kept only for compatibility with releases prior to the Yokohama release\): The value in the **Secret Key** field is used to generate an authentication token sent in the **Authorization** header of incoming client requests. For details, see [Configure key-based MID Web Server authentication](../task/configure-mid-web-server-extension-metric-data.md).
-   **Basic**: Define a username and password in the **Basic Auth User** and **Basic Auth User Password** fields, which appear when selecting this option.
-   **mTLS**: A certificate-based authentication that uses the TLS protocol. For details, see [MID Web Server and agent mTLS Authentication](../concept/mid-web-server-mTLS-authentication.md).

</td></tr><tr><td>

Secret Key

</td><td>

The value generated when Keybased authentication is selected for the value in the Authentication Type field.

</td></tr><tr><td>

Basic Auth User

</td><td>

Username to be used when selecting Basic authentication.

</td></tr><tr><td>

Basic Auth User Password

</td><td>

Password to be used when selecting Basic authentication.

</td></tr><tr><td>

Secure Connection

</td><td>

Option to indicate that the extension is to use the TLS protocol to encrypt incoming connections. A certificate and private key combination must also be provided to the extension. When selecting this option, the **MID Server Unified Keystore** check box appears.

</td></tr><tr><td>

Use MID Unified Keystore

</td><td>

Option for using the MID Server Unified Keystore option for a secure connection.Clear this option to use **Web Server Keystore**.

 For details, see [Configure a secure MID Web Server extension](../task/configure-midwebserver-extension-secure.md).

</td></tr><tr><td>

Keystore Certificate Alias

</td><td>

The alias name of the keypair inside the selected keystore that the extension uses to establish a secure connection.Leave this field empty to use the default alias when using the MID Unified Keystore or when using the Web Server Keystore with a single alias.

</td></tr><tr><td>

Keystore Password

</td><td>

The password for the Web Server Keystore when it is used to establish a secure connection.

</td></tr><tr><td>

Keystore Key Password

</td><td>

The password of the private key entry mapped to the specified alias of the Web Server Keystore. This field can be left empty if the password matches the entry in the Keystore Password field.

</td></tr><tr><td>

Truststore Password

</td><td>

The password to the truststore that holds the Certificate Authority \(CA\) certificates used to validate the signatures of the client certificates. Appears when the **mTLS** authentication type is selected.Leave this field empty if the extension is configured to use the cacerts truststore of the JRE running the MID Server.

</td></tr><tr><td>

Error Message

</td><td>

Message describing any error that causes a command, such as Start or Stop, to fail. This field appears only when the value in the Status field is Error.

</td></tr><tr><td>

Execute on

</td><td>

Location for running this extension. The available options are **Specific MID Server** or **Specific MID Server Cluster**.

</td></tr><tr><td>

MID Server

</td><td>

Depending on your selection in the **Execute on** field, the name of the designated MID Server or MID Server cluster. -   If you selected **Specific MID Server**, the name of the designated MID Server.
-   If you selected **Specific MID Server Cluster**, the name of the designated MID Server cluster.

</td></tr><tr><td>

Executing on

</td><td>

Displays the name of the MID Server on which the extension is running even if the MID Server is down. If the user stops the extension, this field is empty.

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

