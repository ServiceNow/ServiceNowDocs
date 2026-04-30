---
title: Configure a JAR file and credential identifiers
description: Configure a JAR file and credential identifiers so that the JAR file resolves the credential identifiers into actual credentials from the CyberArk external vault. The process enables the MID Server to get and include OAuth 2.0 credentials in the OAuth token request.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [OAuth 2.0 authentication via MID Server using external credential storage, External credential storage, Getting started with credentials, Connections and Credentials, Access Management]
---

# Configure a JAR file and credential identifiers

Configure a JAR file and credential identifiers so that the JAR file resolves the credential identifiers into actual credentials from the CyberArk external vault. The process enables the MID Server to get and include OAuth 2.0 credentials in the OAuth token request.

## Before you begin

Role required: agent\_admin or admin

The CyberArk external vault stores sensitive credentials and the ServiceNow instance stores credential identifiers that map to the specific credential names that the vault stores. The JAR file enables the mapping of a credential identifier to a specific credential name in the external vault. The mapping enables the MID Server to acquire and include the required credential in the OAuth token request. You must configure the credential identifiers and the JAR file in the ServiceNow instance and the MID Server respectively.

## Procedure

1.  [Import the CyberArk JAR file](t_ImportTheCyberArkJARFile.md).

2.  [Configure a connection to send OAuth request via the MID Server using external vault](configure-oauth-2-0-authentication.md).


**Parent Topic:**[OAuth 2.0 authentication via MID Server using external credential storage](../concept/oauth-2-0-support-in-external-credential.md)

