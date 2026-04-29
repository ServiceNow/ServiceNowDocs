---
title: OAuth 2.0 authentication via MID Server using external credential storage
description: Store OAuth 2.0 credentials-client ID and client secret-in the CyberArk vault instead of the ServiceNow instance. The MID Server gets the credentials from the CyberArk vault, when required to get the OAuth token. The token is stored in the MID Server and refreshed automatically upon expiry.
locale: en-US
release: australia
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [External credential storage, Get started with credentials, Connections and Credentials, Access Management]
---

# OAuth 2.0 authentication via MID Server using external credential storage

Store OAuth 2.0 credentials-client ID and client secret-in the CyberArk vault instead of the ServiceNow instance. The MID Server gets the credentials from the CyberArk vault, when required to get the OAuth token. The token is stored in the MID Server and refreshed automatically upon expiry.

The CyberArk Application Identity Management \(AIM\) product uses the Privileged Account Security solution to eliminate the need to store application passwords embedded in applications, scripts or configuration files, and allows these highly sensitive passwords to be centrally stored, logged, and managed within the CyberArk vault. You can configure the CyberArk vault to store OAuth 2.0 credentials rather than directly in a ServiceNow credentials record. To know more about CyberArk, see [CyberArk credential storage integration](c_CyberArkCredStorageIntegrate.md).

## Architecture of OAuth 2.0 authentication of MID Server request

The architecture has two parts: ServiceNow instance and the environment where the Application Identity Manager \(AIM\) client and the MID Server are configured. Examples of environment are the cloud or a customer environment.

The MID Server and the Application Identity Manager \(AIM\) client must be configured on the same environment and the Application Identity Manager \(AIM\) must be configured to interact with the CyberArk external vault. The CyberArk external vault could be hosted in the same environment as that of MID Server and the Application Identity Manager \(AIM\) or a different environment.

The ServiceNow instance maintains credential identifiers that map to specific OAuth 2.0 credentials stored in the CyberArk vault. Before sending an OAuth token request, the MID Server obtains the credential identifier from the instance, and then uses a customer-provided JAR file to send the identifier to the AIM client. The AIM client sends the request to CyberArk vault. The CyberArk vault sends the OAuth 2.0 credentials back to the MID server through the AIM client. After receiving the OAuth 2.0 credentials, the MID server sends the OAuth token request to the third-party authorization server. The token request comprises information such as client and client secret that CyberArk stores, and OAuth scope, and token URL that the instance stores. After the authorization server issues the OAuth token, the MID server stores it in its cache memory.

**Note:** This feature supports the Client Credentials Grant Type.

The image shows the MID server request authentication process.

**Note:** It's assumed that the third-party authorization server and the CyberArk vault are hosted in the customer network.

![MID server request authentication process.](../image/oauth-2.0-external-storage.png)

-   **[Configure a JAR file and credential identifiers](../task/configure-and-import-jar-file.md)**  
Configure a JAR file and credential identifiers so that the JAR file resolves the credential identifiers into actual credentials from the CyberArk external vault. The process enables the MID Server to get and include OAuth 2.0 credentials in the OAuth token request.
-   **[Configure CyberArk](../task/configure-cyberark.md)**  
Configure the CyberArk vault to store OAuth 2.0 credentials and respond to requests for OAuth 2.0 credentials from the MID Server.
-   **[Configure a connection to send OAuth request via the MID Server using external vault](../task/configure-oauth-2-0-authentication.md)**  
Configure a connection to send requests for OAuth 2.0 tokens to a third-party auth server via the MID Server. The MID Server adds OAuth 2.0 credentials \(Client ID and Client Secret\) from the CyberArk external vault, OAuth scope, and token URL from the instance to the request and sends them to the third-party auth server.

**Parent Topic:**[External credential storage](c_ExternalCredentialStorage.md)

